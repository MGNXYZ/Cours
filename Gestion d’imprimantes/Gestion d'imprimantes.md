# Gestion d'imprimantes

- ## <ins>**Installation d'une imprimante HP LaserJet M9050 MFP sur le réseau**<ins>

## A. <ins>**On va commencer par extraire les pilotes en utilisant "WinZip".**<ins> 

- <ins>On double clique simplement puis Unzip.<ins>

![image](https://user-images.githubusercontent.com/95431446/167888939-b05a07ac-a78d-46d2-b8ab-e9f1e2f94b38.png)

![image](https://user-images.githubusercontent.com/95431446/167889305-0f700718-e0b4-4098-b48a-a1fad51c984c.png)

- <ins>On clique sur "Mode Traditionnel" puis suivant<ins>.

![image](https://user-images.githubusercontent.com/95431446/167889484-37a003dc-a46f-4d7c-9e20-a0a462849448.png)

![image](https://user-images.githubusercontent.com/95431446/167889730-1d88b2dc-85c5-4bb7-83c4-acc028e6af2c.png)

- <ins>On ajoute ensuite l'ip de notre imprimante ici "87.68.168.76"<ins>.

![image](https://user-images.githubusercontent.com/95431446/167890706-0f5cf6dc-6bdd-4f82-bea5-daded386c14d.png)

- <ins>On patiente<ins>.
 
![image](https://user-images.githubusercontent.com/95431446/167890883-3de41384-3c24-4b85-8a94-427734ed7f01.png)

- <ins>On choisi ensuite le drivers "HP Hewlett Packard Jet Direct"<ins>.

![image](https://user-images.githubusercontent.com/95431446/167891257-dc656e28-f883-4f49-86f3-e7b38d578631.png)

- <ins>On sélectionne ensuite un driver puis suivant<ins>.

![image](https://user-images.githubusercontent.com/95431446/167892245-777e8ca4-8370-46b1-b69f-a3fb9c0b59a8.png)

- <ins>On renommera notre imprimante "HP LaserJet M9050 MFP" puis suivant a nouveau<ins>.

![image](https://user-images.githubusercontent.com/95431446/167892458-24ddd619-2b0d-42ee-9730-23eb5d15603f.png)

- <ins>On clique enfin sur terminer<ins>.

![image](https://user-images.githubusercontent.com/95431446/167894648-6c015948-d85c-413c-8b11-b4a9332d581f.png)

- <ins>On va maintenant vérifier que notre imprimante est bien installer<ins>.

![image](https://user-images.githubusercontent.com/95431446/167894997-6cefa2dd-e793-4bc9-8e19-f30d25851d2e.png)

![image](https://user-images.githubusercontent.com/95431446/167895127-ebb154f1-29c6-4898-b2c3-4ef116074e10.png)

## B. <ins>**On va maintenant changer les permissions d'utilisation de notre nouvel imprimante**<ins>

- <ins>Toujours dans gestion de l'impression on va faire clique droit sur notre imprimante propriétés et sécurité<ins>.

![image](https://user-images.githubusercontent.com/95431446/167896837-a431c3bb-739a-43ba-9ecf-301038ffdd60.png)

- <ins>On va d'abord supprimer les utilisateurs non concernés par nos restrictions puis ajouter les groupes avec la permission correspondante<ins>.

![image](https://user-images.githubusercontent.com/95431446/167898171-f1acb8a9-f7b8-434d-ba86-695823d332f4.png)

- <ins>On indique ensuite les droits pour chaque groupes<ins>.

> Le groupe comptabilité aura le droit d'impression et de gestion des documents.

![image](https://user-images.githubusercontent.com/95431446/167908369-f6480629-6f9d-4141-a0aa-b581bf47841b.png)

> Le groupe informatique aura tout les droits.

![image](https://user-images.githubusercontent.com/95431446/167908455-83dfa0a9-bad1-407d-b53f-dc88dcbd3703.png)

- <ins>On applique les changement et on clique sur OK<ins>.

![image](https://user-images.githubusercontent.com/95431446/167908586-7af3c6da-6301-49fb-bc12-2e5102290876.png)

- <ins>On va maintenant mettre l'imprimante en réseau pour ce faire toujours dans propriétés l'onglet "Partage".<ins>

> Cocher partager cette imprimante

![image](https://user-images.githubusercontent.com/95431446/167910683-27c8e2ab-5da9-416d-a9bd-a7d82158c3ba.png)

- <ins>Nous vérifions a l'aide d'un autre poste que l'imprimante est bien disponible<ins>

> On ce rend dans l'onglet "Réseau" de l'explorateur de fichier puis on clique sur l'ordinateur distant.

> Puis une fois sur l'imprimante clique droit connecter.

![image](https://user-images.githubusercontent.com/95431446/167911807-1ff80ea8-469f-492a-8f5f-df0870107056.png)
 
- <ins>On va maintenant sur notre ordinateur distant la définir comme imprimante par défaut.<ins>

> Nous nous rendons dans le "Panneau de configuration" > Matériels et audio > Périphérique et imprimantes
> Clique droit définir comme imprimante par défaut.

![image](https://user-images.githubusercontent.com/95431446/167912329-41657abc-f592-420e-b359-181cdd9552be.png)

## C. <ins>**Création d'un pool d'imprimantes**<ins>

