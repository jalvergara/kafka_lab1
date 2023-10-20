# Instrucciones para correr kafka con Docker - Lab 1

Running docker compose:

- docker-compose up
- docker ps

Open two new terminals and run the following command in each terminal: 
- docker exec -it kafka-broker-1 bash  

console1

- kafka-topics --bootstrap-server kafka-broker-1:9092 --create --topic lab1-topic
- kafka-console-producer --bootstrap-server kafka-broker-1:9092 --topic lab1-topic

enviar mensajes

console2

- kafka-console-consumer --bootstrap-server kafka-broker-1:9092 --topic lab1-topic --from-beginning

Important commands: 

List topics:

- kafka-topics  --bootstrap-server kafka-broker-1:9092 --list

get topic offset:

- kafka-run-class kafka.tools.GetOffsetShell --broker-list kafka-broker-1:9092 --topic lab1-topic