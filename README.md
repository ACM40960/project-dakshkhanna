# Face-Mask Detection System using Keras,TensorFlow and OpenCV
**README.md**

The aim of this project is to develop a Face Mask Detection/Recognition System 
that, amidst the global pandemic, helps in  detecting whether a person is wearing a 
face mask or not that can help in multiple ways including, entrance to any hospital, 
students in schools, etc.

The detection system uses Python Programming with Deep Learning, TensorFlow, Keras and
OpenCV.

This is a 2-Step system, namely, Training and detection, where, the program is first trained, 
and then the trained program using OpenCV, uses the in-built Webcam to Live-Test/detect whether 
a person is wearing a mask or not.

Here, I am using Python 3.9.12. 

We will check if Python is already installed in the system and then we will check for the version as described:

**For Windows :**

1. Open cmd/terminal/windows powershell

2. Run the following Command in the console: 
```python
python -V
```
If Python is installed, it will give you the version of the python installed like this:

![version check](https://user-images.githubusercontent.com/105723324/181034088-c73941b8-8077-4eb2-aa3e-97e6c6e6db03.png)

Otherwise, We will first install Python by:

**PreRequisites**
1. A system running Windows 10 with admin privileges
2. Command Prompt (comes with Windows by default) 

**Step 0: Go to https://www.python.org/downloads/ and select your operating system and Version to be downloaded:**

<img width="1439" alt="Screenshot 2022-07-26 at 13 53 56" src="https://user-images.githubusercontent.com/105723324/181011097-baa3beee-8409-4104-824f-d02209ee452b.png">

**Step 1: Download Python Executable Installer**

![Step1](https://user-images.githubusercontent.com/105723324/181026244-64308f87-1483-4b03-8845-9125fbd5edb7.png)

**Step 2: Run Executable Installer**

1. Run the Python Installer once downloaded. (In this example, we have downloaded Python 3.10.5.)

2. Make sure you select the Install launcher for all users and Add Python 3.10 to PATH checkboxes. The latter places the interpreter in the execution path. For older versions of Python that do not support the Add Python to Path checkbox.

3. Select Install Now – the recommended installation options.

![Python Installer](https://user-images.githubusercontent.com/105723324/181026303-ebc3d83c-7009-4779-9a9c-cf6dd5c93b49.png)


For all recent versions of Python, the recommended installation options include Pip and IDLE. Older versions might not include such additional features.

4. The next dialog will prompt you to select whether to Disable path length limit. Choosing this option will allow Python to bypass the 260-character MAX_PATH limit. Effectively, it will enable Python to use long path names.


![Successfull Installation](https://user-images.githubusercontent.com/105723324/181026325-d1d473c9-31e4-4e1b-88d4-0cd615f1029f.png)


The Disable path length limit option will not affect any other system settings. Turning it on will resolve potential name length issues that may arise with Python projects developed in Linux.

**Step 3: Verify Python Was Installed On Windows**

1. Navigate to the directory in which Python was installed on the system. In our case, it is C:\Users\Username\AppData\Local\Programs\Python\Python37 since we have installed the latest version.
2. Double-click python.exe.
3. The output should be similar to what you can see below:

![version check](https://user-images.githubusercontent.com/105723324/181026343-235c2718-6e03-412a-955d-61d91926c64b.png)

**Step 4: Verify Pip Was Installed**

If you opted to install an older version of Python, it is possible that it did not come with Pip preinstalled. Pip is a powerful package management system for Python software packages. Thus, make sure that you have it installed.

To verify whether Pip was installed:

1. Open the Start menu and type "cmd."
2. Select the Command Prompt application.
3. Enter pip -V in the console. If Pip was installed successfully, you should see the following output:

![pip check](https://user-images.githubusercontent.com/105723324/181026361-64100eee-7706-478c-8b41-f7c3c78b6b34.png)

I am using Mac here,

**For Mac :**

1. Open Terminal

2. Run the following command in the terminal :

```python
python --version
```
If Python is installed, it will give you the version of the python installed like this:

<img width="414" alt="Screenshot 2022-07-26 at 13 48 02" src="https://user-images.githubusercontent.com/105723324/181009503-fc5a7eb1-5ec2-4e73-b15c-c73645c82e26.png">

As we can see that the version is Python 3.9.12, which is the latest version.

If not, Following steps can be done to install python in mac:

**Step 0: Go to https://www.python.org/downloads/ and select your operating system and Version to be downloaded:**

<img width="1440" alt="Screenshot 2022-07-26 at 15 11 18" src="https://user-images.githubusercontent.com/105723324/181027203-fe808b26-169f-4e02-9d71-ac33196b3390.png">

**Step 1: Download Python Executable Installer**

<img width="1438" alt="Screenshot 2022-07-26 at 15 12 43" src="https://user-images.githubusercontent.com/105723324/181027527-aaa554f0-655f-4193-a740-1615b6e08f8c.png">

**Step 2: Run Executable Installer**

1. Run the Python Installer once downloaded. (In this example, we have downloaded Python 3.10.5.)
2. Click Continue -> Continue -> Continue -> Agree -> Install 

<img width="617" alt="Screenshot 2022-07-26 at 15 14 01" src="https://user-images.githubusercontent.com/105723324/181028072-a038fa5e-2e91-4e37-8789-e046f3f81733.png">

After Installation is successfull, similar dialogue box should appear: 

<img width="620" alt="Screenshot 2022-07-26 at 15 14 27" src="https://user-images.githubusercontent.com/105723324/181028437-5dba26b6-eaea-47a9-960c-bbf4c70dee71.png">


**Step 3: Verify Python Was Installed On Mac**

1. Open Terminal

2. Run the following command in the terminal :

```python
python --version
```
If Python is installed, it will give you the version of the python installed like this:

<img width="424" alt="Screenshot 2022-07-26 at 15 18 09" src="https://user-images.githubusercontent.com/105723324/181028679-c66ca897-110a-4e30-942d-67b515f49996.png">


Now that latest version of Python is installed and we will move to the IDE.

Here, I have used Jupyter Notebook.

Steps to download/install Jupyter Notebook: 

For you to work on Jupyter Notebook, you need to download Anaconda-Navigator:

The Jupyter Notebook is an open source web application that you can use to create and share documents that contain live code, equations, visualizations, and text. Jupyter Notebook is maintained by the people at Project Jupyter.

## Installation Guide ##

User must first install Anaconda according to their system requirements from [Anaconda Installation](https://www.anaconda.com/products/distribution). The instructions to install can be found on [Installation Guide](https://docs.anaconda.com/anaconda/install/#). 

After the installation, open Anaconda Navigator and click Launch on the Jupyter Notebook application.

<img width="1439" alt="Screenshot 2022-07-26 at 15 27 02" src="https://user-images.githubusercontent.com/105723324/181032639-9814bb0f-67c6-4e2b-b10e-879d717abefa.png">

*Note that Jupyter python script as an extension of .ipynb unlike .py for other python scripts. So the user should open the script using Jupyter Notebook.*


## Running the code ##

The following section shows the steps to run the code/project on your respective systems.

## Steps ##

0. Open the terminal in your respective operating system.

1. Clone the repository 

```python 
git clone https://github.com/ACM40960/project-dakshkhanna 
```

Or

1. Download the Zip folder (Master)

<img width="1440" alt="Screenshot 2022-07-26 at 16 18 26" src="https://user-images.githubusercontent.com/105723324/181045370-47600fd6-fbf4-43ce-9a12-84c8d3b13606.png">

2. Finally, return to the JupyterLab window launched previously, click on the folder icon in the top left corner of the window, and navigate to the newly created project folder. Then double-click on the ACM40960_21200399.ipynb or Click View on file located in this folder to open the Jupyter Notebook (highlighted in the folder navigation pane in the image below).

<img width="1152" alt="Screenshot 2022-07-26 at 16 50 10" src="https://user-images.githubusercontent.com/105723324/181052433-fbe8e9ae-470e-40af-b5cb-be3c3147525f.png">

```diff
- NOTE : MAKE SURE TO STORE AND LOAD EVERYTHING IN AND FROM THE SAME DIRECTORY, OTHERWISE THE PROGRAM WILL SHOOT AN ERROR
```

# Navigating the Jupyter Notebook #

## Executing Code Cells ##

Now that you have opened the Jupyter Notebook, you can run each chunk of code sequentially.

Just to avoid any errors, it is highly recommended to work on the code chunks in the order they are in, otherwise, the project will lead to errors. 

```diff
- Not running the code sequentially will result in error and you won't get the desired output.
```
To execute a code block, ensure it is selected by clicking on the space on the left hand side of the block (a narrow blue bar will be displayed nex tto the block when it is selected)

<img width="1112" alt="Screenshot 2022-07-26 at 16 36 22" src="https://user-images.githubusercontent.com/105723324/181049101-8c171eb6-3784-45d2-8e36-3972633ff063.png">

When the block is selected, either press ``` Shift + Enter ``` or you can press <img width="58" alt="Screenshot 2022-07-26 at 16 41 11" src="https://user-images.githubusercontent.com/105723324/181049931-b24fcb07-5612-401f-b1c0-d670c5b70b13.png"> this run button on the navigation pane on the jupyter notebook page.

<img width="1146" alt="Screenshot 2022-07-26 at 16 39 58" src="https://user-images.githubusercontent.com/105723324/181050288-7250587b-0f86-4d62-b6a0-f580a989a3fe.png">

## Long-running code cells ##

Apart from the package installation, note that some of the code cells in this notebook take a relatively long time to execute. In each case these cells will be preceded with a Comment saying: 

```diff
-WARNING! Running the following cell may take a very long time...
```

## Dataset ##

The dataset consists of 1376 images with 194 images containing images of people wearing masks and 194 images with people without masks and has been downloaded from [Face Mask Dataset](https://data-flair.training/blogs/download-face-mask-data/)

You can either download the dataset from [here](https://data-flair.training/blogs/download-face-mask-data/) or from the Repository.

## Installing packages ##

The project requires a lot of packages that takes time to install and load and are not installed in basic download/installation of python.

You can directly download the packages from the first code block of the project that talks about importing the packages. 

```python
import numpy as np
import keras
import keras.backend as k
from keras.layers import Conv2D,MaxPooling2D,SpatialDropout2D,Flatten,Dropout,Dense
from keras.models import Sequential,load_model
from keras.optimizers import Adam
from keras.preprocessing import image
import cv2
import datetime
import tensorflow as tf
import matplotlib.pyplot as plt
```


*Note : For the haarcascade_frontalface_default.xml, if your system doesn't have it installed post the installation of OpenCV, you can either download it from the repository or [here](https://github.com/kipr/opencv/blob/master/data/haarcascades/haarcascade_frontalface_default.xml)*


## Results ##
After successfully creating a model trained by the dataset, we were able to get 97% accuracy in detecting if a person is wearing a mask or not in real-time.
As the image below shows, You should be able to detect whether a person in frame is wearing a face mask or not in real-time environment using your web-camera. (As you can see the time-stamp mentioned on the frame as well)

![Mask-Collage](https://user-images.githubusercontent.com/105723324/181061983-fe28304e-04f9-485c-9df7-8f6b8c22cd9a.jpg)

## Conclusion ##

In this work, a deep learning-based approach for detecting masks over faces in public places to curtail the community spread of Coronavirus is presented. The proposed technique efficiently handles occlusions in dense situations by making use of an ensemble of single and two-stage detectors at the pre-processing level. The ensemble approach not only helps in achieving high accuracy but also improves detection speed consider- ably. Furthermore, the application of transfer learning on pre-trained models with extensive experimentation over an unbiased dataset resulted in a highly robust and low-cost system. The identity detection of faces, violating the mask norms further, increases the utility of the system for public benefits.

Finally, the work opens interesting future directions for researchers. Firstly, the proposed technique can be integrated into any high-resolution video surveillance devices and not limited to mask detection only. Secondly, the model can be extended to detect facial landmarks with a facemask for biometric purposes.
