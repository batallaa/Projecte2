# T03: Seguretat Lògica — recuperant accés a sistemes

## Part 1: Canvi de password

![Foto 01 guia](img/01.png)

Entrem a la màquina que hem creat amb el disc de Miquel Valls. Si no s’obra aquesta configuració, pressionarem en el moment d’arrancada de la màquina `**SHIFT + tecla aleatòria**`.

Seleccionem **“Advanced options for Zorin”**.

![Foto 02 guia](img/02.png)

Aquí seleccionem qualsevol de les dos opcions que s’indiqui **“recovery mode”**, per poder anar a l’apartat de root on canviarem el password.

![Foto 03 guia](img/03.png)

Si intentem canviar la contrasenya ara, ens sortirà un missatge d’error, per això abans de tot hem de fer:  `**mount -rw -o remount /**`

![Foto 04 guia](img/04.png)
![Foto 05 guia](img/05.png)

Montem el arxiu en mode lectura/escriptura abans de poder fer canvis.  
A continuació, per poder canviar la contrasenya hem de saber el seu user, per això farem un `cat` a la carpeta de contrasenyes i filtrarem només la informació que contingui “Miquel Valls”, amb la comanda:  `**cat /etc/passwd | grep “Miquel Valls”**`

![Foto 06 guia](img/06.png)

Amb `passwd miquel(nom d'usuari)` podem canviar la contrasenya de l’usuari.  
A continuació d’haver posat la comanda, haurem d’escriure dos vegades la contrasenya que vulguem, i ja es faran els canvis.

---

## Part 2: Fortificació del Grub

![Foto 07 guia](img/07.png)

Per primer pas al entrar, serà establir una contrasenya, per això entrarem al grub i a l’apartat de root posarem: `**sudo grub-mkpasswd-pbkdf2 (contrasenya)**`

![Foto 08 guia](img/08.png)

Amb `nano /etc/grub.d/40.custom` entrem a l’arxiu per editar i poder posar una contrasenya al grub.  
Després, ens donarà la contrasenya en format hash.

![Foto 09 guia](img/09.png)

Un cop obrim l’arxiu, haurem d’afegir abaix del codi:

`**set superusers="usuari_exemple"**`
`**password_pbkdf2 usuari_exemple hash.exemple**`

Quan acabem, tanquem l’arxiu guardant els canvis.

![Foto 10 guia](img/10.png)

I actualitzem el grub amb: `**sudo update-grub**`

![Foto 11 guia](img/11.png)

Per guardar la configuració, fem: `**sudo grub-mkconfig -o /boot/grub/grub.cfg**`

![Foto 12 guia](img/12.png)

I ara quan entrem, ens demanarà que possem l’usuari i la contrasenya que hem possat.
