# DataScience-Python-Basics

26-Nov-2020

Conda commands:

1. conda create -n <name_of_env> Python=3.6
    it will create a new folder for each env. with the mentioned version.

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


