# DeltaV Edge Environment Developer Guide

For more detailed info on DeltaV Edge Environment Architecture and System Components, please check: [DeltaV Edge Environment System Components]()

# Development Basics

## Access DeltaV Data on the Edge Node through REST API

REST (representational state transfer) API is a web service that is based on HTTPS and provides data in JSON format, which are both compatible to numerous modern data analytics applications, such as Grafana, Jupyter Notebook, Node-RED, PowerBI, Excel, etc.

For more details on how to access data via REST API, please see more detailed instructions in [REST API Guide](./rest-api/rest-api.md)


## Access DeltaV Data on the Edge Node using OPC UA

The OPC Unified Architecture (OPC UA) interface is a cross-platform, open-source, standard for data exchange for industrial applications. 

For more details on how to access data via OPC UA, please see more detailed instructions in:   [OPC UA Guide](./opc-ua/opc-ua.md)

# Connect via Commercial and Open Source Appications



# Application Development

Sample code and related repositories


-	[delta-edge-sdk](https://github.com/EmersonDeltaV/deltav-edge-sdk) -- _C# Edge REST API Client SDK implemented via HttpClient to simplify Edge REST API consumption_

-	[edge-watch-it](https://github.com/EmersonDeltaV/simple-dockerapp-dotnet6) -- _C# sample app that demonstrates basic Edge functionalities such as User Authentication, connection, and runtime value updates._ 

## Creating and Packaging Edge Applications

You can also develop custom applications that can be packaged as containers and deployed within an Edge node that can be used by everyone in your Enterprise.

-	[simple-dockerapp-dotnet6](https://github.com/EmersonDeltaV/simple-dockerapp-dotnet6) -- _basic ASP.NET Core 6.0 web app created as a docker image that can be published into the DeltaV Edge Environment_


More details on setting up Edge Marketplace Applications can be found in [Edge Marketplace Application Development Guide](edge-applications.md)




