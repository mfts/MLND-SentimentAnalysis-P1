# Deploy a Sentiment Analysis Model

## Introduction

[Sentiment Analysis Web App](https://github.com/mfts/MLND-SentimentAnalysis-P1/tree/master/project) is a notebook and collection of Python files to deploy a RNN performing sentiment analysis on movie reviews complete with publicly accessible API and a simple web page which interacts with the deployed endpoint. 

For the movie reviews we are using the [IMDB dataset](http://ai.stanford.edu/~amaas/data/sentiment/).

## Installation

### Log in to the AWS console and create a notebook instance

Log in to the AWS console and go to the SageMaker dashboard. Click on 'Create notebook instance'. The notebook name can be anything and using ml.t2.medium is a good idea as it is covered under the free tier. For the role, creating a new role works fine. Using the default options is also okay. Important to note that you need the notebook instance to have access to S3 resources, which it does by default. In particular, any S3 bucket or object with sagemaker in the name is available to the notebook.

### Use git to clone the repository into the notebook instance

Once the instance has been started and is accessible, click on 'open' to get the Jupyter notebook main page. We will begin by cloning the SageMaker Deployment github repository into the notebook instance. Note that we want to make sure to clone this into the appropriate directory so that the data will be preserved between sessions.

Click on the 'new' dropdown menu and select 'terminal'. By default, the working directory of the terminal instance is the home directory, however, the Jupyter notebook hub's root directory is under 'SageMaker'. Enter the appropriate directory and clone the repository as follows.

```bash
cd SageMaker
git clone https://github.com/mfts/MLND-SentimentAnalysis-P1.git
```

After you have finished, close the terminal window.

### Follow the notebook for further instructions to build, train and deploy the model to Sagemaker.