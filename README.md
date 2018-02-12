# Data Science Interview Questions
My collection of data science interview questions

# Table of Contents
1. [Computer Science](#computer-science)
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

#### 1\. Process and thread (lock)


<br><br>
## Algorithm

#### 1\. Hashing table and collision
Hashing table is a mapping between keys and values.

#### 2\. Common sorting algorithms and complexity 


<br><br>
## Math

### 1\. Derivative

### 2\. Integral

### 3\. Convex function

<br><br>
## Linear Algebra

#### 1\. Rank

#### 2\. Linear independent

#### 3\. Distance and norms

#### 4\. Rank


#### 5\. Jacobian matrix and  hessian matrix
Jocobian matrix: if you have multiple functions and multiple variables, for example, f(x,y) and g(x,y). You want to take the partial derivatives for all functions with respect to all variables. Then all the gradients can be represented in a matrix, which is called Jacobian matrix:
df/dx  df/dy
dg/dx  dg/dy

<br><br>
## Statistics

#### 1\. Likelihood function
Likelihood function is a function of parameters given the observed data. That is, we consider that the observed data are fixed but the paramters can vary. We hope to find a set of parameter values that maximize the likelihood function, which indicate that under the observed data, the model with such parameter values is the most probable model. In other words, we find a set of parameter values to maximize the likelihood function based on the observed data and hope this model is a good approximation to the true model that generates the observed data.

#### 2\. Bayesian vs frequentist statistics


#### 3\. Fisher information

#### 4\. PPV and NPV
PPV is positive predictive value and NPV is negative predictive value. For a test, PPV measures how many true positives among called positives. Note that PPV and NPV depend are the prevalence (for example, the prevalence of a disease is 0.1%). Sensitivity and specificity are two intrinsic test characteristics and they don't depend on the prevalence. But PPV and NPV depend on both the intrinsic test characteristic and the prevalence.

#### 5\.  Newton's method (Newton–Raphson method)

#### 6\.  Bayes theorem
P(A|B) = P(B|A)P(A) / P(B)

#### 7\.  Expecation, variance, covariance

#### 8\. Bayes factor
The raio of the posterior odds to the prior odds. P(D|M1)/P(D|M2), where D is the data and M1,M2 are models. P(D|M) is the likelihood. Bayes factor is quite similar to likelihood ratio test. The difference is that the bayes factor integrates over all parameters in the model, while likelihood ratio test only evaulates the models at some specific sets of values.  

P(D|M1)/P(D|M2) = [P(M1|D)/P(M2|D)] / [P(M1)/P(M2)], this is posterior odds / prior odds. Bayes factor > 1 indicates the model M1 is more supported by the data than model M2. 


<br><br>
## Machine Learning

#### 1\. KL divergence

#### 2\. AUC (C-statistic)
AUC is commonly used to evaluate machine learning models. In the medical filed, it is also called C-statistic or concordance statistic.
Limitations of AUC: (1) No clear interpretations about the meaning of increment in the AUC obtained by adding new variables to the model. (2) The small increments in AUC by adding new variables may have wrong interpretation that no improvement in model predictive preformance. 





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

#### 4\. Saddle point, minimax point, stationary point


#### 5\. LSTM cell and GRU cell

<br><br>
## Healthcare

#### 1\. Administrative data
Administrative data is the data from government or insurance company for administrative purpose, for example evaluating the quality of health care. Compared to EHR data from hospitals, administrative data has patient demongraphic information as well as dignosis information, but may not have detailed treatment or lab result information.   
