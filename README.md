# Learning deeo learning

Video link - https://youtube.com/playlist?list=PLeo1K3hjS3uu7CxAacxVndI4bE_o3BDtO&si=EjXoDVGxZ7Fq_tos

---

## Theory
<details> <summary>
Tutorial3 - What is neuron
   
</summary>

   1. Take example of the health insurnace problem again which is a binary classification problem using sigmoid function. 

   The neuron is created using the logistic regression function
   ![image](https://github.com/takalkartejas/learning_machine_learning/assets/67382565/155cf8e9-af9a-4824-b364-de4fa93e9028)
   
   ![image](https://github.com/takalkartejas/learning_machine_learning/assets/67382565/0eabf266-e168-4de3-a905-abd84bc84386)

   ![image](https://github.com/takalkartejas/learning_machine_learning/assets/67382565/696eea3a-3129-4ac9-bcd1-e9c5bf1e2397)

   2. Now we form a single neuron which takes age as the output and gives the probablily of buying an insurance as an output
   ![image](https://github.com/takalkartejas/learning_machine_learning/assets/67382565/4151c4af-f8e3-4d35-b52a-077bb72ec12a)

   3. We can have multiple input variables and each of them can have diffrent impact on output which we can manage by assigning weights to each input'
   ![image](https://github.com/takalkartejas/learning_machine_learning/assets/67382565/3d9afd70-2804-4b7c-84ab-de243c6f446c)

   4. Final representaiton of neuron
   ![image](https://github.com/takalkartejas/learning_machine_learning/assets/67382565/628db4b6-0fc8-4e6e-85b9-e46379ebe458)

   **b stands for bias**

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

<details> <summary>
Tutorial11 - loss or cost functions
  
</summary>

 1. Examples-
      1. sparse_categorical_crossentropy
      2.  binary_crossentropy
      3.  categorical_crossentropy
      4.  mean_absolute_error
      5.  mean_squared_error
   2. The neural network model is trained on basis of minimizing these errors
   
   ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/12db67fd-dc81-4f24-803b-d9e6fd002851)
   
   3. In the above example the initial weights are taken as 1 and 1, and the bias is 0
   4. Now we make a forward pass, that is pass all the values we have through the neuron and then check the mean absolute error(one fo the cost funtions) by comparing with the ground truth value like shown below
   
   ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/fb76a27d-5a75-4a45-9c26-e57022a6dd36)

   5. If we go thorugh all the sample once, it is called one epoch
   6. Mean absolute error(MAE)-
      ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/8a8b5257-675a-42ad-9bc2-cd69b92f9d2d)
   7. Mean squared error-
       ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/126f4a2a-34a9-47ca-889b-4f9943d978fa)
   8. Log loss or binary cross entropy
      ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/1a844879-67bb-48dc-8d4c-17d9cb7fb88f)
      
      log loss is used for logistic regression
</details>

<details> <summary>
Tutorial12 - gradient descent for neural network

</summary>

![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/7d86ad81-8429-4d83-9d37-db7e56140a46)

1. The shown in the above image we take a forward pass with randomly selected weights and biases and then calculate error for each sample.
2. We use the errors to calulate the log loss(log loss is the cost function most suitable for logistic regression)
   ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/2270b961-dfd2-4c51-b88d-8edfabe5948a)
3. Now we get a loss = 4.3, we need to back propgate this loss
4. In below equations the partial derivative symbols represent the derivative of cost w.r.t weight and biases. 
 ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/ebd5b7a9-f83c-4730-bee9-b4824c7c948e)

![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/06985f4c-1189-4761-9cd5-a311fb3ffc51)

The derivative shown in above image is calculated by taking derivative of loss function directly

5. Now we get the new weights as shown below
   
   ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/ef212b19-4960-434c-82ee-65a2944fe64b)

6. We repeat this process to go to the minima of the cost function as shown below
7. ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/54c77fdb-8d8b-441c-bdc0-95391fc47486)

</details>

<details> <summary>
Tutorial14 - gradient descent classification

</summary>

1. batch grdient descent-
   1. We go through all training samples and calculate cumulative error
   2. then we back propogate and adjust the weights
   3. But if we have lot of samples, it is really slow to calculate all derivatives etc. foer each epoch
2. Stochstic gradient descent-
   1. Adjust weights after every sample
3. Mini batch gradient descent
   1. Instead of every sample adjust the weight after a batch of sample
   2. ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/1bfda461-066b-42ed-ae09-ffbc30f05259)

</details>

<details> <summary>
Tutorial15 - chain rule

</summary>

