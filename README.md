## MNIST Project
![image](https://cdn-images-1.medium.com/max/1600/1*XdCMCaHPt-pqtEibUfAnNw.png)
## SoftMax
![image](http://wiki.jikexueyuan.com/project/tensorflow-zh/images/softmax-regression-scalargraph.png)
![image](http://wiki.jikexueyuan.com/project/tensorflow-zh/images/softmax-regression-vectorequation.png)
## More details can be accessed in the project report
### Introduction: 
In this project, it use the keras to build the model for the Mnist and use the softmax function to train the model, so it can predict output from the user input handwrite image. And in the next steps, it connects to the Cassandra database to keep the data and later we can check the data in the Cassandra database. 
### Steps：
#### 1、run app.py
1.Local run
 
   a. Install the requirements：
 
       sudo pip install -r requirements.txt
 
   b.Run：
 
       python app.py
 
2. Use Docker

 a. Install the Docker，Docker Tutorial：https://docs.docker.com/install/overview/

 b. Use docker create image (change Image_name to the name you like)

       docker build -t IMAGE_NAME .

 c. Run the image

       docker run -d -p 4000:5000 IMAGE_NAME


### 2、conncet to the Cassandra

 a. Run the Cassandra, Cassandra Tutorial ：https://hub.docker.com/_/cassandra/



       docker run --name some-cassandra -p 9042:9042 -d cassandra:latest

 b. Conncet the Cassandra contanier you create above with the docker container and romove

       docker run -it --link some-cassandra:cassandra --rm cassandra cqlsh cassandra



### 3、Check the data in the Cassandra Container  

      use mnist_database

      select * from mnist1


