# docker-rabbitmq
Environnement Docker pour découvrir RabbitMQ

# Installation
- Créer une VM : <code>docker-machine create -d virtualbox <i>machine_name</i></code>
- Ajouter le répertoire <code>app</code> dans les dossiers partagés de la VM
- Se connecter en SSH sur la machine : <code>docker-machine ssh <i>machine_name</i></code>
- Créer un fichier <code>sudo vi /var/lib/boot2docker/bootlocal.sh</code> qui contiendra les lignes suivantes :
<ul>
	<li>mkdir /home/docker/app/</li>
	<li>mount -t vboxsf app /home/docker/app</li>
</ul>
- Enregistrez puis redémarrez la VM
- Se connecter au conteneur PHP et lancer le composer :
<ul>
	<li><code>docker exec -ti <i>container_name</i> /bin/bash</code></li>
	<li><code>composer install</code></li>
</ul>
