# <ins>**Configuration avancée système Debian**<ins>

## A. <ins>**Afin d’accélérer le démarrage du système, nous allons passé le système d'affichage d'amorçage de grub a 2scd.**<ins>

- <ins>Il nous faut aller éditer le fichier ```etc/dafault/grub``` afin de modifier l'entrée "GRUB_TIMEOUT" avec la valeur "2"<ins>

> On utilise la commande ```vim /etc/default/grub``` une fois notre "GRUB_TIMEOUT" modifier nous enregistrons avec la commande vim ```:wq```.

![image](https://user-images.githubusercontent.com/95431446/168102281-1b897e56-4f78-447b-b408-2cb4ca8545e1.png)

![image](https://user-images.githubusercontent.com/95431446/168102775-76460614-9b4f-40b5-ace4-a33deaa4ad99.png)

-<ins>Nous allons ensuite mettre a jour grub<ins>

> On utilise la commande ```update-grub ou grub2-mkconfig -o /boot/grub/grub.cfg```

![image](https://user-images.githubusercontent.com/95431446/168103354-f89a9517-ba28-41c9-a299-0c5c415d91b9.png)

## B. <ins>**On ce rend compte que notre espace swap n'est pas suffisant nous allons donc l'étendre a 1GO**<ins>

- <ins>**Nous ajouterons 1GO au swap a l'aide de la commande suivante**<ins>
 
```lvresize -L+1G /dev/VGgroupe/LVswap```

![image](https://user-images.githubusercontent.com/95431446/168110996-88c6d14b-a678-4d3d-8208-878e5cddd6ac.png)

## C. <ins>**Nous mettons a jours l'intégralité de nos paquets avec la commande suivante**<ins>

> ```apt upgrade```

![image](https://user-images.githubusercontent.com/95431446/168111379-4cf688f6-e758-447d-a369-1e16e7458058.png)

##FIN
