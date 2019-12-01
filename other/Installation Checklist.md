# Installation and Setup Checklist

This is a checklist to confirm that your laptop is set up properly for DCS 210. If at any point you get an error message, please note the error message and we will help you to fix it! 
If you don't get any error messages, you are properly set up.

Please post a message in the "setupchecklist" channel in Slack once you have walked through the entire checklist. That way, we will know whether or not we need to follow up with you.

## Install

### Anaconda
* Install the [Anaconda distribution](http://continuum.io/downloads) of Python 3.7x. This is a good installation guide [here](https://www.datacamp.com/community/tutorials/installing-anaconda-windows) 
you should read first for the basics. The videos below are OS specific and very much woth watching!
	* For Windows, go [here](https://www.youtube.com/watch?v=dgjEUcccRwM); he has a blog post [here](https://medium.com/@GalarnykMichael/install-python-on-windows-anaconda-c63c7c3d1444) as well.
	__NOTE__: Be sure to set you path in the command prompt
	* For Mac, go [here](https://www.youtube.com/watch?v=YJC6ldI3hWk)

### Github

* Create a [GitHub](https://github.com/) account.

### Slack
* For Windows: https://slack.com/downloads/windows
* For Mac: https://slack.com/help/articles/207677868-download-slack-for-mac#app-store-1


## Verify

### Launch Anaconda Navigator  
<img src="../images/anaconda.png" width = "10%">
	
You should see, at a minimum, the following packages installed:
* Sypder
* Juypter Notebook

<img src="../images/anacondaNavigator.JPG" width = "20%">

Launch Juypter Notebook 
This is a hosted application and will open in your default browser. You will not see the folders as in the image but will be creating some of your own

<img src="../images/jnb.JPG" width = "20%">


### Anaconda Setup
Because this course must support both Mac OS and Windows, I've settled upon using the Anaconda shell for consistency between both operating systems.
The default shell in all versions of Mac OS is bash. Windows users would typically download something like Cygwin or Git Bash. But since we are 
installing Aanaconda, the Anaconda prompt will provide a common linux environment for both sets of users.

The Anaconda prompt window is both a package manager and environment manager (similar to Python's venv).

#### Open an Anaconda Prompt
## Creating an Environment
* conda create --name mylinuxenv m2-base
* activate mylinuxenv
* deactivate
* OR conda install m2-base (gives you all the coreutils as well as bash - run conda search m2-.* to see them all)

## Anaconda Prompt cheatsheet
* conda info --envs : lists all environments
* source activate <env name> : activate an environment
* source deactivate: deactivate an environment
* conda list : list all packages installed
* conda create --name <env name> python=3 astroid babel : create new environment, specify version of python, and install packages
* WINDOWS NOTE: SOURCE is not recognized. When deactivating and activating in the anaconda command prompt, skip 'source' and just type 'deactivate' or 'activate' depending on what you are trying to do.
* conda env export > environment.yml: export conda environment requirements list to a file
* conda env remove -n ENV_NAME : delete environment

### Python
* Open an Anaconda prompt window:
    * Type `conda list` 
    * Type `python` to open the Python interpreter (the prompt should look like >>>)
* While in the Python interpreter:
    * Look at the Python version number. It should start with 3.7.
    * Type `import pandas`
    * Type `exit()` to exit the interpreter. You can now close the command line application.

### Slack
* slack me with success or issue!