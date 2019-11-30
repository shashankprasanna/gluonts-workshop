---
title: "Install MXNet and GluonTS"
weight: 5
---
### Install MXNet and GluonTS into the Python3 conda environment
* On the terminal, activate python3 environment

```
$ source activate python3
```
![launch jupyter](/images/setup/conda_env.png)

{{% notice warning %}}
**Stop:** Do not proceed without activating the python3 environment first. Install MXNet and GluonTS in the base other environments may result in incorrect or corrupt installation.
{{% /notice %}}

* First install MXNet. Install version 1.4.1 which is compatible with GluonTS.

```
$ pip install mxnet==1.4.1
```

To install MXNet for other operating systems, GPU support  etc, visit the [MXNet Get Started page](https://mxnet.apache.org/get_started/)

* Install GluonTS
```
$ pip install gluonts
```

Now we're ready to start time-series modeling!
