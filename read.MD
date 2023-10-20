#Instrucciones para correr kafka con Docker - Lab 1

docker-compose up
docker ps
docker exec -it kafka-broker-1 bash  # x2  Two different terminals

console1
kafka-topics --bootstrap-server kafka-broker-1:9092 --create --topic lab1-topic
kafka-console-producer --bootstrap-server kafka-broker-1:9092 --topic lab1-topic

enviar mensajes

console2
kafka-console-consumer --bootstrap-server kafka-broker-1:9092 --topic lab1-topic --from-beginning
