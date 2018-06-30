#Events backboned microservices POC

##Preparación
Para poder correr la prueba en un solo host (local) usaremos contenedores **Docker**. Por ser una prueba de concepto limitaremos el número de brokers de Kafka a 2.

1. Descargar la configuracion de docker-compose necesaria para correr Kafka en Docker (Kafka + Zookeeper) desde https://wurstmeister.github.io/kafka-docker/
2. Modificar el archivo *docker-compose.yml* de acuerdo a lo que dice la documentación. Por ejempo la IP del HOST de docker fue: 172.22.0.1
Adicionalmente agregaremos otro broker para hacer más interesante la prueba
```bash
docker-compose up
docker-compose up --scale kafka=2```
3. Luego para probar crearemos un container que actuará como producer `start-kafka-shell.sh <DOCKER_HOST_IP> <ZK_HOST:ZK_PORT>`, según el ejemplo sería
```bash
start-kafka-shell.sh 172.22.0.1 172.22.0.1:2181
```
(recordemos que está todo referido al mismo host ya que estamos utilizando la ip de host para los containers docker)
desde este container se pueden correr los test que aparecen en el link, traducidos al ejemplo serían:
```bash

```
4. 

