# DeltaV Edge Environment Developer Guide


## DeltaV Edge Environment Architecture

The DeltaV Edge Environment provides access to DeltaV system data through a unified solution architecture while satisfying IT cybersecurity, communications, and application requirements—all without disrupting the DeltaV system. 


![DeltaV Edge Environment Architecture](deltav-edge-architecture.png)

The DeltaV Edge Environment solution consists of four major product components:

-	Data Provider

-	Edge Node 

-	Edge Orchestration 

-	Data Diode (optional)


## Data Provider

The Data Provider resides on a dedicated DeltaV Application Station. It reads alarms and events information, real-time module and function block parameters, and sends all of the data to the Edge Environment on a continuous basis.

<img src="edge-data-provider.png" width=300>

In addition, for configured automatic FHX exports, the Data Provider constantly accesses the latest configuration hierarchy based on the DeltaV configuration file and sends the configuration data to the Edge Environment. The Data Provider also consolidates different data types and streams into one outbound data flow.

You can easily configure the Data Provider to receive alarms and events, subscribe to real- time parameters, and extract DeltaV system configuration. The Data Provider includes a Data Provider Configuration Tool to facilitate the process of defining the desirable parameters for subscription. 


## Edge Node

The Edge Node hosts and executes a series of software applications including data services, interfaces, databases, and analytical applications to create an on-demand digital twin replicating both DeltaV system data and the configuration hierarchy for data contextualization. 



<img src="edge-node.png" width=300>


The Edge Environment’s Edge Data Service receives data from the Data Provider, recognizes the data characteristics, and pushes the data into a specific database or database area. The Edge Environment’s internal database temporarily caches all received data for up to one year. 
 
Both the runtime data and the cached data are accessible through the Edge Environment’s egress interfaces. These interfaces include OPC UA and REST API. The OPC UA server provides access to DeltaV runtime parameters, alarms and events, and cached data and also supports multiple aggregation methods to simplify comprehensive data queries. The Edge Environment’s REST API is a web service that is based on HTTPS and provides data in JSON format.  
 
To easily use data, you can deploy applications in the Edge Environment. For example, in addition to the above-mentioned Edge Environment services and applications, you can deploy Node-Red, Jupyter Notebook, Grafana, Power BI, and other third-party applications. These data analytics client applications can access Edge Environment's data internally. 

The Edge Environment's operating system is based on Linux kernel. All the software applications are deployed based on the Edge Environment operating system either as a virtual machine or a container. 

![DeltaV Edge Environment Server](./system-components/edge-server.png)

For detailed Server hardware specifications, refer to [Edge Environment System Components](./system-components/system-components.md) 

## Edge Orchestration

**NEED TO KNOW LEVEL OF DETAIL THAT WILL BE PRESENTED HERE**

## Data Diode (Optional)

For additional security, you can deploy an optional data diode between the Data Provider and the Edge Environment. 

<img src="./system-components/opswat-data-diode.png" width=400>

OPSWAT's NetWall Optical Diode is the tested and validated solution for users that need to egress data from the DeltaV system through the DeltaV Edge Environment using a data diode. The NetWall Optical Diode reliably transfers data over a hardware enforced one-way communications link enabling secure data sharing between isolated networks. The Data Diode supports a wide range of industrial protocols, is highly scalable, and can transfer real-time and historical data while ensuring the security and integrity of your critical assets.

For more detailed system component specifications, please check [DeltaV Edge System Components Specifications](./system-components/system-components.md)



# Accessing Data from DeltaV Edge Environment

Listed below are DeltaV objects/entities coming from Data Provider:

- System

- Area

- Process Cell

- Unit Module

- Equipment Module

- Control Module

- Function Block

- Fieldbus Shadow Block

- Parameter

- Alarm

- Named Set

- SIS Module

- Named State

- Engineering Unit

- SIS Named Set

- SIS Named State

- Folder

- Field

- #Properties

- #Config

The DeltaV Edge Environment exposes DeltaV data via industry standard interfaces such as as REST API and OPC UA.  

The OPC Unified Architecture (OPC UA) interface is a cross-platform, open-source, standard for data exchange for industrial applications. 


<img src="edge-data-access.png" width=600>

## Access DeltaV Data on the Edge Node through REST API

REST (representational state transfer) API is a web service that is based on HTTPS and provides data in JSON format, which are both compatible to numerous modern data analytics applications, such as Grafana, Jupyter Notebook, Node-RED, PowerBI, Excel, etc.

For more details on how to access data via REST API, please see more detailed instructions in [REST API Guide](./rest-api/rest-api.md)


## Access DeltaV Data on the Edge Node using OPC UA

The OPC Unified Architecture (OPC UA) interface is a cross-platform, open-source, standard for data exchange for industrial applications. 

For more details on how to access data via OPC UA, please check this repo: [OPC UA Guide](./opc-ua/opc-ua.md)


# Related repositories

-	[delta-edge-sdk](https://github.com/EmersonDeltaV/deltav-edge-sdk)
-	[simple-dockerapp-dotnet6](https://github.com/EmersonDeltaV/simple-dockerapp-dotnet6)

# Third-party tools with Edge

Below are example third party tools (with steps) you can use to access your data via DeltaV Edge Environment.
- [jupyter-labs-for-edge](https://github.com/EmersonDeltaV/jupyter-labs-for-edge)

- Grafana

- Node-RED

- [Power BI](./power-bi/power-bi.md)

- [Microsoft Excel](./microsoft-excel/microsoft-excel.md)

# Creating Edge Applications in Edge App Marketplace (DRAFT)

More details on setting up Edge Marketplace Applications can be found in [Edge Marketplace Application Development Guide](edge-applications.md)
