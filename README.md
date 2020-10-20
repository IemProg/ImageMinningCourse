# Lab 2 Work for Image Mining Course 

This repository contains our Pytorch Notebook experiments on the Cifar10 dataset as part of a Course on Image Mining 

We briefly describe our models and methods: 
### Simple CNN
SHORT DESCRIPTION  
Learning rates:  
Batch size:  
Epochs:  
Interpretation of loss plot:  
Accuracy on test: 66.71 %  
### Simple CNN with Dropout
SHORT DESCRIPTION  
Learning rates:  
Batch size:  
Epochs:  
Interpretation of loss plot:   
Accuracy on test:  
## Additional (pretrained) models:
### VGG16 
SHORT DESCRIPTION  
Learning rates:  
Batch size:  
Epochs:  
Interpretation of loss plot:   
Accuracy on test:  
### Resnet
We used a pretrained resnet model. 
Learning rates: 0.01 
Batch size: 64 
Epochs: 20   
Interpretation of loss plot: We can clearly see that we are overfitting on the train data, as the train loss is increasing up to 99.86 % while the test loss stays the same. We could use a model that relies more on    
Accuracy on test: 90.27 %
### VIG 
SHORT DESCRIPTION  
Learning rates:  
Batch size:  
Epochs:  
Interpretation of loss plot:   
Accuracy on test:  
## Additional Methods: 
### Transfer Learning 
For Resnet and VGG16 we use pretrained models, change the number of outputs for the last linear layer and freeze the previous layers, such that their weight stays unchanged. 
### Optimizers 
We tried out Yogi Optimizer but did not notice any substantial improvements in contrast to ADAM and SGD. 
https://papers.nips.cc/paper/8186-adaptive-methods-for-nonconvex-optimization.pdf
### Learning Rate Finder 
We experimented with the learning rate finder concept introduced in "Cyclical Learning Rates for Training Neural Networks" by Smith, 2015 retrieved from: https://arxiv.org/abs/1506.01186 
However this proved to be an unstable method to estimate the optimal learning rate. 
### Visualising Class Saliency 
Saliency maps are a way to visualize what a network is focusing on, when making a particular classification.
https://github.com/MisaOgura/flashtorch

