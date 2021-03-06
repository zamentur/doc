# Transmission

### Téléchargement des fichiers complétés

Avec un navigateur web, si Transmission est installé sur `https://votre-domaine.org/torrent/` vous pourrez télécharger vos fichiers complétés à l’adresse suivante : https://votre-domaine.org/torrent/downloads/

### Comment télécharger un répertoire entier

En ligne de commande, il faut se placer dans le répertoire de téléchargemement et archiver le répertoire :
```bash
cd /home/yunohost.transmission/completed
zip -r votre_archive.zip [dossier]
```
### Transfert de fichier de son ordinateur de bureau vers YunoHost pour le partage
#### Avec SFTP
À partir de votre gestionnaire de fichier :
```bash
sftp://<utilisateur>@<votre-domaine.org>/home/yunohost.transmission/completed
```

#### Avec SCP

Dans YunoHost, les torrents completés sont enregistrés dans :
/home/yunohost.transmission/completed

Pour transferer le fichier entrez la commande suivante :

```bash
scp (-r) /votre/fichier/ root@votre-domaine.org:/home/yunohost.transmission/completed
```
Pour plus de détails sur le transfert de fichier voir ici : http://doc.ubuntu-fr.org/ssh#transfert_-_copie_de_fichiers

[Site de transmission](http://transmissionbt.com/)

