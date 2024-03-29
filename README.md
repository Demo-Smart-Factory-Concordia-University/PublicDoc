# PublicDoc
Public documentation about the Demo-Smart-Factory at Concordia University.

This demo factory is part of the Gina Cody School research center for Advanced Manufacturing and is operated by the 
[Electrochemical Green Engineering Group](http://ege.encs.concordia.ca)

## General concept

Various manufacturing technologies are assembled in this demo factory. Data exchange is taking place using a publish-subscribe paradigm and is implemented with an Apache Kafka server.

![General Concept](images/GeneralConcept.png)

Data collection uses the MTConnect standard to represent manufacturing data. 
* Streaming [MTConnect](https://www.mtconnect.org/) data to [Kafka](https://kafka.apache.org/) is performed using the [python-mtc2kafka](https://github.com/rwuthric/python-mtc2kafka) library.
* MTConnect agents are implemented using the [MTConnect C++ Agent](https://github.com/mtconnect/cppagent)
* MTConnect adapters are implemented using the [GECO library](https://github.com/EGE-Group-Concordia-University/geco)

![Data Flow](images/DataFlow.png)

## Generic equipment deployment
All the infrastructure follows the principle of Infrastructure as Code (IaC). Deployment is done using docker and docker-compose on various virtual machines. Docker swarm is used as orchestrator.

![Generic deployment](images/GenericEquipmentDeployment.png)

## Access
Members of the project have access through our dedicated JupyterHub server.
