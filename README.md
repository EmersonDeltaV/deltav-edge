# DeltaV Edge Environment

The DeltaV Edge Environment is a platform that provides easy and secure access to DeltaV system data for on-premise use or in the cloud for monitoring, analytics, reporting or for other Enterprise applications.

![DeltaV Edge Environment](./images/deltav-edge-architecture.png)


### Secure Access to DeltaV System Data

Accessing plant data from a Distributed Control System such as DeltaV, can be a very complex task.
Data resides down in the Control Network and thus bringing it outside to the Enterprise network requires multiple layers of secure processing.  
The DeltaV Edge Environment simplifies data access to plant data by handling all of the security transfer from across the different network layers.  

### Data Contextualization

Extracting control system data often strips away valuable information about relationships between data points – information that exists natively within control system configurations. This loss of embedded context makes it hard to understand how the data relates to the real-world process.

DeltaV Edge Environment also manages the contextualization of data coming from the Control Network instead of by relating it to where it is being used, instead of simply presenting raw data values.  

### Easy Application Deployment 

The DeltaV Edge Environment also provides a common application platform that makes this contextual set of data available via industry standard protocols such as OPC UA and REST API, thus allowing more data consumption options through third-party applications such as Grafana, Node-RED, and JupyterLabs Notebook.  


_The intent of this github page is to provide sample code, guides, and software development kits to encourage non-Emerson developers to create their own applications that can unlock the potential of having access to such wealth of plant data, such as data analytics, graphical representation, etc._


Application Development features include:

-	Contextualized data available via OPC UA and REST API.
-	Online Cloud orchestration of Edge Nodes and Applications
-	Easy application management via Docker containers and Virtual Machines.


DeltaV Edge Environment makes the data readily accessible to the user via industry standard REST API and OPC UA endpoints. 


REST (REpresentational State Transfer) API is a web service that is based on HTTPS and provides data in JSON format, which is compatible with numerous modern data analytics applications, such as Grafana, Jupyter Notebook, Node-RED, Power BI, Excel, etc.

The OPC Unified Architecture (OPC UA) interface is a cross-platform, open-source, standard for data exchange for industrial applications.  Data accessed via OPC UA  is managed via an OPC UA Client (e.g. UaExpert, Integration Objects) connected to the DeltaV Edge Environment OPC UA endpoints.

|  <img src="./images/rest-api.png" width=425> | <img src="./images/opcua.png" width=425> |
|------|------|
| <p align="center"> [REST API](developer-guide/rest-api/rest-api.md) </p>|<p align="center"> [OPC UA](developer-guide/opc-ua/opc-ua.md) </p>| 


### Use with Third Party Open Source Applications:

| <p align="center"><img src="./images/Grafana.png" width=275></p> | <p align="center"><img src="./images/Node-RED.png" width=275></p> | <p align="center"><img src="./images/JupyterNotebook.png" width=275></p> |
|---|---|---|
| <p align="center">**Grafana**  </p> | <p align="center">**Node-RED**  </p> | <p align="center"><a href="https://github.com/EmersonDeltaV/jupyter-labs-for-edge">**Jupyter Notebook**</p> |


https://github.com/EmersonDeltaV/jupyter-labs-for-edge

### Connect to Commercial Applications:

| <img src="./images/power-bi.png" width=80> | <img src="./images/microsoft-excel.png" width=100> | 
|----------|----------|
| [Power BI](developer-guide/power-bi/power-bi.md)  | [Microsoft Excel](developer-guide/microsoft-excel/microsoft-excel.md)   |


## Getting Started

To get you started, here are additional info on Edge functionality, sample guides, and repositories:

-	[delta-edge-sdk](https://github.com/EmersonDeltaV/deltav-edge-sdk)
-	[simple-dockerapp-dotnet6](https://github.com/EmersonDeltaV/simple-dockerapp-dotnet6)
-	[Vincent's code](https://8b1e38e9-9001-4711-950c-437a4310f80d.mock.pstmn.io)
-	_Richard's code_


### In-depth [Developer Guide](./developer-guide/developer-guide.md) covering:
 
- DeltaV Edge Envirorment Architecture and System Components
  
- Types and Categories of data being gathered
  
- Accessing Data via REST API
  
- Accessing Data via OPC UA
  
- Connecting to commercial applications (e.g. Power BI, Excel)
  
- Connecting to Third Party Applications within Edge Environment (e.g. Grafana, Node-RED, JupyterLabs Notebook)
  
- Creating Edge Applications in Edge App Marketplace

## Components

|  <p align="center"><img src="./images/data-provider.png" width=275></p>| <p align="center"><img src="./images/edge-node.png" width=275></p> | <p align="center"><img src="./images/edge-orchestration.png" width=275></p> | <p align="center"><img src="./images/data-diode.png" width=275></p> |
|---|---|---|---|
|  <p align="center"><a href="">**Data Provider**</p>| <p align="center"><a href="">**Edge Node**</p> | <p align="center"><a href="">**Edge Orchestration**</p> |<p align="center"><a href="">**Data Diode**</p> |

## Version 1.0 Specifications

|Specification|Description|
|---|---|
| Compatibility | DeltaV v14.LTS, v14.FP1, v14.FP2, v14.FP3, and v15.LTS |
| Number of Supported Data Items | 20k, 100k, 300k |
| Supported Sampling Periods | 1s, 2s, 5s, 10s, 60s |
| Alarms and Events Handling | 100 events/second, 4K peak alarm burst handling |
| Data Types Supported | DeltaV S88 Plant Hierarchy, Configuration Data, Process Values, Alarms & Events, SIS Module Data |
| Store and Forward | Buffers data up to 48 hours |

## Additional Resources 

* [DeltaV Edge Environment Product Page](https://emerson.com/deltavedge)
* [DeltaV Edge Environment Product Data Sheet](https://www.emerson.com/documents/automation/product-data-sheet-deltav-edge-environment-deltav-en-9573950.pdf)
* [DeltaV Edge Environment Solution and Architecture Overview](https://www.youtube.com/watch?v=DKLijP0tvzc)

## Contributing

This project welcomes contributions, suggestions, and feedback. All contributions, suggestions, and feedback you submit are accepted under the Project's license. You represent that if you do not own copyright in the code that you have the authority to submit it under the Project's license. All feedback, suggestions, or contributions are not confidential.

For more information on how to contribute to DeltaV Edge Environment, please read [CONTRIBUTING.md](CONTRIBUTING.md]).


## References
- EDGE is based on eve-os [v9.4.6-lts](https://github.com/EmersonDeltaV/lf-edge-eve)
