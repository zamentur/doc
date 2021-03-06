# Copier l'image sur une carte SD

Maintenant que vous avez l'image ISO YunoHost, vous devez la copier sur une carte SD. Le processus est différent suivant votre système d'exploitation.

<img src="https://yunohost.org/images/sdcard.jpg" width=150>

## Sur Windows

* Téléchargez et installez **[Win32 Disk Imager](http://sourceforge.net/projects/win32diskimager/)**.
* Insérez votre carte SD.
* Copiez le fichier `.img` sur votre carte SD en utilisant *Win32 Disk Imager*.

<img src="https://yunohost.org/images/win32diskimager.png">

## Sur GNU/Linux, BSD or Mac OS

* Ouvrez un terminal.
* Insérez votre carte SD.
* Identifiez votre matériel en tapant :

```bash
sudo fdisk -l
```

Ça devrait être `/dev/diskN`, où `N` est un nombre, ou `/dev/sdX`, où `X` est une lettre.

* Copiez l'image en tapant :

```bash
sudo dd bs=1M if=/chemin/vers/votre/.img of=/nom/du/matériel
```

<span class="glyphicon glyphicon-warning-sign"></span> N’oubliez pas de changer `/chemin/vers/votre/.img` et `/nom/du/matériel` par les valeurs appropriées.

La commande peut prendre quelques minutes, puis votre carte SD sera prête à être utilisée. **:-)**

## Étendre la partition root <small>(facultatif)</small>

Par défaut, la partition root de votre carte SD est très petite.   
Vous pouvez la redimensionner en utilisant un logiciel comme `resize2fs` (ligne de commande) ou `Gparted` (interface graphique).

<img src="https://yunohost.org/images/gparted.jpg" style="max-width:100%;border-radius: 5px;border: 1px solid rgba(0,0,0,0.15);box-shadow: 0 5px 15px rgba(0,0,0,0.35);">

<p class="text-muted">Aperçu de l'interface de Gparted</p>