# ADT Tutorial 1 - Create an ADT for a Wordpress Application

    1. The user has a Wordpress application (Docker image avaliable in public docker hub)
    2. The user would like to deploy the application on the Cloudbroker platform
    3. The user want to apply auto scaling policy by monitoring CPU usage

This application deploys a wordpress blog, complete with MySQL server and a Network File Share for peristent data storage.

#### Step 1: Search ADT for similar wordpress application in the ADT repository.

    Search Keywords: 
        APP_Keywords+wordpress+docker
    Query:
        https://github.com/hkchen-uow/MiCADO-ADT-REPO/search?q=APP_Keywords%2Bwordpress%2Bdocker&unscoped_q=APP_Keywords%2Bwordpress%2Bdocker
    Results:
        ADT/tests-demos/wordpress.yaml
        ADT/prototypes/21-wordpress-hkn.yaml

The user find the ADT (ADT/tests-demos/wordpress.yaml) could be used for his Wordpress application.

And follow the tutorial in 

https://micado-scale.readthedocs.io/en/latest/tutorials.html#wordpress

to modify the ADT for his Wordpress application.

However, the default ADT is deployed in the CloudSigma cloud. While the user need to deploy his application in the CloudBroker cloud instead.

#### Step 2: Search Node_Example for Cloudbroker deployment

    Search Keywords
        NE_Type+Cloudbroker
    Query
        https://github.com/hkchen-uow/MiCADO-ADT-REPO/search?q=NE_Type%2BCloudbroker&unscoped_q=NE_Type%2BCloudbroker
    Results:
        node_example/Occopus/cloudbroker.yaml

The user replace the default CloudSigma deployment with CloudBroker deployment by using the Node_Example template.

However, the default ADT use Network based scaling policy. While the user would like to use CPU based scaling policy instead.

#### Step 3: Search Node_Example for CPU Scaling policy

    Search Keywords:
        NE_Type+Policy+Scaling+CPU
    Query:
        https://github.com/hkchen-uow/MiCADO-ADT-REPO/search?q=NE_Type%2BPolicy%2BScaling%2BCPU&unscoped_q=NE_Type%2BPolicy%2BScaling%2BCPU
    Results:
        node_example/policies/application_d_vm_cpu_scaling.yaml
        node_example/policies/application_a_container_cpu_scaling.yaml
        node_example/policies/application_d_container_cpu_scaling.yaml
        node_example/policies/application_a_vm_cpu_scaling.yaml
        node_example/policies/application_s_vm_schedule_scaling.yaml
        
The user replace the default Network based scaling policy with the CPU based scaling policy by using the Node_Example template 