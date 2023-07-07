# CIFAR-10-image-classification
Problem: <br />
CIFAR-10 dataset  <br />
AlexNet has 5 Conv and 3 FC layers <br />
Play with a medium deep network with atleast 2 conv and 2 FC layers. <br />
Metrics: training time and classification performance <br />
Compare ReLU vs tanh vs sigmoid <br />
With and without momentum, adaptive learning rates <br />
Finally: what would be your recommended architecture.. <br />
<br />
For this problem, as we had to use Pytorch extensively, I went through the videos posted by
our TA and understood the necessities required. AlexNet has 5 Conv and 3 FC layers but as
posted in the problem, initially we tried experimenting with 2 convolutional and 2 fully
connected and then finalized with 2 convolutional and 3 fully connected layers. <br />
The architecture is as follows: <br />
● 2x2 Convolutional layer with stride = 2, and number of filters = 128. <br />
● 2x2 max pool layer with stride = 2 <br />
● Batch normalization <br />
● 2x2 Convolutional layer with stride = 2, and number of filters = 256. <br />
● 2x2 max pool layer with stride = 1 <br />
● Batch normalization <br />
● Linear Layer (output size = 1000) <br />
● Linear Layer (output size = 120) <br />
● Linear Layer (output size = 10)
● Softmax Classification
Convolutional layers have tanh activation while fully connected layers have ReLu activation.
For 40 epochs, this gave 67.54% accuracy.
Training time was around one hour (using GPU on kaggle) for 40 epochs, so for taking
graphs and observations later, therefore for later observations we used 15 epochs.
Both training and validation plots have been included in this report
