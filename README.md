1. Question 1
    1. Just by running the code (in google colab), we can see the output of the code in wandb.
    2. Link for the .ipynb file: https://colab.research.google.com/drive/1CpE6keY5Tq9tkk8Sygkd01azFXKzbYrn?usp=sharing 

2. Question 2
    1. Here we created a class called Neural_network with parameters x_train,y_train,input_dimension,hidden_layers_size,hidden_layers,output_dim,batch_size,epochs,activation_func,learning_rate, decay_rate,beta,beta1,beta2,optimizer,weight_init
    2. Here when we create an object to this class then we need to pass the training data (x_train,y_train), input dimension size, hidden layer size, number of hidden layers, output dimension, batch size, number of epochs, which activation function we want to use, learning rate, decay rate, beta, beat1, beta2 for adam optimizer, which optimizer we want to use and which which weight initializer we want to use.
    3. In this python file we implemented gradient descent optimizer; activation functions of sigmoid, tanh and relu, we can use any one of this activation functions; and random and xavier weight initializers.
    4. Here we can use any batch size, any learning rate, any epochs while creating the object of this class.
    5. Link for the .ipynb file: https://colab.research.google.com/drive/1wNL2i7XOjhhkv43t9uUplBJFiqTalM6M?usp=sharing

3. Question 3
    1. Here we implement optimizers like sgd(stocastic gradient descent), momentum, Nestrov Accelerated Gradient, RMS Prop, ADAM and NADAM.
    2. If we want to use RMS Prop as an optimizer then while creating the object for this class we will send optimizer="rmsprop" then RMS Prop optimizer will be used for computing. 
    3. Similarly 
      * If we want to use SGD optimizer then we use optimizer="sgd"
      * If we want to use Momentum optimizer then we use optimizer="momentum"
      * If we want to use NAG optimizer then we use optimizer="nestrov"
      * If we want to use Adam optimizer then we use optimizer="adam"
      * If we want to use NAdam optimizer then we use optimizer="nadam"
    4. Link for the .ipynb file: https://colab.research.google.com/drive/1x4xMaHQRW-tOxzyaa-p5BaMc2CV4oWNs?usp=sharing
    
 4. Question 4
    1. First, we have splitted the train data in 9:1 ratio. 90% of the data is for training purpose and 10% of the data is for cross validation.
    2. Then, we have set the sweep function of wandb by setting up different parameters in sweep_config.
    3. By runnig the below code  we can start seeing the ouput within our wandb project.
    ```
    wandb.agent(sweep_id,train)
    ```
    5. Link for the .ipynb file: https://colab.research.google.com/drive/1NIEBtntraCGSMvUIWTFTA062pf1_JdJ5?usp=sharing 
 
 5. Question 7
    1. We have used test data for plotting the confusion matrix.
    2. We have used the model which was giving highest validation accuracy for plotting the confusion matrix.
    3. The model is as follows:
      - optimizer : nadam
	  - activation : tanh
	  - batch size : 64
	  - hidden layers : 2 
	  - learning rate : 0.002
	  - weight decay : 0.1
    5. By running the below code we can see plot the confusion matrix in our wandb project:
    ```
       wandb.init(project='fashion_mnist',entity='adi00510',reinit=True)
       nn=Neural_network(x_train,y_train,784,64,2,10,64,7,'tanh',0.002,0.1,0.9,0.9,0.99,'nadam','xavier')
       nn.calculate_accuracy(x_test,y_test,True)
    ```
    6. Link for .ipynb file: https://colab.research.google.com/drive/1h391HHmOpxQdw3kSvSBxkv3-pZNEeRx7?usp=sharing  
6. Question 8
    1. In this file we have implemented squared error loss as we are doing cross entropy loss in the previous questions.
    2. Now we compared this squared error loss with cross entropy loss by running it on 4 configurations.
    3. In most of the cases squared error loss will not perfom better as compared to cross entropy loss in terms of cross validation accuracy, but in some cases cross validation accuracy will be very close.
    4. Link for .ipynb file: https://colab.research.google.com/drive/1rX7S5-qy1EROXNz8EdGx3BAp-59dqcum?usp=sharing

7. Question 10
    1. In this file we loaded Mnist data from keras dataset and we used 3 best configruations by observing the previous configruations which we have used for fashion_mnist dataset.
    2. By running this configruations we got test accuracy as following 96.98%, 95.32%, 92.79% respectively for these 3 best configruations
    3. Link for .ipynb file:
