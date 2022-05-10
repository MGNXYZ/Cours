# Création d’utilisateurs et de groupes

## <ins>Préparation de la création des comptes avec Excel en suivant les recommandation de l'ANSI<ins> 

- ### <ins>Création d'un classeur contenant les noms et prénoms de nos utilisateurs<ins>.

![image](https://user-images.githubusercontent.com/95431446/167416076-292261f5-c944-4c0f-a403-2ef6e6c885e1.png)
_classeur avec les noms et prénoms de nos utilisateurs_

- <ins>**Nous allons commencer par créer leur login avec la première lettre de leur prénom suivi de leur nom de famille, pour ce faire nous allons utilisé la formule suivante :**<ins>

> Créer des noms définie depuis la colonne "Formules" puis taper la commande : 
``` =MINUSCULE(GAUCHE(Prénom))&MINUSCULE(Nom) ```

![image](https://user-images.githubusercontent.com/95431446/167423269-dd8e5041-d1b0-4967-83e6-4fae06fa5e4b.png)

- <ins>**Nous enchainons sur la création des mails**<ins> 

> Nous utiliserons la formule : ``` =MINUSCULE(GAUCHE(Prénom))&MINUSCULE(Nom)&"@gmail.com" ```

![image](https://user-images.githubusercontent.com/95431446/167423697-324879db-7c53-42d5-ac05-dcf6e215b725.png)

- <ins>**Pour finir la création de mots de passe en suivant les recommandation de l'ANSI contenant 12 caractères de types différents.**<ins> 

> Je commence par généré un mot de passe complexe en ligne puis j'applique la formule : 
``` =MAJUSCULE(GAUCHE(Prénom))&MAJUSCULE(GAUCHE(Nom))&"J;h49hL-p5" ```

![image](https://user-images.githubusercontent.com/95431446/167425447-bab90f6c-6488-488e-9cb7-4b49794ec105.png)

- <ins>**J'applique ensuite la description a l'aide d'un menu déroulant créer au préalable.**<ins>

![image](https://user-images.githubusercontent.com/95431446/167430144-3dcdbcbb-0dcf-4bee-bc81-b6b5b40fd59b.png)

  ## FIN
