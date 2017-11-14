# Data Science Interview Questions
My collection of data science interview questions

# Table of Contents
1. Computer Science
2. [Algorithm](#algorithm)
3. [Math](#math)
4. Linear Algebra
5. Probability
6. [Statistics](#statistics)
7. [Machine Learning](#machine-learning)
8. [Deep Learning](#deep-learning)
9. [Healthcare](#healthcare)

<br><br>
## Computer Science

#### 1\. Process and thread

<br><br>
## Algorithm

#### 1\. Hashing table and hashing function
Hashing table is a mapping between keys and values.

<br><br>
## Math

### 1\. Derivative

### 2\. Integral

### 3\. Convex function

<br><br>
## Linear Algebra

#### 1. Rank

#### 2. Linear independent

#### 3. Distance and norms

<br><br>
## Statistics

#### 1. Likelihood function
Likelihood function is a function of parameters given the observed data. That is, we consider that the observed data are fixed but the paramters can vary. We hope to find a set of parameter values that maximize the likelihood function, which indicate that under the observed data, the model with such parameter values is the most probable model. In other words, we find a set of parameter values to maximize the likelihood function based on the observed data and hope this model is a good approximation to the true model that generates the observed data.

#### 2. Bayesian vs frequentist statistics


#### 3. Fisher information

<br><br>
## Machine Learning

#### 1. KL divergence

<br><br>
## Deep Learning

#### 1. Kernel size, stride, padding, channel, feature map in CNN


#### 2. Deconvolution (Fractionally strided convolution, Transposed convolution)
Note that deconvolution is not an appropriate name for this kind of operation (check the CS231n course for explanation). 

Here are some key points based on my understanding:

First, one key point is that the convolution operation can be calculated by matrix multiplication. The input feature map can be writen as a vector, the kernel can be written as a sparse matrix and the convolution is just the product of these two matrices.   

Second, transposed convolution and fractionally strided convolution are two different operations (the learned kernels will be different in these two operations), but they are quivalent in terms of the output. 

In short, fractionally strided convolution is just to pad each pixel first and then do convolution.  Transposed convolution is just to transpose the convolution matrix and apply it to the original output (the output in the convolution). 

[This Github repo](https://github.com/vdumoulin/conv_arithmetic) has visualization for all kinds of convolutions. I highly recommend readers to check it out. 


* [A guide to convolution arithmetic for deep learning](https://arxiv.org/pdf/1603.07285v1.pdf)

#### 3. Dilated convolution (Atrous convolution)
Dilated convolution is similar to the regular convolution. The only difference is that it skips some pixels when doing convolution. Imaging a 3x3 regular convolution, the dilated convolution will use the pixels at rows 1,3,5 and columns 1,3,4 and thus the pixels in the middel are skipped. The dilation rate controls how many pixels to skip. In the previous example, the dilation rate is 2. By using dilated convolution, the receptive fild increases from 3x3 to 5x5 while the number of parameters are the same, which is an advantage over the large kernel. 



<br><br>
## Healthcare

#### 1\. Administrative data
Administrative data is the data from government or insurance company for administrative purpose, for example evaluating the quality of health care. Compared to EHR data from hospitals, administrative data has patient demongraphic information as well as dignosis information, but may not have detailed treatment or lab result information.   