1. We saw in gradient descent video the derivatives of log loss function wrt weights and biases were taken but the calculation was not explained
2. In the following image we take the derivtive of loss wrt e, then e wrt y and then y wrt w1, so we get the derivate of loss function wrt w1 by multiplying them
3. ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/52cbb23b-b2f1-4fe5-8603-30329e84ece1)
4. ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/2b267885-daa6-4985-94f8-bfe56bb67b7e)
</details>

<details> <summary>
Tutorial16 - tensorboard

</summary>

1. Refer code cell - [73]
2. It can tell you how much your accouracy is going up or loss is going down per epoch
3. use the command - tensorboard --logdir tutorial15/logs
4. The graph is in scalars
</details>

<details> <summary>
Tutorial18- customer churn prediction using ann

</summary>

1. we want to know why customers are leaving, what the factors.
2. refer code
</details>

<details> <summary>
Tutorial19- accuracy stuff

</summary>

1. Precision
   
   ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/40bd2d8c-3b18-4264-b11a-717a99a2f70c)
2. Recall
   ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/f724514b-7501-4f33-8667-a3d4e6d88487)

3.  F1 score harmonic mean of precision and recall
   ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/253f1fc1-aeaf-486e-9dba-f280d4660568)

   https://www.labelf.ai/blog/what-is-accuracy-precision-recall-and-f1-score

   refer tutorial 18 end ending for example
</details>

<details> <summary>
Tutorial20- dropout regularization

</summary>

![image](https://miro.medium.com/v2/resize:fit:1125/1*_7OPgojau8hkiPUiHoGK_w.png)

1. We need to avoid underfitting or overfitting
2. ![image](https://miro.medium.com/v2/resize:fit:1036/0*EY8R7nS10y5kQzOx)
3. we avoid over fitting by using drop out regularization
4. some neurons are droped from hidden layers for one epoch and another for another, so that the NN does not create a bias towards some neurons.
5. refer code

</details>



<details> <summary>
Tutorial23- CNN

</summary>

1. These variations are present in hand written digits and can be handled by changing them to 1d array and using ANN
   
   ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/32f5b265-ca02-4b5d-9799-9de6f005e172)

   ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/4d705058-5e15-44d2-afa0-9fe9ddc31964)

2. Disadvantages of using ANN for image classifications
   1. too much computation required, as image size is huge plus it is rgb
   2. Sensitive to location of object like face of a lion can be anywhere in the image and should be recognized
3. Feature extraction-
   ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/808ce04b-7214-4640-9391-863e6ef65ae2)

   ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/538576f0-c37d-4a83-a87c-258892bbe61b)
4. Lets take some 3x3 filters and apply a convolution operation on the image
   ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/ea615c41-aec2-4811-89c1-f56ae965a2e2)

5. The first filter shown in the above image to detect the 9s head is shown in the below image
6. It multiplies with each invidual values and adds them to give an output

![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/bd844168-9ed1-4026-895a-4418be720d38)

7. If the output is close to one we know that the feature is present at that spot and we have succefully detected it as shown below
![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/fa6e77fe-2eef-4713-892c-b5c684320da9)
![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/4ef28983-fd77-4ef8-a803-ba496a6ff034)   

8. we get the feature map as output as shown in above image

9. This same feature gets activated at different spots for different numbers as shown below

10. ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/cfc55080-716f-4ac1-9f7d-ac05809e59eb) 
    
![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/ccb38f7e-3527-444b-b4c9-d31c7543cb96)
![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/f055fb6b-dfb6-449a-baae-33c1ead638e1)
11. We combine the feature map to locate where the koalas head is making it simple
![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/51d8c943-501d-4ec8-8d03-97a2419d2ad2)
12. Then we flatten and feed to ANN
13. We use relu after the feature extraction and before ANN to make -ve values zero
14. ![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/7bac8b34-3a47-4922-b985-35e7d4467273)

15. But the size of feature maps was still equal to orignal image, to reduce them we use pooling
    1.  max pooling- 
![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/ba05efa8-d36d-46fe-a872-9f18ff354a06)
   2. average pooling-
![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/38cb8779-3a44-46ae-a35f-ca905d692449)

![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/3888725d-5c5f-4025-8ae2-f5a682c7a080)

16. final result- 

![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/ce827217-b51b-429f-914e-49b38c256b2d)

![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/eecd39cc-3e4b-4a0e-a732-c22563ad8aab)

![image](https://github.com/takalkartejas/learning_deep_learning/assets/67382565/8de7bca4-263c-4181-85a5-333ac2465895)
</details>



<details> <summary>
Tutorial24- image classifcation using CNN

</summary>

1. we import cifar data set which consists of variety of objects
2. check code

</details>

<details> <summary>

goal-  21, 24, 25, 26, 27, 28, 30, 31, 32, 33, 34, 35, 36