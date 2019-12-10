## =====
## SETUP
## =====

## Azure Services Setup

Create the following resources in your subscription's resource group:

USE A PREFIX FOR ALL RESOURCES:
- 3 letters, first letter of first name + first two letters of last name
- ex: John Doe --> jdo

REPLACE jdo below with your personal prefix to avoid conflicts for resources which are part of URIs:

    Storage Account:            jdoailabsa
	Cognitive Services:         jdoailabcs
	Machine Learning Workspace: jdoailabsml
    Cosmos DB:                  jdoailabscdb

## Storage Account post service creation setup

Create the following containers:
- images
- classification --> copy the light_bulbs folder in this container
- automl --> copy the automl folder content in this container

NOTE: You can use the Azure Portal or Azure Storage Explorer to copy the data

## Cosmos DB post service creation setup

Create a database w/ container:
- type 'Core SQL'
- database id: ailab
- container id: images
- partition key: /id


## ======
## LAB #1
## ======

## End-to-end solution to automatically detect insulators from aerial images and report the location of each insulator within an image into a Cosmos DB image metadata repository with Power BI visualization

Instructions: instructor led
Demo code cheat sheet:
- ai-lab-custom-vision repo
- NOTE: build from scratch and copy some of the reference code when prompted by instructor

## ======
## LAB #2
## ======

## Azure ML Deep Dive and Hands-on
## Creation of a complete solution with crowd sourced image tagging to train a custom ML image classification model and deploy as an auto scale API

Instructions: instructor led
Demo code cheat sheet:
- ai-lab-ml repo
- NOTE: to be leveraged when prompted

## LAB Coverage
- Azure ML Overview
- Managing Compute Resources
- Managing Datastores and Datasets
- multiple ways to Author ML
  - UI Designer
  - Automated ML
  - Notebooks or local python code: going over some sample examples to understand the Azure ML SDK integration
- The ML Platform supporting all the orcherstation and deployment
  - Experiments
  - Pipelines
  - Models
  - Endpoints

## Lab Exercises

ML with the Designer: model, train, deploy as real time or batch endpoints
ML with Auto ML: run models, deploy as endpoints
ML with Notebooks: creating a custom classification model for Defect Detection
- Leveraring Data Labeling
- Exporting a Labeled Data Set
- Training from the Labeled Data Set (code/debug small, then train at scale)
- Deploying as a Web Service