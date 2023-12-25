# asterisk_data

ARCHIVOS DE CONFIGURACION Y SONIDOS DE ASTERISK

# nasterisk:1.0.0

Esta es una imagen docker preparada con la instalacion de Asterisk 18 en ubuntu 22.0 LTS.

# Descarga la imagen en tu pc:
                                                                                                         
<pre><code class="language-console">$ docker pull nsmdeveloper/nasterisk:1.0.0</code></pre>


# Como usar esta imagen

<pre><code class="language-console">$ docker run -itd --name=PBX -p 192.168.0.8:5062:5060/tcp -p 192.168.0.8:5062:5060/udp -p 192.168.0.8:5063:5061/tcp -p 192.168.0.8:5063:5061/udp -p 192.168.0.8:9088:8088/tcp -p 192.168.0.8:9088:8088/udp -p 192.168.0.8:8089:8089/tcp -p 192.168.0.8:8089:8089/udp -p 192.168.0.8:10000-10010:10000-10010/udp -v /home/nsmdeveloper/Documents/learning/docker/asterisk:/etc/asterisk  -v /home/nsmdeveloper/Documents/learning/docker/vol_asterisk_sounds:/var/lib/asterisk/sounds nsmdeveloper/nasterisk:1.0.0
</code></pre>

# Debes cambiar estos datos con los correspondientes  en tu computador / sistema operativo / ip:

* 192.168.0.8:5062 => Por la ip  local de tu pc (el puerto debe ser el mismo 5062).

* /home/nsmdeveloper/Documents/learning/docker/asterisk => por el dictorio que crees en tu pc para los archivos de configuracion de  asterisk.

* /home/nsmdeveloper/Documents/learning/docker/vol_asterisk_sounds => por el dictorio que crees en tu pc para los archivos  de sonidos de asterisk.

# Conectarse a la consola bash del contenedor asterisk:

<pre><code class="language-console">$ docker exec -it PBX /usr/sbin/asterisk</code></pre>

# Iniciar el sevidor asterisk:

<pre><code class="language-console">$ service asterisk start</code></pre>

# Acceder a la consola asterisk:

<pre><code class="language-console">$ docker exec -it PBX /usr/sbin/asterisk -r</code></pre>

# Url imagen asterisk:

<a href="https://hub.docker.com/r/nsmdeveloper/nasterisk" target="_blank">https://hub.docker.com/r/nsmdeveloper/nasterisk</a>




