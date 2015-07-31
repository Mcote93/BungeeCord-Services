#BungeeCord-Services
Fichier pour lancer Bungeecord en tant que services Compatible Centos 6.x &amp; 7.x

##Installations
Pour commencer nous allons créer un utilisateur pour améliorer votre sécurité

useradd BungeeCord

Nous allons maintenant entré dans le dossier de ce compte

cd /home/BungeeCord && git clone git://github.com/Mcote93/BungeeCord-Services.git bungeecord


Mettre en place le cron Job; vi /etc/crontab

ajouter  a vos cron => 10 * * * * service bungeecord monitor

Plus d'informations a venir...


##les Variables importantes
 SERVICE = Nom de votre fichier .jar
 USERNAME =  Nom d'utilisateur de votre serveur Minecraft/BungeeCord
 MCPATH = Directory ou est votre fichier .jar
 