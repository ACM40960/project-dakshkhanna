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

![image](https://user-images.githubusercontent.com/105723324/181009963-4a07d245-3343-4708-82f2-a219fda88b93.png)

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


I am using Mac here,

**Step 4: Verify Pip Was Installed**

If you opted to install an older version of Python, it is possible that it did not come with Pip preinstalled. Pip is a powerful package management system for Python software packages. Thus, make sure that you have it installed.

To verify whether Pip was installed:

1. Open the Start menu and type "cmd."
2. Select the Command Prompt application.
3. Enter pip -V in the console. If Pip was installed successfully, you should see the following output:

![pip check](https://user-images.githubusercontent.com/105723324/181026361-64100eee-7706-478c-8b41-f7c3c78b6b34.png)


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

User must first install Anaconda according to their system requirements from [Anaconda Iinstallation](https://www.anaconda.com/products/distribution). The instructions to install can be found on [Installation Guide](https://docs.anaconda.com/anaconda/install/#). 

After the installation, open Anaconda Navigator and click Launch on the Jupyter Notebook application.

<img width="1439" alt="Screenshot 2022-07-26 at 15 27 02" src="https://user-images.githubusercontent.com/105723324/181032639-9814bb0f-67c6-4e2b-b10e-879d717abefa.png">

*Note that Jupyter python script as an extension of .ipynb unlike .py for other python scripts. So the user should open the script using Jupyter Notebook.*



