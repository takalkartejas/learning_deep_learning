# Learning deeo learning

Video link - https://youtube.com/playlist?list=PLeo1K3hjS3uu7CxAacxVndI4bE_o3BDtO&si=EjXoDVGxZ7Fq_tos

---

## Theory
<details> <summary>
Tutorial3 - What is neuron
   
</summary>

   1. Take example of the health insurnace problem again which is a binary classification problem using sigmoid function. 
   ![image](https://github.com/takalkartejas/learning_machine_learning/assets/67382565/155cf8e9-af9a-4824-b364-de4fa93e9028)
   
   ![image](https://github.com/takalkartejas/learning_machine_learning/assets/67382565/0eabf266-e168-4de3-a905-abd84bc84386)

   ![image](https://github.com/takalkartejas/learning_machine_learning/assets/67382565/696eea3a-3129-4ac9-bcd1-e9c5bf1e2397)

   2. Now we form a single neuron which takes age as the output and gives the probablily of buying an insurance as an output
   ![image](https://github.com/takalkartejas/learning_machine_learning/assets/67382565/4151c4af-f8e3-4d35-b52a-077bb72ec12a)

   3. We can have multiple input variables and each of them can have diffrent impact on output which we can manage by assigning weights to each input'
   ![image](https://github.com/takalkartejas/learning_machine_learning/assets/67382565/3d9afd70-2804-4b7c-84ab-de243c6f446c)

   4. Final representaiton of neuron
   ![image](https://github.com/takalkartejas/learning_machine_learning/assets/67382565/628db4b6-0fc8-4e6e-85b9-e46379ebe458)
   5. Here two step mathemathical calculation is performed 1st is weighted sum and second is sigmoid which is an activation funtion

</details>

<details> <summary>
Tutorial7 - What is neuron
   
</summary>

1. We can add a hidden layer in the previous example as below
    
   ![image](https://github.com/takalkartejas/learning_machine_learning/assets/67382565/a0632309-ae51-4018-9d6a-902fcf984960)

2. Now we can make the network dense but the connections that were missing previously will have near to zero weights.
   ![image](https://github.com/takalkartejas/learning_machine_learning/assets/67382565/d7495800-a3b9-4846-9ddb-cc157c83ce9b)

3. Now we want to classify the handwritten digits from 0 to 9
   ![image](https://github.com/takalkartejas/learning_machine_learning/assets/67382565/c1bbf584-1d8c-4638-a4cc-f39c34ea423c)
4. The outputs will be between 0 to 1 they are somewhat like similarity scores of the image to the digits they represent
5. In this example we convert the image from 2d array to 1d array and supply to the neural network, and the neural network does not have any hidden layers. We will first solve without the hidden layer and then add it and check how the accuracy improves 
</details>

<details> <summary>
Tutorial8 - activation function
   
</summary>
![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/760c9e34-cb69-4440-9b9d-1ae494b04741)
1. sigmoid-
   ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/fb2ce986-6d7e-4884-94be-db8b0b572be5)

   use sigmoid in output layer as it convets output to 0 to 1
2. tanh- 
3. ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/3be5c289-5d1a-448e-84b3-4cf672c54bb3)
   use for hidden layers as it outputs from -1 to 1, centering data around 0
4.Sigmoid and tanh function has really low derivative for higher values which slows down learning process, **vanishing gradient problem**
5. Relu- 
    value < 0: output = 0, value>0, output=value
    ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/cefc1bdb-b2b5-4a13-a7c7-b978a8b44a2e)
    it is light weight and good for computation speed, used by default for deep learning problems

    vanishing gradient problem in -ve range
6. leaky relu-
   ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/191c875d-0452-4adb-9376-c9bc3c6f8673)

   to solve the vanishing gradient problem in relu
</details>


  
goal- 8, 11, 12, 


