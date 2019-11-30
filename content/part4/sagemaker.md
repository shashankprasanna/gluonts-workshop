---
title: "Amazon SageMaker Workflow"
weight: 2
---

In this section you will use Amazon SageMaker to train and tune your DeepAR model. You will use SageMaker automatic model tuner to find better hyperpameters and then deploy the tuned model as an endpoint.

SageMaker is a fully-managed service, which means when you kick off a training job using the SageMaker SDK in the ` 	twitter_volume_sagemaker.ipynb` notebook, few different things happen behind the scene

![sagemaker](/images/labs/sagemaker.png)

* SageMaker spins up request number of instances in a fully-managed SageMaker cluster
* SageMaker pulls the latest (or specified version) of TensorFlow container images, instantiates it on the new instances and loads the training script into the container
* SageMaker copies the dataset over from Amazon S3 and makes it available inside the container for Training
* SageMaker monitors the training and updates progress on the Amazon SageMaker console
* SageMaker copies all the code and model artifacts to Amazon S3 after the training is finished

In addition, SageMaker does a lot more to ensure that the jobs run optimally and you get the best perfomance out-of-the box. As a user you don't have to worry about managing machine learning infrastructure.
