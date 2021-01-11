# DataScience-Python-Basics

26-Nov-2020

Conda commands:

```
1. conda create -n <name_of_env> python=3.6

// it will create a new folder for each env. with the mentioned version.

2. conda info --envs
// This will list all envs

3. conda activate <env_name>
// to activate that virtual env

4. conda deactivate

// to exit/deactivate the env

```

In real time, we'll use anaconda only in servers for development, for deployment we'll use docker.

In anaconda, we use conda commands. In docker, we use "pip commands" for installing Python packages.

PIP: python installer packages

In docker, we use small OS unlike Anaconda.

Eg: Dockerfile

```
FROM python:3.6-slim-stretch
RUN apt-get -y update && apt-get install -y --no-install-recommends \ 
    nginx \
    ca-certificate \
    g++ \
    && rm -rf /var/lib/apt/lists/*

ENV PYTHONUNBUFFERED= TRUE
ENV PYTHONDONTWRITEBYCODE= TRUE
ENV PATH = "/opt/program:${PATH}"
COPY model_training /opt/program
WORKDIR /opt/program
RUN /opt/programs
RUN pip3 install -r requirements.txt
RUN rm -rf /root/.cache

```
while deployment, we should be knowing what all we need, otherwise it'll be heavy.

 requirements.txt

```

pandas=0.23.4
matplotlib=3.0.3
scipy=1.2.1
scikit-learn=0.20.1
requests=2.21.0
tensorflow=1.10.0
flask=1.0.2
splunc-hec-handler=1.0.8
schedule=0.6.0
psutil=5.6.1

```
REALTIME
========

Everything is micro service.

When anaconda, when Docker?

we use it for Batch jobs for training our models.
Output of batch is the formula. We publish this as a rest API. The API code is in the docker.

Now, the frontend will talk with docker to access rest API

Frontend ==> docker 

Anaconda is a virtual env which inherits lots of packages.

NOTE: flask (REST API) is an external package that didn't come with Anaconda.

===============================================================

27-nov-2020

If in CLI, if something is not found, do: pip install <name>

Create a folder (new -> folder) in jupyter notebook (in Chrome localhost:8080) and rename it.

REPL => read execute print loop

Python Basics:

Python is a type inference lang. Variable data type depends on the value.

Variables:

a= 10
​
type(a)
int

b="Shubham"
type(b)
str

c= 10.5
type(c)
float

d= input ("Enter a number ")
Enter a number 22
d
​
'22'
# Everything we pass to "input" is treated as a string 








