# Intro to Deep Learning Tutorial Project

These materials are for the 'Introduction to Deep Learning' tutorial. 
The goal of this tutorial is to get hands-on with PyTorch and GPU Deep Learning (DL).
It is specifically targeted toward attendees who may be familiar with the concepts of DL, but want practical experience.
Familiarity with Python and typical ML packages (e.g. pandas, numpy, sklearn) is expected.

At the end of this session, you will understand how to:
* Build some common DL architectures in PyTorch
* Evaluate and improve the performance of DL models
* Take advantage of more compute (and when you should do so)


## Project Contents
* `admin-setup` folder - contains code for downloading data and other setup for the admin copy of this project
* `1-Load-Data-PyTorch.ipynb` - Tutorial notebook for loading and visualizing data in PyTorch
* `2-Build-Model.ipynb` - Tutorial notebook for training a model with transfer learning
* `3-Improve-Performance.ipynb` - Tutorial notebook for improving model training speed
* `4-Hyperparameters-Tuning.ipynb` - Tutorial motebook for improving model accuracy
* `Deep-Learning-Tutorial-slides.pdf` - Slide deck for the tutorial

## Project setup
The below recommended flow for setting up this project assumes it has been uploaded to a Domino deployment as a public project, and a Domino admin has set up the prerequisites listed below.
1. Fork the project
2. In your forked copy of the project, mount the data as follows
    * go to the **Materials** section in the left navigation of the project and click **Data**
    * go to the **Domino Datasets** tab
    * click **Mount Shared Dataset**
    * choose **Serengeti4kImages** from the searchable dropdown and click **Mount Dataset**
3. Launch a Workspace to explore the notebooks.
    * go to the **Run** section in the left navigation of the project and click **Workspaces**
    * click **Create New Workspace**
    * choose **Deep Learning Tutorial** from the workspace environment drop-down
    * choose **JupyterLab** as the IDE
    * choose a **GPU** tier from the hardware tier drop-down (the smallest available GPU is fine)
    * click **Launch Now**

## Prerequisites
These should be completed by a Domino admin.

### Dataset setup
The public copy of this project should have a Dataset called `Serengeti4kImages` available to mount to other projects.
See `admin-setup/Download-Workshop-Data.ipynb` for details on downloading the data into the Dataset.

### Compute Environment
There should be a Compute Environment called `Deep Learning Tutorial` available with the following properties.
* Custom base image: `quay.io/domino/ngc-pytorch:20.12-py3`
* Dockerfile instructions: `RUN pip install line_profiler`
* Pluggable workspace tools:

```
jupyterlab:
  title: "JupyterLab"
  iconUrl: "/assets/images/workspace-logos/jupyterlab.svg"
  start: [  /opt/domino/workspaces/jupyterlab/start ]
  httpProxy:
    internalPath: "/{{ownerUsername}}/{{projectName}}/{{sessionPathComponent}}/{{runId}}/{{#if pathToOpen}}tree/{{pathToOpen}}{{/if}}"
    port: 8888
    rewrite: false
    requireSubdomain: false
vscode:
  title: "vscode"
  iconUrl: "/assets/images/workspace-logos/vscode.svg"
  start: [ "/opt/domino/workspaces/vscode/start" ]
  httpProxy:
    port: 8888
    requireSubdomain: false
```

Equivalent environments are likely to work as well, but have not been tested.
(For example, NGC pytorch images used with the option to [Automatically make compatible with Domino](https://docs.dominodatalab.com/en/latest/user_guide/4e0c34/create-a-domino-environment-with-a-pre-built-image/), or any other environment with working pytorch installed.)
If the `line_profiler` package is not installed, it can also be installed within the tutorial notebook where needed.


## Reference material
* Data location - https://www.zooniverse.org/projects/zooniverse/snapshot-serengeti
* Article - https://www.pnas.org/content/115/25/E5716
* Article code repo - https://github.com/Evolving-AI-Lab/deep_learning_for_camera_trap_images

