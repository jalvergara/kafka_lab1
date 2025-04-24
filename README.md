# Instrucciones para correr kafka con Docker - Lab 1

## Running docker compose:

- docker-compose up
- docker ps

Open two new terminals and run the following command in each terminal: 
- docker exec -it kafka-test bash  

console1

- kafka-topics --bootstrap-server kafka-test:9092 --create --topic test_clase_kafka
- kafka-console-producer --bootstrap-server kafka-test:9092 --topic test_clase_kafka

enviar mensajes

console2

- kafka-console-consumer --bootstrap-server kafka-test:9092 --topic test_clase_kafka --from-beginning

### Important commands: 

List topics:

- kafka-topics  --bootstrap-server kafka-test:9092 --list

get topic offset when connecting as the consumer:

- kafka-console-consumer --bootstrap-server kafka-test:9092 --topic test_clase_kafka --from-beginning --property print.offset=true
