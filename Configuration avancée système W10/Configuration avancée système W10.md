# <ins>**Configuration avancée du systsème windows 10**<ins>
  
- ## A. <ins>**Mise en place du bureau a distance**<ins>
  
- <ins>**On va commencer par ce rendre dans le panneau de configuration**<ins>
  
> Panneau de configuration > système et sécuriter > autoriser l'accés à distance
  
![image](https://user-images.githubusercontent.com/95431446/168151711-bbc9d189-8b01-4388-809d-9653aa17dce4.png)

![image](https://user-images.githubusercontent.com/95431446/168151865-096cae84-8ebb-4353-9c20-5c1173e95407.png)

-<ins>**On va utilisé powershell en mode _administrateur_ pour ajouter le groupe informatique au groupe "Bureau a distance"**<ins>
  
> On utilise une commande ```net localgroup "Utilisateurs du Bureau à distance" Informatique /add```
  
![image](https://user-images.githubusercontent.com/95431446/168153685-4bd4cb64-741f-40fc-ad31-f541a1bc8300.png)

- <ins>**Pour vérifier tout ca on ce rend dans la console de la "Gestion de l'ordinateur"**<ins>
  
![image](https://user-images.githubusercontent.com/95431446/168154066-6eca8ef1-642c-49c0-9b72-cc7f88cbb7a6.png)

![image](https://user-images.githubusercontent.com/95431446/168154123-5d98514e-cc5c-4d28-9cda-d5b5f936807c.png)

- <ins>**On va maintenant vérifier quel port utilise le RDP en s'y connectant avec remmina dans notre machine debian**<ins>
  
> On commence par installer remina avec la commande ```apt install remmina```.
  
![image](https://user-images.githubusercontent.com/95431446/168162637-88c4b631-1c72-4bf0-8c86-2f89cacdba10.png)

> Taper ensuite remmina dans la barre de recherche de debian.

![image](https://user-images.githubusercontent.com/95431446/168163146-ba7cc444-bb99-4b17-bf3f-d88c1315f56c.png)

> On séléctionne RDP et on entre l'ip de notre machine distante ```192.168.1.58```
  
![image](https://user-images.githubusercontent.com/95431446/168163296-a152c84c-08de-4122-81b5-1ab6a567c05f.png)

> Appuyer simplement sur la touche entré.
  
![image](https://user-images.githubusercontent.com/95431446/168163430-1599026e-e55a-47ca-9bce-538c0ced0d9a.png)

> Entre ici vos imformation de compte windows  

![image](https://user-images.githubusercontent.com/95431446/168163511-3494ae6e-018b-4ebb-b786-36a3ed4a6839.png)

> Nous voila connecté.
  
> Un simple ip a sur notre machine debian nous indique que notre ip est 192.168.1.47
  
![image](https://user-images.githubusercontent.com/95431446/168164099-f69983e7-d141-4ce0-82af-70bd0f55dde7.png)

> Un simple ip a sur notre machine debian nous indique que notre ip est 192.168.1.47

-<ins>**Depuis remina nous lancon l'invite de commande.**<ins>
  
> On tape la commande ```netstat``` -on dans le cmd et on constate que notre machine est bien connecté à notre ip debian.

![image](https://user-images.githubusercontent.com/95431446/168164670-1083fe50-2621-44d6-adaa-2d218b6bc404.png)

> On sais que le port utilisé par RDP est le 3389

> Il est également possible de voir le port avec ```Regedit```
>HKEY_LOCAL_MACHINE > SYSTEM > CurrentControlSet > Control > Terminal Server > WinStation > RDP-TCP.
> On cherche ensuite la ligne PortNumber
> Le port ce situe entre paranthése
  
![image](https://user-images.githubusercontent.com/95431446/168165455-5c8395c5-304e-452c-85ae-b68e775015d2.png)


## B. <ins>**
