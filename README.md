#                                           Neural_Network_Charity_Analysis

OVERVIEW:

In this project we will be helping by create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup. We let them know in advances the successful rate since there is money on the line. We will be creating model in where we will be manipulating data, creating test , and analyze the model that is created.


Results:
	
	In the beginning I had to drop EIN and NAME columns.

Had to find the unique value for example. 

APPLICATION_TYPE            17
AFFILIATION                  6
CLASSIFICATION              71
USE_CASE                     5
ORGANIZATION                 4
STATUS                       2
INCOME_AMT                   9
SPECIAL_CONSIDERATIONS       2
ASK_AMT                   8747
IS_SUCCESSFUL                2
dtype: int64


The dependent variable would be ISSUCESSFUL.

On the optimaizer the results for the first 

# Define the model - deep neural net, i.e., the number of input features and hidden nodes for each layer.
number_input_features = len(X_train[0])
hidden_layer1 = 80
hidden_layer2 = 30

nn = tf.keras.models.Sequential()

# First hidden layer
nn.add(
tf.keras.layers.Dense(units=hidden_layer1, input_dim=number_input_features, activation="relu")
)
# Second hidden layer
nn.add(
tf.keras.layers.Dense(units=hidden_layer2, activation="relu")
)
# Output layer
nn.add(
tf.keras.layers.Dense(units=1, activation="sigmoid")
)
# Check the structure of the model
nn.summary()

the rsults of this are 
Model: "sequential"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
dense (Dense)                (None, 80)                3840      
_________________________________________________________________
dense_1 (Dense)              (None, 30)                2430      
_________________________________________________________________
dense_2 (Dense)              (None, 1)                 31        
=================================================================
Total params: 6,301
Trainable params: 6,301
Non-trainable params: 0

We han see thst the total params are 6301 and the triable params 6301 and the non-trainable params 0

268/268 - 0s - loss: 0.9533 - accuracy: 0.6925
Loss: 0.9532940983772278, Accuracy: 0.6924781203269958
 We can see that this model didn’t reach 75% but it only reach 69%.

# Define the model - deep neural net, i.e., the number of input features and hidden nodes for each layer.
number_input_features = len(X_train[0])
hidden_layer1 = 100
hidden_layer2 = 50
hidden_layer3 = 20
nn = tf.keras.models.Sequential()
# First hidden layer
nn.add(
tf.keras.layers.Dense(units=hidden_layer1, input_dim=number_input_features, activation="relu")
)
# Second hidden layer
nn.add(
tf.keras.layers.Dense(units=hidden_layer2, activation="relu")
)
# Output layer
nn.add(
tf.keras.layers.Dense(units=1, activation="sigmoid")
)
# Check the structure of the model
nn.summary()

Model: "sequential_1"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
dense_3 (Dense)              (None, 100)               4800      
_________________________________________________________________
dense_4 (Dense)              (None, 50)                5050      
_________________________________________________________________
dense_5 (Dense)              (None, 1)                 51        
=================================================================
Total params: 9,901
Trainable params: 9,901
Non-trainable params: 0
_________________________________________________________________
In [30]:
1

And in this one the total params =9901 and the triable 9901 and nontrainable 0

This one didn’t reach 75% either it reached 47%

268/268 - 0s - loss: 0.9391 - accuracy: 0.4731
Loss: 0.9390515685081482, Accuracy: 0.4731195271015167


The third one 

# Define the model - deep neural net, i.e., the number of input features and hidden nodes for each layer.
number_input_features = len(X_train[0])
hidden_layer1 = 100
hidden_layer2 = 50
hidden_layer3 = 20
nn = tf.keras.models.Sequential()
# First hidden layer
nn.add(
tf.keras.layers.Dense(units=hidden_layer1, input_dim=number_input_features, activation="relu")
)

# Second hidden layer
nn.add(
tf.keras.layers.Dense(units=hidden_layer2, activation="relu")
)
# Output layer
nn.add(
tf.keras.layers.Dense(units=1, activation="sigmoid")
)
# Check the structure of the model
nn.summary() 


Model: "sequential_2"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
dense_6 (Dense)              (None, 100)               4800      
_________________________________________________________________
dense_7 (Dense)              (None, 50)                5050      
_________________________________________________________________
dense_8 (Dense)              (None, 1)                 51        
=================================================================
Total params: 9,901
Trainable params: 9,901
Non-trainable params: 0
________________________


And in this one the total params =9901 and the triable 9901 and nontrainable 0.

This one didn’t reach 75% either it only reach 65%.

268/268 - 0s - loss: 0.6522 - accuracy: 0.6578
Loss: 0.652248203754425, Accuracy: 0.6578425765037537


Summary:

So the first challenge the model percentage was 44% but with more messing round we where able to get more higher percentage some close to 75% but not 75%. The first and third attempt from the optimizer gave higher percentage  one with 65% and the thirsd one with 65%.
![image](https://user-images.githubusercontent.com/115046550/225139906-6ec9f113-51d1-4f13-9ea3-3f06beb5f73e.png)

