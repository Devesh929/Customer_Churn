# Customer Churn Prediction and Reason-for-leaving Prediction using Machine Learning

We have built a sample prototype to demonstrate how we will develop real industry level solutions. This prototype  helps to identify  about-to-withdraw customers  and act accordingly to ensure that the bank can take the best-possible course of actions. Also the prototype predicts the possible reasons of leaving for a customer which may give a better picture of customer thoughts.

The software (web-app) provides the following features: 

1. Create a *user-friendly* interface which will help bank with clear and easy-to-interpret visual data. 

2. Predict probability of a current customer to leave bank ranging from 0 to 1 
   where 0 will denote that customer will never leave bank and 1 will denote that customer is definitely going to leave bank. 
   
3.  Provide quick & on-demand data of top percentage of people likely to leave . Enables user to streamline their focus on required number of people . However choosing to predict for any customer from the data is always an option . 

4. Show all details , prediction of probability of a customer leaving bank along with its graph.
   Also show probability of different reasons of leaving for each customer and display easy-to-interpret pie-charts demonstrating each reason for in-depth analysis . 
This pie-chart graph shows that if probability of churn becomes true and customer really leaves, then what factors will contribute to  his/her leaving the organization, i.e. , reasons for leaving and it will show probability of each reason contributing to his/her withdrawal from services of organization.

### Using this prototype live !
This prototype to predict customer churn is live at https://synd-demo.herokuapp.com/ !!
We have deployed whole machine-learning model on web for ease-of-access . Simply go to this url and login using the below 
username and password . 

Username - ```bank``` <br>
Password - ```bank```

## How to use the web-app : a walkthrough

Visit the link mentioned above to launch the fully functional web-application.
On clicking the link, a page like this will appear:




Enter the login credentials provided above, **note** that entering wrong credentials will prevent user-login!

Now , user will have the choice of entering request data.




Through Default File , we have provided a sample testing file-  ```testtestdefault1``` , located in the `default` folder for the user , which is of this format:




As shown , the file requires these entries , along with an empty column of  **Exited** which represents exiting probability from 0-1.

Now, on clicking **Predict** , a dropdown menu consisting of all employee-ids is available. <br> We have also provided the feature of **Show Top X%** most likely to leave, which will depend on percentage of total data required by a user . Along with it are sample buttons which show selective-data ex. TOP-2 , TOP-4 likely to leave customers.



Select any customer from drop-down menu and click **Predict** -



A data-visualised meter showing churn-risk (low-medium-high) , along with top reasons for leaving and details of customers is shown.
To try out more features , user can **Go Back** to previous stage.<br>
User may enter required percentage and **Show** - 



Visualisation of required *top x%* of people likely to leave appears , through which user can be redirected to the result page on clicking and generating a link of the respective Customer through Customer ID by clicking the interactive bar-graphs .

A sample of **TOP 2** - 


Similarly , viewing **TOP 4** - 


Also through the feature of **Upload Test Data File** , one can choose his/her own test requirements for prediction and analysis.
We have provided a sample ```uploadtest.csv``` for the user.




As usual , you can select any customer for whom you want to calculate the risk.
**Keep in mind**- The user testdata file must be of **same format** as that of the sample shown.




It shows the prediction further , smiliar to Default file shown :





As shown , the **Enter input X%** is still available , along with interactive data representation . 



When done , customer can **Logout** anytime .


Our web-app uses pre-loaded ```.h5``` models for prediction . These ```.h5``` models are built on our local machines using Python.
The models are based on *Keras and Neural networks* . So we need Keras and other Machine Learning libraries on our web environment to 
load this pre-defined models.
In our live web-app we have already made the environment.If you want to know how our models are trained on local machines and you want to see the working & code of models, check the code of ```howmodel1isbuilt.py``` and ```howmodel2isbuilt.py```


## How to run locally 

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Pre-requisites

* Creating a virtual environment using [Anaconda](https://www.anaconda.com/download/). If you need to create your workflows in Python and keep the dependencies separated out or   share the environment settings, Anaconda distributions are a great option.

The following main Python-based libraries have been used :

* ```Flask```
* ```Numpy```
* ```Pandas```
* ```Tensorflow```
* ```Keras```

which will be installed during setting the environment.

Provided the requirements are already installed in your system , you can simply execute the .py script named ```flask_app.py```
However, for future deployment purposes it is essential to create a virtual environment.

#### Step 1 : Main Directory
Go to command prompt/terminal (for Linux users) and change to the project as the default directory.
Example: If current path is ```C:\Users\name>```
change to ```C:\Users\name>cd Desktop\flasksite```  (if downloaded to Desktop)

#### Step 2 : Create environment
Create a conda environment using ```conda create -n env```
This will create an empty Python environment with name ```env``` . 
Activate using ```activate env```
To exit from the virtual environment , simply execute ```deactivate env ```
For further information , you can refer [here](https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/20/conda/)

#### Step 3 : Install required libraries
Anaconda distribution comes with many default downloaded libraries which the user can directly , however to efficiently manage the
environment , manually install libraries.
A simple way would be to use ```pip``` - Python default package manager
```pip install [nameOfPackage]```
Install the libraries specified in pre-requisites
Example:
* ```pip install flask```
* ```pip install numpy```

For more information about ```pip``` you can refer [documentation](https://docs.python.org/3/installing/index.html)

#### Step 4 : Execute script
When all python dependencies are installed , simply execute the .py script named ```flask_app.py```  
```python flask_app.py ``` in the cmd prompt should do the task.
Follow the link generated, and the flask code should be up and running !




