# <ins>**Configuration de l’environnement de travail W10**<ins>

- ## <ins>Création d'une console de management.<ins>

- <ins>**Avant de commencer on va créer une console de management.**<ins> 

> On tape ``` mmc ``` dans la barre de recherche.

![image](https://user-images.githubusercontent.com/95431446/167690990-1140f52c-7afa-4da4-bea0-906a09d0bf96.png)

- <ins>On ajoute un composant logiciel.<ins>

![image](https://user-images.githubusercontent.com/95431446/167691234-79b17710-2f00-494b-96fa-dfefe169fe4b.png)

- <ins>On ajoute Editeur d'objet de stratégie de groupe.<ins>

![image](https://user-images.githubusercontent.com/95431446/167692105-32d97851-4dcd-43e0-8463-bc284e0d193d.png)

- <ins>Avant de terminer cette opération ils faut créer une exception pour les administrateurs.<ins>

> On clique sur Parcourir

![image](https://user-images.githubusercontent.com/95431446/167692625-1d093227-b0cd-4310-b527-f6b467deb60b.png)

- <ins>Puis on clique sur Utilisateurs suivi de Non-administrateurs et enfin on clique sur ok<ins>

![image](https://user-images.githubusercontent.com/95431446/167693093-6e4c1156-df4d-4346-8451-0403a16515a3.png)

![image](https://user-images.githubusercontent.com/95431446/167693701-7f3a5077-3691-4111-8b7e-0145a964f0d7.png)

![image](https://user-images.githubusercontent.com/95431446/167693775-845dcf3a-a927-4962-8dd6-2e1fc5384e19.png) 

- ## <ins>**On va maintenant supprimer les options de gravure CD et empêcher l'accès au CD et DVD**<ins>

![image](https://user-images.githubusercontent.com/95431446/167694338-db188ce3-6091-4291-834a-c258604c9388.png)
_On navigue dans l'onglet de gauche comme dans la capture d'écran_

![image](https://user-images.githubusercontent.com/95431446/167694823-e1feb941-e1a4-4159-a5d8-a5fb1f64e5d9.png)

- On double clique puis on active la règle **on répéte ensuite l'opération sur _refuser l'accès en écriture_.** 

![image](https://user-images.githubusercontent.com/95431446/167695031-c208795b-fd33-44cd-80e8-b022662e9803.png)

- ## <ins>**On va ensuite désactiver le windows store**<ins>

- On ce rend sur composant Windows puis Windows store et on désactive l'application.

![image](https://user-images.githubusercontent.com/95431446/167696486-db2ff367-c8c9-4055-bea2-0766528d2f49.png)

- ## <ins>**On va ensuite désactiver regedit**<ins>

- On ce rend sous modèles administrateurs > Système et on active la règle "Empêche l'accès aux outils de modifications du Registre"

![image](https://user-images.githubusercontent.com/95431446/167696970-07f94f8c-3811-4073-84e2-61a3dd94bee8.png)

- ## <ins>**Il nous faut maintenant mettre un fond d'écran par défaut**<ins>

- On ce rend alors dans "Bureau" > "Bureau" .

![image](https://user-images.githubusercontent.com/95431446/167697473-03f7b219-b0ac-4e9e-afe8-cfa33b186ab8.png)

- On renseigne le chemin d'accès de notre image.

![image](https://user-images.githubusercontent.com/95431446/167697769-1e15d5fa-5e17-48b7-a3c3-21850cdb1ea7.png)

- ## <ins>**Maintenant on va modifier les paramètres du Pare-feu Windows pour qu'il soit toujours activé**<in>

**_Il faut qu'on ajoute un nouveau composant groupe local mais sans Non-Administrateurs_**

- <ins>On ce rend ensuite dans Configuration ordinateur > Paramètres de sécurité > Pare-feu Windows Defender<ins>

![image](https://user-images.githubusercontent.com/95431446/167700323-a9f58700-7f6c-450a-8881-d30455f01c0f.png)

- <ins>On active le Pare feu pour **_tout_** les profils<ins>

![image](https://user-images.githubusercontent.com/95431446/167700931-b78be5e3-a073-4b88-a8fb-b7ee9632f3f1.png)

- ## <ins>**Bravo c'est presque finis on va maintenant vérifier si toute nos règles sont bien activé**<ins>

- <ins>On ouvre l'invite de commandes<ins> 

> On va maintenant utilisé la commande ```gpupdate``` pour appliquer les GPO suivi d'un ```gpresult /R``` pour voir si elle s'applique correctement.

![image](https://user-images.githubusercontent.com/95431446/167701894-1e70111c-83d3-4d0b-9d2b-0ed2523024e3.png)

![image](https://user-images.githubusercontent.com/95431446/167702019-6bb56e8c-1450-4334-b5bb-01119c1a73df.png)

## FIN
