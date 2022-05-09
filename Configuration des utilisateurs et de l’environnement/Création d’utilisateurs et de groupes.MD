# Création d’utilisateurs et de groupes

## <ins>Créations des groupes et compte sur windows 10<ins>

- ### <ins>Création des utilisateurs et des groupes de la direction et de la comptabilité via l'invite de commandes.<ins>

- On commence par créer les groupes : Direction et Comptabilité 

> On utilise la commande : ``` net localgroup 'nom du groupe' /add ```

![image](https://user-images.githubusercontent.com/95431446/167437082-165dde0a-999a-4873-88c7-0815f74ec343.png)
_création des utilisateurs_

> Il est possible de créer un commentaire pour les groupes a l'aide de la commande : 
``` net localgroup 'nom du groupe' /comment:"commentaire" ```

![image](https://user-images.githubusercontent.com/95431446/167441102-14eb3fd3-0cfc-4e58-afc3-304b21b012ff.png)
_ajout de commentaire pour nos groupes_

- On ajoute ensuite les utilisateurs et leur mots de passe : 

> On utilise la commande : ``` net user 'utilisateur' 'password' /add ```

![image](https://user-images.githubusercontent.com/95431446/167437829-409fd37e-097d-4515-8d66-4283907c7fa9.png)
_ajout de l'utilisateur rgrimes avec sont mot de passe_

- Enfin nous ajoutons les utilisateurs a leur groupes respectif : 

> On utilise la commande ``` net localgroup 'nom du groupe' 'nom de l'utilisateur' /add ```

![image](https://user-images.githubusercontent.com/95431446/167439628-06a86f0b-1559-4f30-ba81-d775706cbd29.png)
_ajout de rgrimes au groupe Direction_


- ###  <ins>Création des utilisateurs et des groupes informatiques et logistique via Powershell.<ins>

**On lance Powershell en mode _administrateur_**

![image](https://user-images.githubusercontent.com/95431446/167442192-b7610897-cf68-4a33-acf5-042d93137fc8.png)
_clique droit exécuter en tant qu'administrateur_

- On commence par créer nos groupe : 

> On utilise la commande ``` 
