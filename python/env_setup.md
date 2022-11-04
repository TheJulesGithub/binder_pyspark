Welcom to this Spark course. 
--------------------------------

@Author: jules-edouard.denis@airbus.com
Novembre 2022

# Introduction

This course is a practical work on Spark. It is based on `pyspark` tool (Python Spark).

* Thirst, you will work on your PC (in "local") with very simple toy case based on a `jupyter notebook` user friendly interface (TP 1)
* Then (TP 2) you will dig in technical concepts (also on `jupyter-notebook` interface)
* Finaly (TP 3) we will script a bit, and use a consola to run your spark jobs.

# Environement set-up

First you need to set up an environment.

Requirements:
* Java :
	* https://javadl.oracle.com/webapps/download/AutoDL?BundleId=247134_10e8cce67c7843478f41411b7003171c
	* https://stackoverflow.com/questions/10891405/installing-jdk-without-administrator-privileges to install it without admin rights
	* Make sure you set your JAVA_HOME env variable
		* On windows : `SETX JAVA_HOME "path\of\java"` (`where java` to know what is the correct path)
* An internet connexion
* Miniconda (Windows) (or Anaconda) installed:
		* If not installed, please, see: https://docs.conda.io/en/latest/miniconda.html#latest-miniconda-installer-links
* Pyspark


## Environment set-up (Windows)

1. If not installed, install miniconda (https://docs.conda.io/en/latest/miniconda.html#latest-miniconda-installer-links).

2. Create a "virtual environment", it is an isolated Python installation. You can install anything on it (even break it) without any consequence on your base Python installation (because it's wipeable).

Open an anaconda prompt (Researcj bar > anaconda prompt)

```
# Create a virtual environment
conda create -n spark_env -y

# Activate environement
conda activate spark_env

# Install packages
conda install pyspark -y
# (-y to avoid user accept message)

conda install jupyter -y
conda install -c conda-forge findspark -y
```

Your install is now clean :)

## Set up (Linux)

1. Verify Python is installed on your PC (a priori yes):
	* Open a prompt
	* Commad:

```
python --version
```

Your version shall be at least version 3.

2. Set up environement

In your terminal:

```
# Install tool to enable virtual environment on linux
pip install virtualenv

# Create virtualenv
virtualenv spark_env

# Activate your virtualenv
source  activate spark_env/bin/activate.sh

# Install requirements
pip install pyspark
pip install jupyter
```
Your install is now clean :)

Do not close the prompte !

## Excercise

For the two first BE, we will work on a user friendly coding interface (`jupyter notebook`).

On your (still opened) terminal:

```
jupyter-notebook
```

NB:
* If you close your terminal when jupyter is running, you will loose your work (!)
* If you (accidentally) close your terminal after install, don't worry:

Open a new on, and:

Windows:
```
# Activate environement
conda activate spark_env
```

Linux:
``` 
# Activate your virtualenv
source activate spark_env/bin/activate.sh
```

