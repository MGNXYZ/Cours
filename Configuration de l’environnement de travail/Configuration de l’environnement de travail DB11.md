# <ins>Configuration de l'environnement de travail Debian 11<ins>

## <ins>Création des restrictions<ins>

- <ins>**Désactivation des repos deb-src**<ins>

_On passe en route avec ``` su - ```_

- <ins>On va ensuite éditer la sources.list avec Vim<ins> 

> Il nous faut d'abord installer vim ``` apt install vim ```

> On fait ensuite tape ensuite la commande ``` vim /etc/apt/sources.list ```

![image](https://user-images.githubusercontent.com/95431446/167804753-79ff25c4-43fb-4176-b265-0211482b58be.png)

> Un fois dans vim on utilise ``` : ``` pour entrer dans le mode commande de vim.
> On va ensuite activer la numérotation des lignes dans vim ``` :set nu```

![image](https://user-images.githubusercontent.com/95431446/167808236-03cce22b-fe15-41be-b95c-093cb7c6072b.png)

> On active aussi la colorisation syntaxique avec ``` :syntax on ```

![image](https://user-images.githubusercontent.com/95431446/167808591-b61bf6bb-03fd-4417-ad65-a70376c53b56.png)

> On saisi la commande ``` :g/^deb-src/s/^/#/g ```

![image](https://user-images.githubusercontent.com/95431446/167805223-a0c7e266-9d38-4e05-a93a-43ee820417fe.png)

![image](https://user-images.githubusercontent.com/95431446/167805329-582aafc0-2066-4d0e-ae97-25132f4b00d6.png)

> Plus qu'a enregistrer et quitter avec la commande ``` :wq ```

![image](https://user-images.githubusercontent.com/95431446/167805491-c9600654-fd70-4acc-9126-4e4e95df84a6.png)

## FIN
