# Configuration du stockage et des ressources Windows 10

## <ins>Configuration des ressources.<ins>

- ### **Création d'un dossier "Commerciaux" uniquement accessible au groupe commercial**

1. <ins>**On ce rend dans E:**<ins>

![image](https://user-images.githubusercontent.com/95431446/167820215-202789b2-3308-435e-b2f2-3ba36b2f6231.png)

2. <ins>**On ouvre les propriétés du dossier.**<ins>

![image](https://user-images.githubusercontent.com/95431446/167820488-524b47b0-c498-49bd-a559-4a0ed3aeef7a.png)

3. <ins>**On ce rend dans sécurité puis on clique sur avancé.**<ins>

![image](https://user-images.githubusercontent.com/95431446/167820707-ca90bb3a-5ef1-43da-b32c-92b86cc85622.png)

4. <ins>**On désactive l'héritage**<ins>

![image](https://user-images.githubusercontent.com/95431446/167821228-0f248b0f-d01e-4deb-961c-40eea404636e.png)

5. <ins>**On supprime toutes les autorisations héritées de cet objet.**<ins>

![image](https://user-images.githubusercontent.com/95431446/167821687-b13320c7-fa7a-4fe9-a559-356e17aed0f1.png)

6. <ins>**On applique les changements**<ins>

![image](https://user-images.githubusercontent.com/95431446/167821893-ded39c20-5009-4095-929f-8a7d4e763473.png)

7. <ins>**On clique maintenant sur ajouter**<ins>

![image](https://user-images.githubusercontent.com/95431446/167822317-ac5fff61-1f55-4bf7-af34-b2ba37ec7008.png)

8. <ins>**On clique sur Sélectionnez un principal on ajoute ensuite le groupe Commerciaux et Systèmes**<ins>

![image](https://user-images.githubusercontent.com/95431446/167823003-7ec601fc-6de7-437c-9cc2-4c789e0be433.png)

9. <ins>**On clique maintenant sur "Appliquer ces autorisations..." _voir ci-dessous_**<ins>

![image](https://user-images.githubusercontent.com/95431446/167823423-e0cbbe18-3c57-49a3-90ad-8dd45eb7676d.png)

10.<ins>**On clique maintenant sur Appliquer puis OK**<ins>

![image](https://user-images.githubusercontent.com/95431446/167825389-5f62ca32-cc99-4c6a-adf8-1259f8b3b870.png)

- Voila le dossier commerciaux n'est accessible que par leur groupe.

- ## <ins>**Création d'un dossier Support_Info accessible uniquement au groupe informatique**<ins>

1. <ins>**Voir étapes 1. a 8. de "Création d'un dossier "Commerciaux" uniquement accessible au groupe commercial" mais en remplaçant le groupe commerciaux par le groupe informatique.**<ins>

2. <ins>**On coche cette fois "Modification" _et_ "Appliquer ces autorisations...".**<ins>

![image](https://user-images.githubusercontent.com/95431446/167828125-906e1e1b-09fb-4360-a40e-4d59ee8312fe.png)

3. <ins>** On applique et OK pour quitter**<ins>

![image](https://user-images.githubusercontent.com/95431446/167828540-3d525bdd-28c7-40e3-a875-b839fe60fff3.png)

- ## <ins>**Création du partage réseau de "Support_Info"**<ins>

1. <ins>**On commence par ce rendre dans les propriétés du fichier puis dans l'onglet partage suivi de Partage avancé...**<in>

![image](https://user-images.githubusercontent.com/95431446/167830010-6cab2ae1-dcc8-4073-b7f7-f07420752664.png)

2. <ins>** On coche Partager ce dossier, on ajoute ensuite le signe ```$``` a la fin pour le rendre invisible et enfin ce rendre dans Autorisations**<ins>

![image](https://user-images.githubusercontent.com/95431446/167830607-f5269d90-15c5-44eb-a28f-e6abf830e403.png)

3. <ins>**On supprime "Tout le monde".**<ins>

![image](https://user-images.githubusercontent.com/95431446/167831031-425bcc12-606c-4106-9c81-408b5f11b325.png)

4. <ins>**On ajoute ensuite Utilisateurs authentifiés.**<ins>

![image](https://user-images.githubusercontent.com/95431446/167831200-d85b6a6c-7e65-4ca6-9cde-2626be69fe36.png)

5. <ins>**On coche dans "Autoriser" "Modifier" puis appliquer suivi de OK.**<ins>

![image](https://user-images.githubusercontent.com/95431446/167831525-3fc56f3c-4d2e-4196-8dc2-e85e73303502.png)


- ## <ins>Test du partage avec le binome<ins>

1. <ins>**Il nous faut pour cela nous rendre dans ce PC dans l'explorateur de fichiers puis dans les onglet cliquer sur ordinateur**<ins>

![image](https://user-images.githubusercontent.com/95431446/167836397-9d8fa429-3814-4478-ab29-c867a17664a6.png)

2. <ins>**On clique ensuite sur connecter un lecteur réseau**<ins>

![image](https://user-images.githubusercontent.com/95431446/167836508-12a83b09-0d32-47cb-9d28-fe29e8257137.png)

3. <ins>**On lui ajoute la lettre de lecteur U: on renseigne ensuite le chemin pour accéder au partage**<ins>

![image](https://user-images.githubusercontent.com/95431446/167837738-7bde3620-2313-4d8d-aef8-aaaaedc91e79.png)

4. <ins>**On clique pour finir sur Terminer une fois le partage ouvert nous créons le dossier et le fichier word Test**<in>

![image](https://user-images.githubusercontent.com/95431446/167838175-0c2b4772-341f-48bd-95e6-3a1b9193d0a6.png)
_Les fichiers sont bien partager entre les deux machines_

## FIN
