Homework 5

Question 1a) Try a different optimizer and determine accuracy
Model with SGD:
accuracy without normalization: 0.866
                    training time: 4377.2 examples/sec on cpu
accuracy with normalization: 0.867
                    training time: 4355.8 examples/sec on cpu

Model with Adam optimizer: 
accuracy without normalization: 0.806
                    training time: 4176.4 examples/sec on cpu
accuracy with normalization: 0.872
                    training time: 4335.4 examples/sec on cpu

Highest accuracy was model with Adam optimizer and batch norm.


Question 1b) Change batch size and determine accuracy
Model with SGD without normalization:
Batch size 50(low): 0.889
        training time: 3561.9 examples/sec on cpu
Bactch size 500 (high) 0.88
        training time: 4344 examples/sec on cpu

Questions 1c) Replace batch normalization with dropoout
Model with SGD: test acc 0.840
        training time: 4107 examples/sec on cpu

Model with Adam: test acc 0.833
        training time: 4114.2 examples/sec on cpu

This model had very similiar results throughout, regardless of Adam or SGD. Every time I ran the model I got a higher test accuracy.

Question 2a) When validation loss > training loss you can call it overfitting. An optimal fit is the goal of the learning algorithm. The loss of the model will almost always be lower on the training dataset than the validation dataset. This means that we should expect some gap between the train and validation loss learning curves. an optimal fit one where the plot of training loss and validation loss decreases to a point of stability.

Question 2b) There is very little gap between the training loss and validation loss when using drop out. Testing loss will not be greater than training loss during the case of underfitting.

Question 2c)Vary the drop out parameters
Dropout p=0.9: Huge gap between training loss and validation loss. Training loss is very high. Training loss > Validation loss
Dropout p=0.2: Almost no gap between training loss and validation loss (but validation loss is slightly greater). Validation loss is not smooth.

Question 2d) The gap between training and validation loss is smaller (although validation is still slightly greater) possibly because it uses new data acquired from dropout.

Question 2e) During training, some number of layer outputs are randomly ignored or “dropped out.” This has the effect of making the layer look-like and be treated-like a layer with a different number of nodes and connectivity to the prior layer. Dropout increases training time.

