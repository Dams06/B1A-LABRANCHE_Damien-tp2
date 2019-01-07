# TP2 RESEAUX
TP 2 - Exploration du réseau d'un point de vue client

Partie 1- Solo : 
•	Pour voir les infos des cartes réseaux de notre PC il faut ouvrir un terminal et rentrer ceci : « ipconfig /all » et ensuite chercher les informations que vous voulez. Pour le TP on veut le nom, l’adresse MAC et l’adresse IP de l'interface Wifi et même chose pour l'interface Ethernet.

Interface Wifi  - nom : Carte réseaux sans fil Wi-Fi
		               - adresse MAC : D0-57-7B-0D-12-9F
		               - adresse IP : 10.33.0.67
			           -adresse Réseaux : 10.33.0.0
			           -adresse Broadcast : 10.33.0.255
Interface Ethernet  -nom : Carte Ethernet Ethernet
			               -adresse MAC : 70-4D-7B-3C-3F-D6
			               -adresse IP : il n’y en a pas.
			               -adresse Réseaux : il n’y en a pas.
			               -adresse Broadcast : il n’y en a pas.

Pour afficher la Gateway il faudra écrire dans le terminal la même chose « ipconfig /all » aller à Carte réseaux sans fil Wifi et regarder Passerelle par default et l’adresse IP est 10.33.3.253. 
Pour trouver l’adresse IP, MAC et la Gateway en utilisant l’interface graphique il faut faire un clic droit sur dans votre barre des taches sur l’icones internet et sélectionner ouvrir les paramètres réseaux et internet puis cliquer sur Wifi ou Ethernet suivant la connection que vous avez et cliquer sur Propriétés du matériel.

Une gateway est l’adresse d’un équipement qui fait la liaison entre deux réseaux. Donc la gateway du réseau IngéSup

Modification des informations
Comme vu plus haut on sait que notre adresse sur le réseau IngéSup est 10.33.2.10/22 et que le masque est 255.255.252.0.

On fait donc un ET logique binaire :

11.33.2.10 + 255.255.252.0 
  = 0000101.00100001.00000010.00001010
  + 11111111.11111111.11111100.00000000
  = 00001010.00100001.00000000.00000000  
  = 11.33.0.1/22
Nous avons plus qu'a ajouter 1 à la partie hôtes de cette IP, donc la première adresse disponible sur le réseau IngéSup est 10.33.0.1/22

Changer d'adresse IP avec nmap
Avec l'outil Nmap on exécute la commande :

 nmap -sn -PE 192.168.1.0/24
192.168.1.0/24 est l'adresse réseau sur lequel je suis connecté actuellement.

dsl il va manquer la deuxieme partie en duo mais j'ai pas pu la faire. J'èspère que tu me croiras.