# Install and Publish

## Introduction

This guide show how to install `Primavera Sound 2013 Schedule` in your system.
There are two ways: 

  * *setupTools*
  * *EasyInstall*

## Requirements

* Python 2.7.x
* SetupTools
* EasyInstall

## setupTools

Install python application using **setupTools** configuration and publish to the world.
  * Configure `setup.py` file.
  * Register in http://pypi.python.org.
  * Create a `.pypirc` file with user and password from pypi.
  * Introduce next commands in application base directory:

```shell
sudo python setup.py install
sudo python setup.py register
sudo python setup.py sdist upload
sudo python setup.py bdist upload
```
  * Go to yout profile in pypi and you can see you package.

## EasyInstall

Using `easy_install` command you can install every application published in pypi.

To install this project you have to use the command:

```shell
easy_install primaverasound_2013
```

Now you can use `retrieve_schedule.py` script in your computer as a new command.

## Information

* *SetupTools*: Install packages - http://packages.python.org/an_example_pypi_project/setuptools.html
* *CheeseShop*: Install packages and versions - http://wiki.python.org/moin/CheeseShopTutorial

