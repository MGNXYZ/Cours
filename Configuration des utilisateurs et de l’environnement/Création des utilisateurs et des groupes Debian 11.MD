# <ins>Création des utilisateurs et des groupes<ins>

## <ins>Création des utilisateurs et des groupes Debian 11<ins>

- <ins>**On commence par créer les groupes**.<ins>

> On utilise la commande ``` addgroup 'nom du groupe' ```

![image](https://user-images.githubusercontent.com/95431446/167666834-b912e52b-9cd7-40e9-9675-53d44dcd390e.png)
 
- <ins>**On ajoute ensuite nos utilisateurs**.<ins>

> On utilise la commande ``` useradd -c "Nom complet" 'nom du usr' -m -g 'groupe' --shell /bin/bash -p "mot de passe" ```

![image](https://user-images.githubusercontent.com/95431446/167635828-29db3a43-e376-48a6-851e-3ab661ca0cb7.png)
_On ajoute l'utilisateur ddixon_

- <ins>**On ajoute le prestataire en ksh pour ce faire il nous faut installer ksh**<ins>

> On utilise la commande ``` sudo apt install ksh ```

![image](https://user-images.githubusercontent.com/95431446/167663157-a1a90c63-cfdf-4755-970d-64854f169329.png)
_ksh est deja installer sur ma machine_

> On créer ensuite notre utilisateur prestataire avec ``` useradd -c "Nom complet" 'nom du usr' -m -g 'groupe' --shell /bin/ksh -p "mot de passe" ```

![image](https://user-images.githubusercontent.com/95431446/167663795-d62005cd-219f-4a3c-a7c2-e24ab69cf637.png)

- <ins>**On force le changement de mot de passe de notre prestataire.**<ins>

> Avec la commande ```passwd -e 'nom d'utilisateur' ```

![image](https://user-images.githubusercontent.com/95431446/167666332-0a1415eb-03ce-4b5e-9f20-5b4506686d19.png)

## FIN
