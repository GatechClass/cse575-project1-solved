# cse575-project1-solved
**TO GET THIS SOLUTION VISIT:** [CSE575-Project1 Solved](https://mantutor.com/product/cse575-project1-solved/)


---

**For Custom/Order Solutions:** **Email:** mantutorcodes@gmail.com  

*We deliver quick, professional, and affordable assignment help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;65264&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSE575-Project1 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
In this part, you need to first perform parameter estimation for a given dataset (which is a subset from the MNIST dataset). The MNIST dataset contains 70,000 images of handwritten digits, divided into 60,000 training images and 10,000 testing images. We use only images for digit “7” and digit “8” in this question.

Therefore, we have the following statistics for the given dataset:

Number of samples in the training set:&nbsp; “7”: 6265 ;”8″: 5851.

Number of samples in the testing set: “7”: 1028;&nbsp;&nbsp; “8”: 974

You are required to extract the following two features for each image:

<ol>
<li>The average of all pixel values in the image</li>
<li>The standard deviation of all pixel values in the image</li>
</ol>
We assume that these two features are independent, and that each image (represented by a 2-D features vector) is drawn from a 2-D normal distribution.

<a href="http://yann.lecun.com/exdb/mnist/">You may go to the original MNIST dataset (available here</a><a href="http://yann.lecun.com/exdb/mnist/"> http://</a><a href="http://yann.lecun.com/exdb/mnist/">y</a><a href="http://yann.lecun.com/exdb/mnist/">ann.lecun.com/exdb/mnist/ </a><a href="http://yann.lecun.com/exdb/mnist/">(</a><a href="http://yann.lecun.com/exdb/mnist/">Links to an external site.)</a><a href="http://yann.lecun.com/exdb/mnist/"><strong>&nbsp;(http://</strong></a><a href="http://yann.lecun.com/exdb/mnist/"><strong>y</strong></a><a href="http://yann.lecun.com/exdb/mnist/"><strong>ann.lecun.com/exdb/mnist/) </strong></a><a href="http://yann.lecun.com/exdb/mnist/">) to extract the images for digit 7 and digit 8, to form t</a>he dataset for this project. To ease your effort, we have also extracted the necessary images, and store them in “mnist_data.mat” files. The file can be downloaded <a href="https://asu.instructure.com/courses/31489/files/7881772/download?wrap=1"><strong>here.</strong></a> A description of the file can be downloaded <a href="https://asu.instructure.com/courses/31489/files/7882575/download?wrap=1"><strong>here</strong></a>

You may use the following piece of code to read the dataset: import scipy.io

Numpyfile= scipy.io.loadmat(‘mnist_data.mat’)

The specific algorithmic tasks you need to perform for this part of the project include:

<ol>
<li>Extracting the features and then estimating the parameters for the 2-D normal distribution for each digit, using the training data. Note: You will have two distributions, one for each digit.</li>
<li>Use the estimated distributions for doing Naïve Bayes classification on the testing data. Report the classification accuracy for both “7” and “8” in the testing set.</li>
<li>Use the training data to train a Logistic Regression model using gradient ascent. Report the classification accuracy for both “7” and “8” in the testing set.<strong> Note that you are not allowed to use package like sklearn to compute the boundary. You need to implement your own version for using gradient ascent to find the solution.</strong></li>
</ol>
<strong>Algorithms:</strong>

MLE Density Estimation, Naïve Bayes classification, Logistic regression

<strong>Resources:&nbsp; </strong>

<a href="http://yann.lecun.com/exdb/mnist/">A subset of MNIST dataset, download either from</a><a href="http://yann.lecun.com/exdb/mnist/"> http://</a><a href="http://yann.lecun.com/exdb/mnist/">y</a><a href="http://yann.lecun.com/exdb/mnist/">ann.lecun.com/exdb/mnist/ </a><a href="http://yann.lecun.com/exdb/mnist/">(</a><a href="http://yann.lecun.com/exdb/mnist/">Links to an external site.)</a><u>&nbsp;&nbsp;&nbsp; </u><a href="http://yann.lecun.com/exdb/mnist/"><strong> (http://</strong></a><a href="http://yann.lecun.com/exdb/mnist/"><strong>y</strong></a><a href="http://yann.lecun.com/exdb/mnist/"><strong>ann.lecun.com/exdb/mnist/) </strong></a><a href="http://yann.lecun.com/exdb/mnist/">(requiring you to extract data corresponding to digit 7 and digit </a>8 only),&nbsp; or from the .mat files provided.

<strong>Workspace: </strong>

Any Python programming environment.

<strong>Software: </strong>

Python environment.

<strong>Language(s): </strong>

Python. (MATLAB is equally fine, if you have access to it.)

<strong>Required Tasks:</strong>

<ol>
<li>Write code to extract features for both training set and testing set.</li>
<li>Write code to implement the Naive Bayes Classifier and use it produce a predicted label for eachtesting sample.</li>
<li>Write code to implement the Logistic Regression and use it produce a predicted label for each testingsample.</li>
<li>Write code to compute the classification accuracy, for both the Naive Bayes Classifier and LogisticRegression.</li>
<li>Write a short report summarizing the results, including the final classification accuracy.</li>
</ol>
<strong>Note that you are not allowed to use package like sklearn to compute the boundary.</strong>

<strong>Optional Tasks:</strong>

<ol>
<li>Repeat the experiments for different pairs of digits.</li>
<li>Consider doing multi-class classification.</li>
</ol>
Optional tasks are to be explored on your own if you are interested and have extra time for them. No submission is required on the optional tasks. No grading will be done even if you submit any work on the optional tasks. No credit will be assigned to them even if you submit them. (So, please do not submit any work on optional tasks.)

<strong>What to Submit:</strong>

Code:

Acceptable file types are .py/.m or .zip.

If you have only one file, name the file to be main.py or main.m for matlab users, and submit it.

If you have multiple code files, please name the main file as main.py and name other files properly based on its content; Similarly, for matlab users, you should have only one main.m and other relevant .m files.

Next, zip all the files and submit Code.zip file.

Documentation comment is important and required. Be sure to read through the directions carefully to ensure you have included all necessary parts in your code.

Report:

Acceptable File types: .pdf

Length: 2-5 A4 pages

Content: Include the formula that you used to estimate the parameters, the estimated values for the parameters, the expression for the estimated normal distributions, an explanation for how the distributions are used in classifying a testing sample, and the final classification accuracy for both “7” and “8” for the testing set.

&nbsp;
