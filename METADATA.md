# MiCADO: METADATA Ontology for TOSCA Repository & Use Cases

##This repository holds the TOSCA related material developed as a part of the [COLA Project](https://project-cola.eu/)
------------
### ADT/
###### Application Description Templates are kept here
These templates describe the application topology and policies for COLA use-cases. They are submitted to the toscasubmitter component in MiCADO to deploy applications to the cloud.

There are mainly two types of ADT:
* *prototypes/*

    Live application's ADTs are kept here.The ADT name standard format is constructed using the following Metadata:
    
    * *APP_ID*: Unique ID for the APP.
    * *APP_Name*: Application name.
    * *APP_Keywords*: List of application keywords.
    * *APP_Version*: Application version.
     
* *tests-demos/*

    Tests/Demos ADTs are kept here

### node_example/
###### node_example definitions are kept here
There are three types of node_example:
* *applications/*
    
   The *application* node example name standard format is constructed using the following Metadata:
   
    * *APP_ID*: Unique ID for the APP.
    * *APP_Name*: Application name.
    * *APP_Keywords*: List of application keywords
    * *APP_Version*: Application version.
    
* *Occopus/*

    The *Occopus* node example name standard format is constructed using the following Metadata:
    
    * *PROVIDER_NAME*: The name of the cloud provider.

* *policies/*
    
    The *policies* node example name standard format is constructed using the following Metadata:
    
    * *APP_ID*: Unique ID for the APP.
    * *APP_Name*: Application name.
    * *APP_Deployment*: The deployment type of the application, e.g. VM or container
    * *Policy_Type*: Type of the policy, e.g. Monitoring, Scaling, Network and Secret.
    * *Policy_Name*: The name of the policy.
    * *Policy_Keywords*: List of policy keywords, e.g. Basic, CPU, Memory, Deadline, Optimizer ……
    * *Policy_Version*: Policy version.
    
------------
#### Use Cases

Github provide a simple text search function (https://github.com/hkchen-uow/tosca/find/METADATA), 
which allow ADT developers to search ADT by queries. Here are some typical use cases and relevant queries:


1. I would like to find all the prototype ADT.
    
    ```
    ADT/prototypes
    ```
2.	I would like to find all the test/demo ADT.

    ```
    ADT/tests-demos
    ```
    
3.	How can I find the ADT for an application named “repast”?

    ```
    ADT/repast
    ```
4.	How can I find the ADT with a keyword “cloudbroker”?

    ```
    ADT/cloudbroker
    ```
5.	How can I find the ADT for an application named “repast” with a “prototype” type?
    
    ```
    ADT/prototypes/repast
    ```
6.	I would like to find some application examples to construct an ADT.
    
    ```
    node_example/applications
    ```
    
7.	How can I find the application examples for application named “application_example_a”?
    
    ```
    node_example/applications/application_example_a
    ```
    
8.	I would like to find some Occopus examples to construct an ADT.
    
    ```
    node_example/Occopus
    ```
    
9.	How can I find the Occopus examples for deployment in “ec2”?
    
    ```
    node_example/Occopus/ec2
    ```
    
10.	I would like to find some policy examples to construct an ADT.
    
    ```
    node_example/policies
    ```
    
11.	How can I find all the policy examples for application named “application_a”?
    
    ```
    node_example/policies/application_a
    ```
which is deployed as VM/container

    node_example/policies/application_a_vm

with “cpu_scaling”

    node_example/policies/application_a_vm_cpu_scaling
