# Instrucciones para correr kafka con Docker - Lab 1

## Running docker compose:

- docker-compose up
- docker ps

Open two new terminals and run the following command in each terminal: 
- docker exec -it kafka-test bash  

console1

- kafka-topics --bootstrap-server kafka-test:9092 --create --topic kafka_lab2
- kafka-console-producer --bootstrap-server kafka-test:9092 --topic lab1-topic2

enviar mensajes

console2

- kafka-console-consumer --bootstrap-server kafka-test:9092 --topic kafka_lab2 --from-beginning

### Important commands: 

List topics:

- kafka-topics  --bootstrap-server kafka-test:9092 --list

get topic offset:

- kafka-run-class kafka.tools.GetOffsetShell --broker-list kafka-test:9092 --topic lab1-topic2