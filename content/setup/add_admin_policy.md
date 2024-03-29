---
title: "Update notebook IAM role"
date: 2019-10-27T23:41:36-07:00
weight: 3
---

### Give your notebook instances admin privileges
{{% notice warning %}}
**Note:** We're providing admin privileges to the SageMaker notebook instance only because we're using this instance as our development environment. In practice, only add policies that you actually need. For the workshop you'll only need access to Amazon S3 and Amazon ECR.
{{% /notice %}}

* Click on the **gluontsworkshop** and you'll see additional details about the instance. Click on the IAM role link, this should take you to the IAM Management Console. Once there, click attach policy button.
![go_to_IAM](/images/setup/go_to_IAM.png)
![attach_policy](/images/setup/attach_policy.png)
* Select **AdministratorAccess** and click on **Attach policy**
![admin attach](/images/setup/admin_attach.png)
* Close the the IAM Management Console window and head back to the SageMaker console.
