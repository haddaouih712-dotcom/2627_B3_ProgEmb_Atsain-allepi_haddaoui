Les nouveaux documents seront pour le moment dans la partie wiki de notre github. On ajoutera ultérieurement les photos et screenshot sur github.










Rapport programmation embarquée


Questions 1 : Notez le hostname et le nom d'utilisateur choisis. Pourquoi est-il nécessaire de définir ces informations avant le premier démarrage d'une Raspberry Pi utilisée sans écran ?

Notre hostname est : C106-WA-MH
Notre identifiant est : Usermw.
MDP : 123@

Définir ces informations permet de configurer la carte SD. En configurant la carte SD, on donne un identifiant et un mot de passe pour s’identifier. Ce qui permet à ne pas laisser n’importe qui se connecter. D'ailleurs en configurant, on pourra connecter la Raspberry à un appareil via le même Wi-Fi que notre ordinateur. Ce qui permettra de connecter via SSH notre ordinateur et notre Raspberry.

Question 2 : Expliquez pourquoi TX est relié à RX et RX à TX. 

Lorsque qu'un appareil envoie un signal à un autre appareil, il doit être sûr de l’avoir bien reçue. Le second appareil va devoir envoyer un signal pour confirmer la reception du signal du premier appareil. TX relié à RX et RX à TX permet une bonne communication entre les émetteurs TX et récepteur RX. 

Question 3 : Expliquez le rôle de GND dans cette liaison. 

Le GND est la masse du circuit. Il ferme le circuit électrique. Il permet de conserver la stabilité et le bon fonctionnement du circuit électrique.

Question 4 : Que signifie le réglage 115200 8N1 ? 

Le réglage 115200 8N1 est appelé banderate. Il correspond à la vitesse de transmission bit par bit utilisé dans des protocoles tel que UART

Question 5 : Pourquoi ne faut-il pas connecter la broche 5 V de l'adaptateur aux GPIO de la Raspberry Pi ?
Il ne faut pas connecter la broche 5 V de l'adaptateur aux GPIO de la Raspberry Pi car cela risque d’endommager la Raspberry Pi , il ne peut pas supporter 5V. Il peut supporter au maximum 3,3 V.

Question 6 : Que se passe-t-il si le terminal série est configuré à une autre vitesse que la Raspberry Pi ?

Lorsqu'on envoi des instructions de la Raspberry PI au PCB la communication ne va pas se faire et les données peuvent être corrompus.

Question 7 : Dessinez un schéma de câblage représentant le shield utiliser. Comparez la connexion UART et la connexion SSH : quels équipements et quelles configurations sont nécessaires dans chaque cas ? Donnez un avantage et une limite de chaque méthode. Notez l'adresse IP obtenue. Avez vous accès à internet ? Où se trouve la clé privée ? Où se trouve la clé publique ? Pourquoi la clé privée ne doit-elle pas être copiée dans ~/.ssh/authorized_keys ? Quel est le rôle de authorized_keys ? Quelle différence faites-vous entre le mot de passe du compte Raspberry Pi et la phrase secrète de la clé privée ? Pourquoi faut-il tester une nouvelle connexion avant de désactiver l'authentification par mot de passe ? Quels droits doivent avoir les dossiers et fichiers .ssh pour limiter les risques ?

Ce qu’on a fait : 

On a suivi les étapes pour configurer notre carte sd on a choisi le bon modèle, le bon modèle d’exploitation et on a écrit sur la carte SD les instructions. On a ensuite choisi notre hostname ainsi que notre identifiant et notre mot de passe. Ensuite on a suivi les instructions en mettant les codes dans le fichier config.txt. On a ensuite utiliser un adaptateur UART - USB de 3,3 V pour connecter la Raspberry Pi Zero W au PC. 


On est désormais bloqué à la connexion login. 

