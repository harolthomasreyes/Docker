1. command: `docker-compose up`
1. open a new terminal Productor
1. command: `docker exec -it kafka-broker-1 bash`
1. open a new terminal Consumer
1. command: `docker exec -it kafka-broker-1 bash`
1. command Terminal Productor: `kafka-topics --bootstrap-server kafka-broker-1:9092 --create --topic myprimerkafka`
1. command Terminal Productor: `kafka-console-producer --bootstrap-server kafka-broker-1:9092 --topic myprimerkafka`
1. open a new terminal Consumer
1. command Terminal Consumer: `kafka-console-consumer --bootstrap-server kafka-broker-1:9092 --topic myprimerkafka  --from-beginning`
