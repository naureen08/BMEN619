HW02

1a) The accuracy achieved using losing logistic regression:
batch = 100
iteration = 3000
accuracy= 82.7

1b) derivative of the sigmoid function:
𝜎(𝑥)⋅(1−𝜎(𝑥))

1c) one reason the loss does not decrease is that the model is too simple for the data and is not learning any more.

2a)loss function:
    def sigmoid(self, s):
        return 1 / (1 + torch.exp(-s))
    
    def sigmoidPrime(self, s):
        # derivative of sigmoid
        return s * (1 - s)

2b) Increase batch size to improve final training loss

2c) When testing errors stops decreasing

2d) Chain rule


3a) MNIST with NN ReLU activation function: 92.5% accuracy

3b) Modified with Adam optimizer: 84.53% accuracy
Optimze with SGD, momentum=0.9 : 97.1% accuracy  

3c) SGD and momentum model, batch size 50: 96.8% accuracy
                            batch size 1000: 97.7% accuracy

    Adam Optimizer model, batch size 1000: 92.8% accuracy
                          batch size 50: 61.63% accuracy 
    
    A larger batch size increases accuracy but takes much longer to train. The smaller the batch size, the greater the randomness/noise. On the other hand, assuming an appropriate batch size is chosen, they train much more quickly than full batch learners. 

    A batch size of 1 means we choose to adjust the gradient after every single forward and backwards pass. This is known as online learning.