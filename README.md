# binder_pyspark
A binder for Pyspark.

## About MyBinder

MyBinder (https://mybinder.org/) permits to run jupyter notebooks (in fact any type of code) online. It's like google colab (https://colab.research.google.com/), but it enable any type of environment (python, java, ...). [here](https://mybinder.org/v2/gh/apache/spark/fbbcf9434a?filepath=python%2Fdocs%2Fsource%2Fgetting_started%2Fquickstart_df.ipynb) is an example of MyBinder (open access) jupyter notebook (source: Pyspark documentation).

It is especially usefull when your environement is cross language (like pyspark, which need also java.)

It is based on docker images builded from github repositories. 
A you can see, the configuration files needed (see `binder/` dir) are very light.

Here, I used config files from the apache Spark github page (https://github.com/apache/spark), especially content of `binder` dir:
* `apt.txt` list all system requirement (here java)
* `postBuild` is a script file (bash) launch after apt, it concist in running all the `pip install` requested (e.g. `pip install pyspark`).


## How to start ?


1. Go to MyBinder: https://mybinder.org/

2. Fill the form:
* GitHub repository name or URL: https://github.com/TheJulesGithub/binder_pyspark
* Git ref (branch, tag, or commit): main
* Path to a notebook file (optional): binder_pyspark/python/BE_1_introductions.ipynb

3. Click on launch

4. Test URL
Here is the optained URL: https://mybinder.org/v2/gh/TheJulesGithub/binder_pyspark/main?labpath=python%5CBE_1_introductions.ipynb

## Usefull documentation

Doc MyBinder: https://mybinder.readthedocs.io/en/latest/introduction.html

## Code troubleshooting

*Manage git credentials on windows*:
We strongly advise to use SSH clone on Windows (you need then to generate a key with gitbash) > avoid password issue gitBash UX (bug).