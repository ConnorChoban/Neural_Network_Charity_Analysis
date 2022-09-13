# Neural_Network_Charity_Analysis

## Overview

The purpose of this analysis is to use machine learning concepts to create a neural network to examine whether applicants will successfully meet the criteria to receive funding from a charity organization. In this analysis, we'll create a complex neural network and make modifications in an attempt to correctly classify the data at least 75% of the time.

## Results

### Data Preprocessing

- In our code, we tried to classify applicants by whether their applications were successful or not. Therefore, we used the column "IS_SUCCESSFUL" as our target variable. 
- The features for our model consist of all additional columns besides the "IS_SUCCESSFUL" column and the EIN and NAME which were dropped. 
- In our code we dropped EIN and NAME as they serve for identification purposes and don't have an impact on the data. 

### Compiling, Training, and Evaluating the Model

- I initially set up the neural network with 80 neurons in the first hidden layer, and 20 in the second, as generally the neurons in the second layer should be a fraction of the number in the first layer. As I made modifications to the neural network in an attempt to increase the accuracy score, I changed the number of neurons and added a third layer. Finally, I used a "relu" activation function for the hidden layers, since we needed a fucntion that could help predict (regression) whether an applicant would be sucessful. I then used a "sigmoid" function for the output layer, as it's ideal for binary classification.
- I was not able to acheive the target model performance (75%), but I did managed to acheive an accuracy score as high as approximately 74.3%.
- I tried altering the number of neurons in the hidden layers, adding a third hidden layer, and changing the epochs, but they all had little impact on the final accuracy score.

#### Initial Neural Network Setup

<img width="877" alt="Screen Shot 2022-07-29 at 6 28 37 AM" src="https://user-images.githubusercontent.com/99847786/181740592-e4414fb9-e0a8-41ab-bc6a-735a37241a51.png">
<img width="878" alt="Screen Shot 2022-07-29 at 6 29 07 AM" src="https://user-images.githubusercontent.com/99847786/181740602-8dd9cf61-f2a2-4fc9-bd69-b5abd507088d.png">


#### Changing Number of Neurons in the Hidden Layer

(100 in the first layer, 30 in the second)

<img width="938" alt="Screen Shot 2022-07-29 at 6 31 30 AM" src="https://user-images.githubusercontent.com/99847786/181741077-0b5388c0-dc57-418f-84b1-06175583de01.png">

<img width="710" alt="Screen Shot 2022-07-29 at 6 31 53 AM" src="https://user-images.githubusercontent.com/99847786/181741086-2934101b-c874-4b3d-b7ff-085ef42756b3.png">

(120 in the first layer, 50 in the second)

<img width="880" alt="Screen Shot 2022-07-29 at 6 32 42 AM" src="https://user-images.githubusercontent.com/99847786/181741245-ddbdaec7-eb48-4542-a59f-645afaef6267.png">

<img width="651" alt="Screen Shot 2022-07-29 at 6 33 42 AM" src="https://user-images.githubusercontent.com/99847786/181741376-9f9e98c9-f7d7-49d1-9cc3-7adb05b0cf3c.png">

#### Adding a Third Hidden Layer

<img width="873" alt="Screen Shot 2022-07-29 at 6 34 07 AM" src="https://user-images.githubusercontent.com/99847786/181741463-41bc36c7-debe-49c9-bc3e-b5df0f3b216d.png">

<img width="619" alt="Screen Shot 2022-07-29 at 6 34 40 AM" src="https://user-images.githubusercontent.com/99847786/181741560-a89cb806-a7f3-4eef-9e1d-30734b5f3957.png">


####  Adding Epochs

(50) Epochs

<img width="592" alt="Screen Shot 2022-07-29 at 6 35 34 AM" src="https://user-images.githubusercontent.com/99847786/181741931-e1dc406b-3648-4051-847d-ac353268c779.png">
<img width="603" alt="Screen Shot 2022-07-29 at 6 35 49 AM" src="https://user-images.githubusercontent.com/99847786/181741968-697e2064-1d94-4aa1-bda3-92f42f46b7ac.png">


(200) Epochs

<img width="602" alt="Screen Shot 2022-07-29 at 6 35 55 AM" src="https://user-images.githubusercontent.com/99847786/181741993-6d7952df-03e4-46b1-934f-0c8eb218c411.png">
<img width="609" alt="Screen Shot 2022-07-29 at 6 36 30 AM" src="https://user-images.githubusercontent.com/99847786/181742029-1c66e062-f262-4fd8-a329-f0559f486552.png">


## Summary

The model was partially successful in that it managed to correctly classify loan applicants 74% of the time, just under the goal of an accuracy score of 75%. However, in this case, a Random Forest model may be a better option due to the fact that it can easily handle outliers without skewing our dataset or model; a key concern with neural networks is that they're prone to overfitting. By using a Random Forest Classifier, we can avoid this issue while also saving time and our computer's resources - another concern that might come up when working with colleagues across multiple teams. 
