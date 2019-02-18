## MNIST Flask
![image](https://github.com/adi0111/Mnist/blob/master/ezgif-4-97402aa376b6.gif)
### Steps：
#### 1、run app.py
 1.Local run
 
 1⃣️install the requirements：
 
 sudo pip install -r requirements.txt
 
 2⃣️Run：
 
 python app.py
 

2. use Docker

1⃣️install the Docker，Docker Tutorial：https://docs.docker.com/install/overview/

2⃣️ use docker create image (change Image_name to the name you like)

docker build -t IMAGE_NAME .

3⃣️run the image

docker run -d -p 4000:5000 IMAGE_NAME


### 2、conncet to the Cassandra

1⃣️ run the Cassandra（jump：https://hub.docker.com/_/cassandra/



docker run --name some-cassandra -p 9042:9042 -d cassandra:latest

2⃣️conncet the Cassandra contanier you create above with the docker container and romove

docker run -it --link some-cassandra:cassandra --rm cassandra cqlsh cassandra



### 三、Check the data in the Cassandra Container  

use mnist_database

select * from mnist1


