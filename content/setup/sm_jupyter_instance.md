---
title: "Launch a SageMaker notebook instance"
date: 2019-10-27T22:39:43-07:00
weight: 2
---

{{% notice info %}}
**Note:** In this workshop, we'll be using an Amazon SageMaker notebook instance for simplicity and convenience. You can use your own laptop, workstation or EC2 instance to perform steps detailed in this and subsequent sections. You'll just need to make sure you have the latest version of MXNet and GluonTS. If you're going to be using other AWS services such as Amazon S3, Amazon SageMaker, you'll need to make sure that you have the right privileges to access these AWS services. The SageMaker Jupyter notebook on the other hand is preconfigured and ready to use.
{{% /notice %}}

### Launch an Amazon SageMaker notebook instance

* Open the [AWS Management Console](https://console.aws.amazon.com/console/home)
{{% notice info %}}
**Note:** This workshop has been tested on the US West (Oregon) (us-west-2) region. Make sure that you see **Oregon** on the top right hand corner of your AWS Management Console. If you see a different region, click the dropdown menu and select US West (Oregon)
{{% /notice %}}

* In the AWS Console search bar, type SageMaker and select Amazon SageMaker to open the service console.
![SageMaker Console](/images/setup/setup_aws_console.png)
* Click on Notebook Instances
![Launch notebook instance 1](/images/setup/setup_notebook.png)
* From the Amazon SageMaker > Notebook instances page, select Create notebook instance.
![Launch notebook instance 2](/images/setup/setup_create_notebook.png)
* In the Notebook instance name text box, enter a name for the notebook instance.
 * For this workshop select **"gluontsworkshop"** as the instance name
 * Choose ml.c5.xlarge. We'll only be using this instance to launch jobs.
 * Volume size 50 - this is only needed for building docker containers or when dealing with larger datasets.
![Fill notebook instance](/images/setup/setup_fill_notebook.png)
* To create an IAM role, from the IAM role drop-down list, select Create a new role. In the Create an IAM role dialog box, select Any S3 bucket. After that select Select **Create role**. Amazon SageMaker creates the **AmazonSageMaker-ExecutionRole-*** ** role.
![iam](/images/setup/notebook_iam.png)
* Keep the default settings for the other options and click Create notebook instance. On the **Notebook instances** section you should see the status change from *Pending -> InService*
* While the notebook instance spins up, continue to work on the next section, and we'll come back and launch the instance when it's ready.
