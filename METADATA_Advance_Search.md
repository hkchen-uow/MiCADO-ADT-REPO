# MiCADO: METADATA Ontology for TOSCA Repository & Use Cases

##This repository holds the TOSCA related material developed as a part of the [COLA Project](https://project-cola.eu/)
------------
### ADT/
###### Application Description Templates are kept here
These templates describe the application topology and policies for COLA use-cases. They are submitted to the toscasubmitter component in MiCADO to deploy applications to the cloud.

There are mainly two types of ADT:
* *prototypes/*

   Live application's ADTs are kept here.

* *tests-demos/*
    
   Tests/Demos ADTs are kept here
    
ADT METADATA:

    * *ADT_Status*: Is the template ready to be submitted to the toscasubmitter component?, 
                    1. True
                    2. False.
    * *ADT_Type*: The type of ADT, 
                  1. Prototypes : Live application's ADTs are kept here. The ADT is ready to be submitted to the TOSCASubmitter.
                  2. Tests/demos : Tests/Demos ADTs are kept here, please check the ADT_Status.
    * *ADT_Description*: ADT description.
    * *APP_Name*: Application name.
    * *APP_Keywords*: List of application keywords.
    * *APP_Deployment*: List of deploment methods use in the ADT, e.g. VM, Docker Container
    * *APP_Version*: Application version.
    * *APP_Policies*: List of policy types uses in the ADT:
                      1. Monitoring
                      2. Scaling
                      3. Network
                      4. Security
    * *POLICY_Keywords*: List of keywords related to the policies. 
     


### node_example/
###### node_example definitions are kept here
There are three types of node_example:
* *applications/*

   The *application* node examples are kept here
   
* *Occopus/*

   The *Occopus* node examples are kept here
    
* *policies/* 
   
   The *policies* node example are kept here
   
Node Example Metadata
    
    * *NE_Type*: Type of the Node Example,e.g. application, occopus, policies. Sub-type,e.g. Monitoring, Scaling, Network and Secret, 
    * *NE_Name*: The name of the node example.
    * *NE_Keywords*: List of keywords for search, e.g. Basic, CPU, Memory, Deadline, Optimizer ……
    * *NE_Version*: Node example version.
    
------------
#### Use Cases

Github provide an advance search function 
(https://github.com/search?q=ADT+repo%3Ahkchen-uow%2FMiCADO-ADT-REPO&type=Code&ref=advsearch), 
which allow ADT developers to search ADT by queries. Here are some typical use cases and relevant queries:


1. I would like to find all the prototype ADT.
    
    ```
    https://github.com/hkchen-uow/MiCADO-ADT-REPO/search?q=in:path+ADT/prototypes/
    ```
2.	I would like to find all the test/demo ADT.

    ```
    https://github.com/hkchen-uow/MiCADO-ADT-REPO/search?q=in:path+ADT/tests-demos/
    ```
    
3.	How can I find the ADT for an application named “repast”?

    ```
    https://github.com/hkchen-uow/MiCADO-ADT-REPO/search?q=APP_Name&repast
    ```
4.	How can I find the ADT with a keyword “azure”?

    ```
    https://github.com/hkchen-uow/MiCADO-ADT-REPO/search?q=APP_Keywords&Azure
    ```
5.	How can I find the ADT for an application named “repast” with a “prototype” type?
    
    ```
    https://github.com/hkchen-uow/MiCADO-ADT-REPO/search?q=ADT_Type&Prototypes&APP_Name&repast
    ```
6.	I would like to find some application examples to construct an ADT.
    
    ```
    https://github.com/hkchen-uow/MiCADO-ADT-REPO/search?q=in:path+node_example/applications/
    ```
    
7.	How can I find the application examples for application named “application example a”?
    
    ```
    https://github.com/hkchen-uow/MiCADO-ADT-REPO/search?q=NE_Name%26application+example+a
    ```
    
8.	I would like to find some Occopus examples to construct an ADT.
    
    ```
    https://github.com/hkchen-uow/MiCADO-ADT-REPO/search?q=in:path+node_example/Occopus/
    ```
    
9.	How can I find the Occopus examples for deployment in “ec2”?
    
    ```
    https://github.com/hkchen-uow/MiCADO-ADT-REPO/search?q=NE_Keywords%26ec2
    ```
    
10.	I would like to find some policy examples to construct an ADT.
    
    ```
    https://github.com/hkchen-uow/MiCADO-ADT-REPO/search?q=in:path+node_example/policies/
    ```
    
11.	How can I find all the policy examples for application named “application example a”?
    
    ```
    https://github.com/hkchen-uow/MiCADO-ADT-REPO/search?q=NE_NAME%26application%2Bexample%2Ba+in%3Apath%2Bnode_example%2Fpolicies%2F
    ```
which is deployed as VM/container

    https://github.com/hkchen-uow/MiCADO-ADT-REPO/search?q=NE_Type%26application%26application+example+a%26vm

with “cpu_scaling”

    https://github.com/hkchen-uow/MiCADO-ADT-REPO/search?q=NE_Type%26application%26application+example+a%26vm%26cpu+scaling