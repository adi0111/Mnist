## MNIST Flask
![image](https://github.com/adi0111/Mnist/blob/master/ezgif-4-97402aa376b6.gif)
## SoftMax
![image](http://wiki.jikexueyuan.com/project/tensorflow-zh/images/softmax-regression-scalargraph.png)
![image](http://wiki.jikexueyuan.com/project/tensorflow-zh/images/softmax-regression-vectorequation.png)
### Introduction: 
In this project, it use the keras to build the model for the Mnist and use the softmax function to predict the data from the input image. And in the next steps, it connect to the Cassandra database to keep the data and later we can check the data in the Cassandra database. 
### Steps：
#### 1、run app.py
 1.Local run
 
  a. install the requirements：
 
 sudo pip install -r requirements.txt
 
  b.Run：
 
 python app.py
 

2. Use Docker

 a. install the Docker，Docker Tutorial：https://docs.docker.com/install/overview/

 b. use docker create image (change Image_name to the name you like)

       docker build -t IMAGE_NAME .

 c. run the image

       docker run -d -p 4000:5000 IMAGE_NAME


### 2、conncet to the Cassandra

 a. run the Cassandra（jump：https://hub.docker.com/_/cassandra/



       docker run --name some-cassandra -p 9042:9042 -d cassandra:latest

 b. conncet the Cassandra contanier you create above with the docker container and romove

       docker run -it --link some-cassandra:cassandra --rm cassandra cqlsh cassandra



### 3、Check the data in the Cassandra Container  

      use mnist_database

      select * from mnist1


