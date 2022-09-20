# Python Best Practices

## Virtual Environments 
### What is a virtual environment?
When coding with Python, it is the norm to download packages and to use the code from these packages. You probably do this the whole time. For example: `pip3 install python-opencv`
Virtual Environments keep **all of your packages in one place** (which will generally be in the folder you're working in). 

### When should you use a virtual environment?
As a general rule of thumb, you **should create a new virtual environment for each project** you're working on. 

### Why use a virtual environment?
When you install a package **without** a virtual environment you are installing it **systemwide**. This can be problematic for a couple of reasons:
1. you may need different versions of a package for two different projects
2. when you want to share your code or run your code on a different machine, you won't actually have all the packages in one place

### How do you create a virtual environment?
Using the venv or virtualenv package. Both are virtually interchangeable
#### Mac or Linux 
##### Create Virtual Environment
If you haven't already, create a folder for your project
`mkdir my_project`
Change into your project folder
`cd my_project`
create the virtual environment
`python3 -m venv <name of virtual environment>`
or
`python3 -m virtualenv <name of virtual environment>`
#### Activate Virtual Environment
For the sake of this example, lets say I have named my venv `myvenv`
`source myvenv/bin/activate`
now your shell should have the name of your venv on the left of each line
e.g.
`(myvenv)$`

#### Windows
##### Create Virtual Environment
If you haven't already, create a folder for your project
`mkdir my_project`
Change into your project folder
`cd my_project`
create the virtual environment
`python -m venv <name of virtual environment>`
or
`python -m virtualenv <name of virtual environment>`
#### Activate Virtual Environment
`myvenv/bin/activate`
now your shell should have the name of your venv on the left of each line
e.g.
`(myvenv)$`

#### Install Packages
`pip install <package-name>`
or install a **specific version of a package**. This is a very important use of virtual environments!
`pip install django==2.2.26`

#### Check what packages you have installed
`pip list`

#### Remove a package
`pip uninstall <package-name>`
e.g.
`pip uninstall numpy==1.18.0`

#### Deactivate virtual environment
`(myvenv)$ deactivate`

### Use a virtual environment with a Jupyter Notebook
#### install ipykernel
make sure your virtual environment is active
e.g. `source myenv/bin/activate`
then install the ipykernal package
`pip install ipykernel`
#### Create a new kernel for your Jupyter Notebook
`ipython kernel install --user --name=projectname
