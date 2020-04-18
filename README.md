



# COMP 4102 - Final Project
Classification of NBA Teams


Team Members:
Abubakar Abdulsalam, Gurveer Dhindsa

# Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites
For building and running the application you may need:
- [Jupyter Notebook](https://jupyter.org/install)

### Installing
First, clone this repository to your local machine using `https://github.com/AbubakarAbdulsalam/COMP4102_Project.git

### Running the application locally
Option 1:
To view the mode code, execute
```
jupyter notebook TrainedModel.ipynb
```
To view a sample rediction, execute
```
jupyter notebook SamplePrediction.ipynb
```

Option 2:
There is an option to view source code WITHIN GitHub/Google Colab. To do so, click on a .ipynb file within the GitHub repository.
Also, you can click the 'Open in Colab' button on the top of the .ipynb file to open it in Google Colab. This way you can run execute the file within your browser!
Note, running TranedMode.ipynb could take up to several hours as we are dealing with such a large dataset.

# 1. Abstract
This project is aimed towards classifying and detecting 30 National Basketball Association (NBA) teams in the current 2020 season. This can assist the general population in identifying and learning about the various teams by simply taking a photograph containing a logo. The photograph can be anything ranging from a teams’ poster, merchandise item or the floorboards of the stadium.

# 2. Introduction
For this project, we are utilizing convolutional neural networks (CNN) for image classification. Neural networks have found a varying amount of use in classification problems over the past decade. Convolutional neural networks are however, used mostly with classification problems. A convolutional neural network is a special kind of feedforward neural network that  reduces the number of parameters in a deep neural network with many units without losing too much in the quality of the model. Convolution neural networks have found applications in image and text processing where they beat many previously established benchmarks. A feedforward neural network aims to approximate a function. The flow of information occurs in the forward direction. The challenges with this algorithm include the collection of significant enough dataset that is normally required by neural networks. We needed to also separate the different iterations, the logos of several teams have gone through from the present version being used.

# 3. Background
For non-basketball fans or fans alike, it may become difficult to distinguish the logos of the 30 different NBA teams. NBA stadiums and merchandise containing such logos can be troublesome for individuals with vision-related disabilities as they may not know the team associated with the logo. In this project, we aim to develop a classification system that accepts a square photograph of anything containing a logo. This photograph can consist of anything ranging from a teams’ poster, a merchandise item or the floorboards of their stadium. The photograph can contain various types of noise but only one requirement must be in place, a logo must be present. This project involves the use of a smartphone device by leveraging its camera technology. 

# 4. Approach
A neural network (NN), is a mathematical function y = fNN(x). So, for a 3-layer neural network that returns a scalar, fNN is represented by y = fNN(x) = f3(f2(f1(x))). Where f1 and f2 are vector functions of the following form fl(z) d=ef gl(Wlz + bl). The variable l is called the layer index and can span from 1 to any number of layers. The function gl is called an activation function. It is a fixed, usually nonlinear function. The parameters Wl (a matrix) and bl (a vector) for each layer are learned using the gradient descent algorithm by optimizing a particular cost function (such as MSE). A convolutional neural network being a variation of the feedforward neural network just works a bit differently to an FFNN. In images, pixels that are close to one another usually represent the same type of information: sky, water, leaves, fur, bricks, etc. The exception from the rule are the edges. CNN splits an image into square patches using a moving window approach. Numerous small sized filters are used to detect certain patterns in the square patches of an image since most useful information in an image is localized. An example is given below, assuming the size of the square patches used is 3 and that P is a sample patch of a grayscale image with P.

A filter would need to learn to detect the pattern contained in this patch of image, and the size of that filter would be a 3 x 3 matrix.  The values contained in these filters are called parameters. Parameters at positions corresponding to the 1s in the image patch would be positive, while parameters in positions corresponding to the 0s in the image patch would be close to zero. When the image patch is convolved with the filter matrix, the higher the resultant value, the more similar the filter matrix is to the image patch. An example is shown in Figure 1 when the result of the convolution is 12. If the shape of the matrix P (input patch) is changed even slightly, say element at row 1, column 2 is changed to a 0. The convolution with the filter matrix F becomes 10, which signifies less similarity to the filter F.


# 5. Challenges
## 5.1. Goals and Deliverables
The challenges we face include a non-existent dataset. Classification is something that has been done before, but not in terms of classifying NBA logos. In order to successfully complete this project with a high accuracy at classifying, research about machine learning must be completed as an additional component as this project touches upon machine learning concepts. 
The main deliverable for this project is a trained model with saved parameters. The later stages of this project will involve the use of Keras to develop a model trained to classify NBA logos. Keras is an open-source library that can be used in Python to create and research about deep learning models. 

To achieve the deliverable of this project, our team will need to collect a dataset containing at least 40 images of each of the 30 NBA logos. It is unfeasible to take each of these pictures personally, so we will require the assistance of online resources. The images will be labelled during the training stage and a subset will be selected to be held back for testing the models. In terms of measuring our success for this project, we have decided that a 80% accuracy will be the benchmark to be equaled or surpassed by our model.

## 5.2. Schedule
The following schedule is designed in order to complete the project in advance by some days. A safety net is set in place so that we can counter any unexpected issues and prepare for the presentation ahead of time. Weekly tasks are specified below.

#### Week 1 (February 1, 2020)
During this week we expect to begin our data collection for each of the 30 NBA logos. Since there are no available datasets online, we will be creating our own dataset by scraping data from online webpages. Each member will also conduct research about image processing and manipulation.

#### Week 2 (February 8, 2020)
During this week, we expect to complete data collection and shift our research towards image classification. The dataset of NBA logos will also need to be cleaned prior to developing the model. The cleaning process will begin during the later days of this week.

#### Week 3 (February 15, 2020)
During this week, we will have successfully cleaned the dataset. Data cleaning in this case is very important, because data scraped from online is unlikely to be uniform. Image processing and manipulation will take place during this week. For example, our images may require transformations and size adjustments. More information regarding this topic will be achieved through the research phase in week 1. 

#### Week 4-6 (February 22, 2020 - March 7, 2020)
During the beginning days of week 4, we expect to be working on our first iteration of the model. There are different configurations of models to be trialed and we do not expect to have our first version perfected. Hence, we have grouped weeks 5 and 6 as the tasks for each group member will be relatively the same. It will involve iterative research and developing a variety of models, while comparing their performances.

#### Week 7 (March 14, 2020)
During this week, we expect to have more than one model working well. We plan on combining these models to produce another model with optimal performance. 

#### Week 8-9 (March 21, 2020 - March 28, 2020)
For preparations of the final presentation and submission, this week will be dedicated to documentation such as the work done and the processes used to complete the project.

# 6. Results
We experimented with different combinations of layers of neural networks, before settling on the final model summarised in Figure 2 below. The final model presented us with a significantly higher accuracy score on the validation dataset we had, than the previous iterations of models we tried.

# 7. List of Work
Equal work was performed by both project members. Refer to section 5.2 for a detailed breakdown of the tasks performed.

# 8. GitHub Page
The source code of this project can be at github.com/AbubakarAbdulsalam/COMP4102_Project. In order to open the .ipynb file, Jupyter Notebook must be installed on the machine. For more information regarding Jupyter Notebook setup, refer here. Upon cloning the repository, the TrainedModel.ipynb file can be opened in Jupyter Notebook but executing the terminal command jupyter notebook TrainedModel.ipynb in the root directory of the project. This will open a page in your default web browser.

# 9. References
A. Burkov, The hundred-page machine learning book. Quebec, Canada?: Andriy Burkov, 2019.

Upadhyay, Y. (2019, March 8). Feed forward Neural Networks. Retrieved from https://towardsdatascience.com/feed-forward-neural-networks-c503faa46620

