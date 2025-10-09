# T03: Seguretat Lògica — recuperant accés a sistemes

## Breu descripció

Després de la primera feina exitosa, us arriba un encàrrec urgent. Rebreu formació prèvia sobre seguretat lògica per afrontar la tasca.

Un client ha portat un portàtil amb **Zorin OS** (Linux amb entorn gràfic). El directiu usuari ha oblidat la contrasenya i cal recuperar l’accés perquè hi ha documentació important. Per evitar riscos sobre l’equip original, el disc s’ha **clonat** i se us ha lliurat el **disc virtual** per treballar sobre la còpia.

Objectius principals:

- Recuperar l’accés al sistema Linux (Zorin OS) des del disc virtual clonat.  
- Identificar l’usuari existent i assignar-li una nova contrasenya.  
- Investigar i implementar mesures per **fortificar l’accés al GRUB** (protecció amb contrasenya i bones pràctiques).  
- Documentar tot el procediment amb captures i pujar-ho al repositori.

---

## Procediment individual (resum de passos)

### 1. Preparar l’entorn
- Crear una **màquina virtual (VM)** (per exemple VirtualBox, VMware, etc.).  
- Connectar el **disc virtual** proporcionat a la VM com a dispositiu d’arrencada o segon disc, segons es requereixi.

---

### 2. Vulnerar l’accés al GRUB del Linux (recuperació)
- Arrencar la VM i, en el menú del **GRUB**, editar l’entrada del kernel per obtenir un shell de recuperació:
  - Opció 1: Editar la línia de kernel i afegir `init=/bin/bash`.  
  - Opció 2: Arrencar en mode **single-user** (`systemd.unit=rescue.target` o `single`) segons la versió i configuració.
- Aquest pas pot donar accés a una shell amb permisos root (dependrà de la configuració; pot ser necessari remuntar el sistema en lectura-escriptura).

---

### 3. Identificar l’usuari del sistema
- Un cop a la shell/entorn de recuperació, identificar els usuaris disponibles:
  - Consultar `/etc/passwd`:
    ```bash
    cat /etc/passwd | grep "/home"
    ```
  - O llistar directoris de /home:
    ```bash
    ls -la /home
    ```

---

### 4. Modificar la contrasenya
- Si el sistema està muntat en només lectura, remuntar-lo en lectura-escriptura:
  ```bash
  mount -o remount,rw /

