# DeltaV Edge Environment

The DeltaV Edge Environment is a platform that provides easy and secure access to DeltaV system data for on-premise use or in the cloud for monitoring, analytics, reporting or for other Enterprise applications.
Accessing plant data from a Distributed Control System such as DeltaV, can be a very complex task.
Data resides down in the Control Network and thus bringing it outside to the Enterprise network requires multiple layers of secure processing.  

The DeltaV Edge Environment simplifies data access to plant data by handling all of the security transfer from across the different network layers.  DeltaV Edge Environment also manages the contextualization of data coming from the Control Network instead of by relating it to where it is being used, instead of simply presenting raw data values.  

The DeltaV Edge Environment provides a common application platform that makes this contextual set of data available via industry standard protocols such as OPC UA and REST API, thus allowing more data consumption options through third-party applications such as Grafana, Node-RED, and JupyterLabs Notebook.  



The intent of this github page is to provide sample code, guides, and software development kits to encourage non-Emerson developers to create their own applications that can unlock the potential of having access to such wealth of plant data, such as data analytics, graphical representation, etc.


# Application Development features include
-	Contextualized data available via OPC UA and REST API.
-	Online Cloud orchestration of Edge Nodes and Applications
-	Easy application management via Docker containers and Virtual Machines.


# Getting Started

To get you started, here are additional info on Edge functionality, sample guides, and repositories:

\<In-depth Developer Guide (separate page) including:\>

\<Types of data being gathered\>

\<High level architecture description, describing behavior – e.g. polling, continuous streaming, data throughput, one-way data transfer, limitations, and other application behavior that may be useful to developers, and recommendations\> 

# Sample usage

-	\<sample data access using OPC UA\>
-	\<sample data access using REST API\>
o	Examples to get all values coming from PT-101.
-	Connecting data to Power BI

# Note to developers

<e.g. things like.. “Only latest versions are supported, and will not include…”>


# Related repositories

-	[delta-edge-sdk](https://github.com/EmersonDeltaV/deltav-edge-sdk)
-	[simple-dockerapp-dotnet6](https://github.com/EmersonDeltaV/simple-dockerapp-dotnet6)

# Third-party tools with Edge [Draft]
Below are the list of third party tools (with steps) you can use to access your data via Edge.
- [jupyter-labs-for-edge](https://github.com/EmersonDeltaV/jupyter-labs-for-edge)
- grafana
- power bi

# Contributing

This project welcomes contributions, suggestions, and feedback. All contributions, suggestions, and feedback you submitted are accepted under the Project's license. You represent that if you do not own copyright in the code that you have the authority to submit it under the Project's license. All feedback, suggestions, or contributions are not confidential.

For more information on how to contribute to DeltaV Edge Environment, please read CONTRIBUTING.md.


# References [draft]
- EDGE is based on eve-os [v9.4.6-lts](https://github.com/EmersonDeltaV/lf-edge-eve)
