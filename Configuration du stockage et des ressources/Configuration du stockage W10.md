# <ins>Configuration du stockage et des ressources Windows 10<ins>

- ## Partitionnement d'un disque. 

- On va utilisé DISKPART dans l'invite de commande pour créer une partition DATA sur notre deuxième disque dur au format MBR.

> On lance l'invite de commande ``` cmd ``` dans la barre de recherche clique droit exécuter en tant qu'administrateur.
> On tape ensuite ```DISKPART```

![image](https://user-images.githubusercontent.com/95431446/167811867-9cc0abc5-e972-423e-b509-5a61314b303c.png)

> On va lister les disques avec la commande ``` list disk ```

![image](https://user-images.githubusercontent.com/95431446/167812834-f8e8556e-b39e-4660-ad0c-36fcc2bf6777.png)

> On selectione le disque 1 avec la commande ``` select disk 1 ```

![image](https://user-images.githubusercontent.com/95431446/167813104-80158ad3-64c9-4b05-998e-d59ee70bdb3a.png)

> ``` list disk ``` a nouveau pour voir si DISKPART a bien sélectionner le disque 1

![image](https://user-images.githubusercontent.com/95431446/167814529-a7dc5370-3d78-4aa7-b36b-e1d7c2c8da8a.png)

> On met hors ligne le disque avec ```offline disk``` puis on le réactive avec ```online disk``` 

![image](https://user-images.githubusercontent.com/95431446/167814927-6c7177bf-4908-4337-8ca2-8846e2f1c066.png)

> On converti ensuite le disque au format MBR avec la commande ``` convert MBR ```

![image](https://user-images.githubusercontent.com/95431446/167815278-5b12e785-4efb-4804-b457-730b4bd2c912.png)

> On va maintenant créer la partition de 15GO avec la commande ```create partition primary size=15000```

![image](https://user-images.githubusercontent.com/95431446/167815594-8b9e9f30-3e89-493f-b647-150741e656bd.png)

> On va maintenant donner le nom DATA a notre partition avec la commande ``` format fs=ntfs label="DATA" ```

![image](https://user-images.githubusercontent.com/95431446/167816125-4198bbde-4658-469c-8dbb-eb46bc255a36.png)

> On lui assigne la lettre E avec la commande ```assign letter=E```

![image](https://user-images.githubusercontent.com/95431446/167816665-9eff35ac-f073-4b5e-98d2-ecdf428078a4.png)

> ``` Exit ``` pour quitter DISKPART

- Il nous reste plus qu'a vérifier que le volume est disponible.

> _Vérifions depuis DISKPART avec la commande ``` detail disk ```_

![image](https://user-images.githubusercontent.com/95431446/167818159-d4600df3-848d-4fcf-9533-81c82a67ae48.png) 

> _Dans l'explorateur de fichier._

![image](https://user-images.githubusercontent.com/95431446/167817376-db29e77d-c724-4cf9-ace3-001e9574569f.png)

> _On peut également utiliser la commande ```wmic logicaldisk get deviceid, volumename, description```_

![image](https://user-images.githubusercontent.com/95431446/167817456-62dd45ed-ad93-4fa0-ab19-34a09f5ed1ca.png)

## FIN
