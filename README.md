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
           1. If we want to use SGD optimizer then we use optimizer="sgd"
           2. If we want to use Momentum optimizer then we use optimizer="momentum"
           3. If we want to use NAG optimizer then we use optimizer="nestrov"
           4. If we want to use Adam optimizer then we use optimizer="adam"
           5. If we want to use NAdam optimizer then we use optimizer="nadam"
    4. Link for the .ipynb file:
    
