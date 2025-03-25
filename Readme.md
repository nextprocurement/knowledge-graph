# Next Procurement processing pipeline

In this git is the project for the creation of a pipeline for the processing of public tender data from platforms such as TED and PLACE for its transformation to knowledge graphs. To achieve this, part of the work done in the They Buy For You (TBFY) project has been recovered. 

This process has been completely encapsulated in a docker container. Some of the main values such as pipeline endpoint, API port, etc. can be freely defined in the dokcer-compose.yaml. Other values such as the rules for the network mapping are also easily accessible.

The project has an entrypoint in the form of an API, through which all requests for data processing can be sent, as well as providing the files for processing.

Translated with DeepL.com (free version)

## Installation

The installation previously requires the installation of docker.

```
https://docs.docker.com/compose/install/
```

Once docker is installed, the project is deployed with the command

```bash
docker-compose up --build -d 
```

in the root directory of the project.

## Usage

If the value of the PLATFORM_IP environment variable is not modified, the pipeline will search in localhost for the fuseki service to publish the data, and it will not be deployed if it does not find the service. 

Once successfully deployed, the api interface can be accessed at localhost:5050. There you will find all the information about how to use the API.

## Acknowledgements

This work has received funding from the NextProcurement European Action (grant agreement INEA/CEF/ICT/A2020/2373713-Action 2020-ES-IA-0255).

<p align="center">
  <img src="static/Images/eu-logo.svg" alt="EU Logo" height=100 width="200" style="margin-right: -27px;">
  <img src="static/Images/nextprocurement-logo.png" alt="Next Procurement Logo" height=100 width="200">
</p>
