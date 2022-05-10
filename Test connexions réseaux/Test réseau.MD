# <ins>Teste de la connectivité réseau<ins>

- ## Pour tester la connectivité réseau entre nos machine nous allons procédé a un ping

- <ins>**Depuis la machine windows ouvrir l'invite de commande et exécuter la commande : ping <'ip de debian'>**<ins>

![image](https://user-images.githubusercontent.com/95431446/167403162-9bdd9c20-8979-4a2b-9b45-4620a6c99e40.png)

![image](https://user-images.githubusercontent.com/95431446/167403200-31967d9c-1d0c-4264-a1af-e40dbb732f03.png)

  _Le ping fonctionne de windows vers la machine debian_

- <ins>**Pour ce qui est du coté debian le ping ne fonctionne apriori pas il faut pour cela activé la règle autorisant le protocole ICMP dans le pare-feu windows**<ins> 

![image](https://user-images.githubusercontent.com/95431446/167403630-cd65362b-2a30-4193-88c9-35fefad0efad.png)

  _Le ping sans l'activation de la règles ICMP_

- <ins>**On ce rend dans le Pare-Feu Windows Defender avec fonctions avancées de sécurité.**<ins>

![image](https://user-images.githubusercontent.com/95431446/167404405-528a7d67-7677-4f6f-9865-e648c05e4416.png)

- <ins>**On ce rend sur la règles analyse de l'ordinateur viruel (Demande d'écho - trafic entrant ICMPv4)**<ins>

![image](https://user-images.githubusercontent.com/95431446/167407226-2b1e2d3a-7fde-4a73-af60-bfcd4458c638.png)

- <ins>**Dans le menu action on clique sur Activer la règle.**<ins>

![image](https://user-images.githubusercontent.com/95431446/167408307-04f8c29e-266e-432e-a973-397018f3ec8a.png)

- <ins>**Il est maintenant possible de ping la machine windows depuis debian avec la commande : ping -c3 <'ip de windows'>**<ins>

>  (-c3 nous permet de ne faire que trois requête) 

![image](https://user-images.githubusercontent.com/95431446/167408707-5e625feb-7b34-476a-8a33-08101dcdb8b4.png)

  ## FIN
