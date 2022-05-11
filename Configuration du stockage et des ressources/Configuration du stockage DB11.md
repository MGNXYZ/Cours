# Configuration du stockage et des ressources Debian 11

## A. <ins>**Configuration du stockage Debian 11.**<ins>

- <ins>**Partitionnement des disques**<ins>
 
1. - <ins>Nous allons créer 3 partitions<ins>

> Ils nous faudra passer en super utilisateurs avec la commande ```su -``` puis lister les disques avec la commande ```fdisk -l``` pour connaitre le nom du disque à partitionner.

![image](https://user-images.githubusercontent.com/95431446/167848183-d0e4936c-efa3-4373-b8e2-4d11d6255eae.png)

> On utilisera ensuite la commande  ```fdisk /dev/sda``` pour ce placer sur le disque sda.

![image](https://user-images.githubusercontent.com/95431446/167849378-12d236e1-a9c5-45b9-b975-f1867393743b.png)

🛑 **_Attention_ il faut suivre la procédure a la lettre** 

- **Première partition :**

```
n : créer une nouvelle partition
p : type de partition primaire
Laisser le numéro de partition par défaut
Laisser le premier secteur par défaut
+15G pour ajouter 15Go 
```

- **Deuxième partition :**

```
n : créer une nouvelle partition
p : type de partition primaire
Laisser le numéro de partition par défaut
Laisser le premier secteur par défaut
+15G pour ajouter 15Go 
```

- **Troisième partition :**

```
n : créer une nouvelle partition
p : type de partition primaire
Laisser le numéro de partition par défaut
Laisser le premier secteur par défaut
Laisser le dernier secteur par défaut pour occuper tout l'espace restant
```

![image](https://user-images.githubusercontent.com/95431446/167853379-71f59627-7fac-4ff9-8a41-2769e84cce6f.png)

> Quitter fdisk en utilisant la commande ```w``` afin d'écrire les modifications.

2 - <ins> Installons le paquet xfsprogs pour pouvoir utiliser le système de fichier xfs<ins>.

> On utilise la commande ```apt install xfsprogs```.

> on formate nos 3 disques précédemment créer avec la command ```mkfs.``` suivi du type de système de fichiers et de leur nom ainsi que du chemin de la partition voir ci-dessous.

```
mkfs.ext4 -L PROFILS /dev/sda1
mkfs.ext4 -L DATA /dev/sda2
mkfs.xfs -L LOGS /dev/sda3
```

![image](https://user-images.githubusercontent.com/95431446/167856752-5baf009f-c35e-4dc6-a7cd-19553c201b15.png)

## FIN partie 1.

## B. <ins>**Occupation des espaces disques**<ins>

- <ins>**Finalement, l’espace alloué au dossier contenant les profils utilisateurs « /home » a été sous-estimé, nous allons donc le remplacer par le volume nommé "PROFILS"**<ins>

> Nous allons commencer par faire un backup du répertoire home en préservant les droits de nos utilisateurs avec la commande : 
> ```cp -rp /home /tmp/home-backup```

![image](https://user-images.githubusercontent.com/95431446/167858589-69b8c927-1577-4982-bf61-847408e9be60.png)


> Nous allons ensuite modifier le fichier "/etc/fstab" avec vim a l'aide de la commande : 
>``` vim /etc/fstab```

> Nous commentons la ligne contenant /home avec un "#".

![image](https://user-images.githubusercontent.com/95431446/167859115-0039891f-e440-4f20-8ac2-1342037872f2.png)

> On ajoute ensuite la ligne permettant de monter la partition "PROFILS" dans "/home" puis ```:wq``` pour enregistrer et quitter.
> On ajoute la ligne "LABEL=PROFILS /home ext4 defaults 0 2" 

![image](https://user-images.githubusercontent.com/95431446/167860215-5ef896b1-9fad-4d01-a376-e8ea6f27d952.png)

> On utilise ensuite ```mount -a``` pour enregistrer les modifications et monter la partitions.

> On copie ensuite notre backup de home dans la partition nouvellement créer : 
> A l'aide de la commande ```cp -rp /tmp/home-backup/* /home/```
> ```ls /home``` pour vérifier que tout c'est bien passé.

![image](https://user-images.githubusercontent.com/95431446/167862015-43e33b96-d9d0-4faf-8579-96874ddcc749.png)


## FIN partie 2

## C. <ins>**Dossiers de service**<ins>

- <ins>**Nous allons maintenant mettre en commun les données des services dans le volume "DATA" il sera monté dans le dossier "/services" 

> On commence par créer "/services" avec la commande ```mkdir -p /services/```
> ```cd /services``` puis ```mkdir commercial comptabilite direction informatique logistique```

- <ins>**On va ensuite accorder les droits a chaque dossier qui correspond a leur services.**<ins>

> On ce rend dans "services" ```cd /services```
> Ensuite suivre les commandes ci-dessous : 
```
chown :commercial commercial
chown :comptabilite comptabilite
chown :direction direction
chown :informatique informatique
chown :logistique logistique
```
> On change les droits de tout les répertoires avec la commande ```chmod g+x *```

![image](https://user-images.githubusercontent.com/95431446/167870580-59967d71-43b8-46a3-b866-9fe6a61007ce.png)

##FIN
