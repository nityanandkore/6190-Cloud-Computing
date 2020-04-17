# What problems does Sagemaker solve?

Amazon SageMaker is a fully managed service that provides every developer and data scientist with the ability to build, train, and deploy machine learning (ML) models quickly. SageMaker removes the heavy lifting from each step of the machine learning process to make it easier to develop high quality models.
Traditional ML development is a complex, expensive, iterative process made even harder because there are no integrated tools for the entire machine learning workflow. You need to stitch together tools and workflows, which is time-consuming and error-prone. SageMaker solves this challenge by providing all of the components used for machine learning in a single toolset so models get to production faster with much less effort and at lower cost.

SageMaker is a platform for developing and deploying ML models. It promises to ease the process of training and deploying models to production at scale. To accomplish this goal, it offers services that aim to solve the various stages of the data science pipeline such as:

Data collection and storage
Data cleaning and preparation
Training and tuning ML models
Deploy to the cloud at scale

With that in mind, SageMaker positions itself as a fully managed ML service. The typical workflow for creating ML models involve many steps. In this context, SageMaker aims to abstract the process of solving each one of these stages. In fact, as we will see, by using SageMaker’s built-in algorithms, we can deploy our models with a simple line of code.


# What are competitive offerings to Sagemaker?

## Exploratory Data Analysis

The first step would be to get acquainted with the data by performing some exploratory data analysis. We can quickly fire up a notebook instance using the SageMaker console, which provides us with the Jupyter notebook.
Data can be loaded onto the notebook instance from any source. We can upload it directly from our work machines or alternatively, data can be easily pulled in from S3 buckets, AWS Athena, AWS Redshift or any other cloud storage services. In case we need to perform sizable ETL operations on input data, we can create AWS Glue jobs which can process the data and make it available in S3 buckets.
Since our car insurance data is small, we could upload the .csv files directly from our work machines. The .csv files can be processed using various preloaded python libraries allowing us to quickly visualize the data and understand the input variables in great detail.

## MODEL BUILDING
After understanding the data, we can apply some feature engineering to prepare the data for training.

## MODEL TRAINING
Now that the data is ready, we can create a training job to build our ML model. A training job requires data to be uploaded to the S3 bucket. We will use the XGBoost algorithm container, which comes built-in with SageMaker, to create our ML model. There are several hyper parameters available for configuration by data scientists. Let’s configure them with default settings and create a training job. We have parameterized the training job to use a single instance of ml.m4.xlarge ML instance and provided a path for input as well as output data.

## MODEL DEPLOYMENT

Now that our model is deployed and ready to serve predictions, let’s test its performance using the test data. 
In case we prefer batch predictions as opposed to hosting a live endpoint, we can use the SageMaker Batch Transform feature. Just like a training job, it can spin up an ML instance, run predictions on input data and make the predictions available to the output path. Once done, the batch transform job tears down the ML instance.
Another extremely useful feature is A/B testing. This is used to test the performance of a new model geared towards only a certain subset of users. Sagemaker provides native support for deployment using A/B testing.

## MODEL TUNING
Furthermore, as advanced functionality, we can employ the SageMaker hyperparameter tuning to find the best set of hyper parameters for tuning the ML model. On the algorithm XGBoost, SageMaker natively supports hyper parameter tuning. As part of the tuning job, SageMaker will run multiple training jobs and vary the hyper parameters in the ranges provided by the user. On execution, the results of the experiment are provided for the data scientists to choose the best model.

# Post a screenshot of a lab where you had difficulty with a concept or learned something.
In progress
