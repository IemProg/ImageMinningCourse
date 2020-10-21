# Lab 2 Work for Image Mining Course 

This repository contains our Pytorch Notebook experiments on the Cifar10 dataset as part of a Course on Image Mining 

We briefly describe our models and methods: 
### Simple CNN
SHORT DESCRIPTION: 
A convolutionnal neural network CNN with two convolutionnal layers and one hidden linear layer. Between each convolutionnal layer, we used a leaky relu activation and a max-pool layer, as well as a leaky relu activation for the hidden linear layer. Again we used the negative log likelihood loss and the log softmax activation for the final layer as it is standard for classification with C classes.

    Learning rates: 0.001
    Batch size:  32.
    Epochs: 10, 20.
    Total params: 62,006.  
    Accuracy on test: 66.71 %  

### Simple CNN with Dropout
SHORT DESCRIPTION: Testing the effect of dropout to a CNN model 

    Learning rates: 0.01
    Batch size:  32
    Epochs: 10
    Total params: 4,746,186
    Accuracy on test:  68.41 % (for dropout:0.1)
    Different values for dropout: [0.2, 0.3, 0.5, 0.9]

## Additional (pretrained) models:
### VGG16 
SHORT DESCRIPTION : Using pretrained model VGG-16 on CIFAR-10 by freezing the first layers and retraining the last one.

    Learning rates: 0.01  
    Batch size:  32
    Epochs:  10
    Total params: 138,357,544  
    Accuracy on test:  86.06 %
    
### Resnet18
We used a pretrained resnet model.   

    Learning rates: 0.01   
    Batch size: 64   
    Epochs: 20     
    Interpretation of loss plot: We can clearly see that we are overfitting on the train data, as the train loss is increasing up to 99.86 % while the test loss stays the same. We could use a model that relies more on regularization.    
    Accuracy on test: 90.27 %  
### ViT (Vision Transfomer) 
SHORT DESCRIPTION: A novel method of using Transfomers for classification tasks.

    Learning rates: 3e-5.
    Batch size:  64.
    epochs: 20.
    dropout = 0.1.
    emb_dropout = 0.1 
    Accuracy on test:  54.67

## Additional Methods: 

### Transfer Learning 
For Resnet and VGG16 we use pretrained models, change the number of outputs for the last linear layer and freeze the previous layers, such that their weight stays unchanged. 

### Optimizers 
We tried out Yogi Optimizer but did not notice any substantial improvements in contrast to ADAM and SGD.  
Paper retrieved from: 
https://papers.nips.cc/paper/8186-adaptive-methods-for-nonconvex-optimization.pdf

### Learning Rate Finder 
We experimented with the learning rate finder concept introduced in "Cyclical Learning Rates for Training Neural Networks" by Smith, 2015 Retrieved from:   https://arxiv.org/abs/1506.01186   
However this proved to be an unstable method to estimate the optimal learning rate. 

### Visualising Class Saliency 
Saliency maps are a way to visualize what a network is focusing on, when making a particular classification. In order to check, the behavior behind the prediction process of the trained models.

Library: https://github.com/MisaOgura/flashtorch
