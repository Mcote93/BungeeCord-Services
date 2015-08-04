#BungeeCord-Services
Fichier pour lancer Bungeecord en tant que services Compatible Centos 6.x &amp; 7.x

##Installations
Pour commencer nous allons créer un utilisateur pour améliorer votre sécurité ;

useradd bungeecord 

Nous allons maintenant entré dans le dossier de ce compte et télécharger BungeeCord.jar ;

cd /home/bungeecord && wget http://ci.md-5.net/job/BungeeCord/lastSuccessfulBuild/artifact/bootstrap/target/BungeeCord.jar

Intallation du script qui rend BungeeCord comme un services de votre serveur ;

cd /etc/init.d && wget https://raw.githubusercontent.com/Mcote93/BungeeCord-Services/master/bungeecord && chmod +x bungeecord

Mettre en place le cron Job ; 
 
vi /etc/crontab

ajouter cette commande a la fin de votre fichier ;
 
*/10 * * * * /etc/init.d/bungeecord monitor
* */12 * * * /etc/init.d/bungeecord backup
0 6 * * * /etc/init.d/bungeecord mail-log >/dev/null 2>&1


et pour finir les commandes disponible son ;

service bungeecord {start|stop|status|monitor|restart}

##les Variables importantes du fichier
SERVICE = Nom de votre fichier .jar
USERNAME =  Nom d'utilisateur de votre serveur Minecraft/BungeeCord
MCPATH = Directory ou est votre fichier .jar
 
