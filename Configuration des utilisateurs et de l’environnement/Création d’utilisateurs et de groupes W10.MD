# Création d’utilisateurs et de groupes

## <ins>Créations des groupes et comptes sur windows 10<ins>

- ### <ins>Création des utilisateurs et des groupes de la direction et de la comptabilité via l'invite de commandes.<ins>

- <ins>**On commence par créer les groupes : Direction et Comptabilité.**<ins> 

> On utilise la commande : ``` net localgroup 'nom du groupe' /add ```

![image](https://user-images.githubusercontent.com/95431446/167437082-165dde0a-999a-4873-88c7-0815f74ec343.png)

 _création des utilisateurs_

> Il est possible de créer un commentaire pour les groupes a l'aide de la commande : 
``` net localgroup 'nom du groupe' /comment:"commentaire" ```

![image](https://user-images.githubusercontent.com/95431446/167441102-14eb3fd3-0cfc-4e58-afc3-304b21b012ff.png)

 _ajout de commentaire pour nos groupes_

- <ins>**On ajoute ensuite les utilisateurs et leur mots de passe :**<ins> 

> On utilise la commande : ``` net user 'utilisateur' 'password' /add ```

![image](https://user-images.githubusercontent.com/95431446/167437829-409fd37e-097d-4515-8d66-4283907c7fa9.png)

 _ajout de l'utilisateur rgrimes avec sont mot de passe_

- <ins>**Enfin nous ajoutons les utilisateurs a leur groupes respectif :**<ins> 

> On utilise la commande ``` net localgroup 'nom du groupe' 'nom de l'utilisateur' /add ```

![image](https://user-images.githubusercontent.com/95431446/167439628-06a86f0b-1559-4f30-ba81-d775706cbd29.png)

 _ajout de rgrimes au groupe Direction_


- ###  <ins>Création des utilisateurs et des groupes informatiques et logistique via Powershell.<ins>

- <ins>**On lance Powershell en mode _administrateur_**<ins>

![image](https://user-images.githubusercontent.com/95431446/167442192-b7610897-cf68-4a33-acf5-042d93137fc8.png)

 _clique droit exécuter en tant qu'administrateur_

- <ins>**On commence par créer nos groupe :**<ins> 

> On utilise la commande ``` New-LocalGroup -Name "nom du groupe" -Description "desc. du groupe" ```

![image](https://user-images.githubusercontent.com/95431446/167573955-56bae475-b6a6-400a-8d76-bb6dc59268a6.png)

 _Création du groupe Informatique_

- <ins>**On créer ensuite les utilisateurs des groupes avec une description et leur mots de passe.**<ins> 

> On utilise la commande ```  New-LocalUser -Name "Nom d'utilisateur"  -Description "La desc." ``` powershell nous demande alors le mot de passe

![image](https://user-images.githubusercontent.com/95431446/167580158-8f0c6935-8037-486a-8fc9-1277cdd031ba.png)

 _Création de l'utilisateur bman_

- <ins>**On ajoute ensuite les utilisateurs a leur groupe respectif.**<ins> 

> On utilise la commande ``` Add-LocalGroupMember -Group "nom du groupe" -Member "utilisateur" ```

![image](https://user-images.githubusercontent.com/95431446/167580795-dc2dab3d-04b1-489c-938e-4ae7de6c0429.png)

 _ajout de llamblot au groupe Informatique_

- ### <ins>Création d'un utilisateur via l'interface graphique<ins>

- <ins>**On ce rend dans _Gestion de l'ordinateur_.**<ins>

![image](https://user-images.githubusercontent.com/95431446/167583304-a8b8bf90-69dc-435b-a54a-66b2e6cffab1.png)

- <ins>**On ce rend ensuite dans l'onglet Utilisateurs et groupes locaux**<ins>

![image](https://user-images.githubusercontent.com/95431446/167583463-858125d8-5a78-447c-b140-ba09aac68747.png)

- <ins>**Puis utilisateurs**<ins> 

![image](https://user-images.githubusercontent.com/95431446/167583645-710d537c-d2d1-4abc-865f-a84f09ab934f.png)

- <ins>**Clique droit "Nouvel utilisateur..."**<ins>

![image](https://user-images.githubusercontent.com/95431446/167584214-3ed0047b-cff3-4bd4-b831-32675f3137c4.png)

- <ins>**On rempli avec les informations de notre excel**<ins> 

![image](https://user-images.githubusercontent.com/95431446/167585184-3dafc05d-4e20-4cce-aa9c-2e2ce9fafa0c.png)

 _création du compte de gstokes_

- <ins>**On ce rend ensuite dans l'onglet Groupes.**<ins>

![image](https://user-images.githubusercontent.com/95431446/167586765-65643dc1-a1b1-4d74-a3b7-4c864336a6d4.png)

- <ins>**Clique droit "Nouveau groupe..."**<ins>

![image](https://user-images.githubusercontent.com/95431446/167586913-f3aeb085-12ca-42ef-94c2-10cd3e47fd57.png)

- <ins>**On rempli les champs avec les informations de notre excel**<ins>

![image](https://user-images.githubusercontent.com/95431446/167587224-8dc2b889-f6f0-4fcb-9ce6-9e5a0a82e117.png)

- <ins>**On clique ensuite sur "Ajouter..." pour mettre nos utilisateur concerner dans le groupe.**<ins>

![image](https://user-images.githubusercontent.com/95431446/167587872-bd88eadf-c798-4805-a09c-3946823f550b.png)

 _on utilise le point virgules pour séparer les utilisateurs ``` ; ```_

![image](https://user-images.githubusercontent.com/95431446/167588046-a50001f8-5e08-42b3-8ef4-b53f16c8238c.png)

- <ins>**Finaliser la manœuvre en cliquant sur Créer.**<ins>

- ### <ins>Comme le demande l'énoncer nous allons maintenant créer les exceptions et autres.<ins>

- <ins>**Nous commencerons par ajouter les membres du services informatique au groupe Administrateurs.**<ins>

![image](https://user-images.githubusercontent.com/95431446/167589423-f93918d7-d574-4530-a325-7d03f6a8c8c9.png)

- <ins>**Nous allons ensuite activé l'exigences de complexité pour les mots de passe et le changement obligatoire tout les 25 jours, nous utiliserons pour ce faire l'éditeur de stratégie de groupe locale en utilisant 'windows + R' nous tapons ensuite ``` gpedit.msc ```**<ins>

![image](https://user-images.githubusercontent.com/95431446/167590517-b0a8d876-26da-4a7c-9d60-5fa1834c6e60.png)

- <ins>**Il nous faut ensuite nous rendre dans l'onglet Configuration ordinateur > Paramètres Windows > Paramètres de sécurité >  stratégie de compte > Stratégie de mot de passe :**<ins> 

![image](https://user-images.githubusercontent.com/95431446/167593887-6ef0a489-dca4-4f88-aec5-e3ebb5f2536a.png)

- <ins>**Longueur minimal du mot de passe à 12 :**<ins> 

![image](https://user-images.githubusercontent.com/95431446/167594093-35ce3a1f-78f8-4bd6-a727-6eb9aee350f8.png)

- <ins>**Durée de vie maximale du mot de passe a 25 jours :**<ins> 

![image](https://user-images.githubusercontent.com/95431446/167594176-7a190cd6-6ed5-468b-b8ab-d76730007cea.png)

- <ins>**Activation de l'exigence de complexité :**<ins> 

![image](https://user-images.githubusercontent.com/95431446/167594529-6ef9a875-0d92-4a03-8148-4129d88d5eba.png)

 - <ins>**Nous allons également contraindre les heures d’ouverture de session de notre intérimaire a l'aide de l'invite de commande.**<ins>

> Nous utiliserons la commande ``` net user 'utilisateurs' /times:L-V,9:00-12:00 ```

![image](https://user-images.githubusercontent.com/95431446/167596304-30b805a9-d33c-4caa-a833-e82e9b4a50a1.png)

- <ins>**Pour finir nous allons créer le fichiers Procédures avec le règlement intérieur qui sera sur le bureau de tout les utilisateurs.**<ins>

- <ins>**Nous allons devoir nous rendre dans ``` C:\Users\Default\Desktop ```**<ins>
 
_Le dossier est caché il est possible de le faire apparaitre avec affichage voir ci dessous_

![image](https://user-images.githubusercontent.com/95431446/167607028-b1d59be8-36d6-4433-87a8-abbd90bd325a.png)
![image](https://user-images.githubusercontent.com/95431446/167607290-ab5ec096-267c-4afc-ad68-f3352604d613.png)
![image](https://user-images.githubusercontent.com/95431446/167607365-dd918a00-f5ad-40dc-857e-e42932c6817a.png)

- <ins>**On y ajoute alors le dossier Procédures avec le règlement intérieur.**<ins>

![image](https://user-images.githubusercontent.com/95431446/167607424-7a8f016b-cfe0-463d-b7af-53c36cdce78c.png)


## FIN
