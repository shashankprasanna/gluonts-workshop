---
title: "Download the workshop content"
date: 2019-10-28T00:14:06-07:00
weight: 4
---
### Launch JupyterLab client and clone the workshop repository
* Your notebook instance should now be ready. Click *JupyterLab* to launch your client.
![launch jupyter](/images/setup/launch_jupyter.png)

* Click *File > New >  Terminal* to launch terminal in your JupyterLab instance.
![Launch terminal](/images/setup/launch_terminal.png)

* Download the workshop code and notebooks. Enter bash (optional), change directory to ~/SageMaker, clone the repository
```bash
bash
cd ~/SageMaker
git clone https://github.com/aws-samples/amazon-sagemaker-time-series-prediction-using-gluonts
```

* Confirm that you're able to see the contents. Should see 3 parts
```
ls amazon-sagemaker-time-series-prediction-using-gluonts/notebooks
```
