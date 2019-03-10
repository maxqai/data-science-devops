Author: Nikolay Borissov, borissov@hotmail.de

Structuring Data Science Projects
====================

Inspired by [Reproducible Science](https://github.com/mkrapp/cookiecutter-reproducible-science) and favouring the philosophy of [Cookiecutter Data Science](https://github.com/drivendata/cookiecutter-data-science),
this project provides a more software engineering oriented structure for data science projects including scripts for automated and reproducable builds using modern tools like docker-compose, docker and make for 
simplifying the build and run commands. 

Requirements
------------
* Install `cookiecutter` by executing: `pip3 install cookiecutter`
* Install [docker](https://www.docker.com)

Usage
-----
To start a new science project:
 
* git clone https://github.com/maxqai/structuring-datascience-projects.git
* cookiecutter cookiecutter-reproducible-science

or

* cookiecutter https://github.com/maxqai/structuring-datascience-projects.git

Project Structure
-----------------

```
├── AUTHORS.md
├── docker-compose.yml <- Builds and runs docker images
├── LICENSE
├── Makefile           <- Simple commands on top of docker-compose
├── README.md
├── bin                <- Compiled model code can be stored here
├── config             <- Configuration files, e.g., for your model if needed
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
├── docker             <- Contains docker files      
├── docs               <- Documentation of project
├── notebooks          <- Ipython or R notebooks
├── reports            <- Any project reports
│   └── figures        <- Figures of reports
├── requirements       <- Contains requiremenents.txt for pip installer 
├── src                <- Source code for this project
│   ├── data           <- scripts and programs to process data
│   ├── external       <- Any external source code, e.g., pull other git projects, or external libraries
│   ├── models         <- Source code for your own model
│   ├── tools          <- Any helper scripts go here
│   ├── visualization  <- Scripts for visualisation of your results, e.g., matplotlib, ggplot2 related.
│   └── webapp         <- Contains webapp code 
├── tests              <- Contains test code 

```

Running the container
---------------------

Using Makefile on top of docker-compose to simplify building and running docker containers.

Build the container and start a Jupyter Notebook server

* make notebook 

Build the container and start IPython shell

* make ipython

Build the container and start a bash

* make bash

Prints available make commands

* make help

License
-------
This project is licensed under the terms of the [Apache 2.0](/LICENSE)
