# DeltaV Edge Environment Developer Guide

For more detailed info on DeltaV Edge Environment Architecture and System Components, please check: [DeltaV Edge Environment System Components]()

# Development Basics

DeltaV Edge Environment makes DeltaV data accessible to the Plant and Enterprise networks via industry standard interfaces such as REST API and OPC UA.

For more details on how to access data via REST API, please see more detailed instructions in [REST API Guide](./rest-api/rest-api.md)
For more details on how to access data via OPC UA, please see more detailed instructions in: [OPC UA Guide](./opc-ua/opc-ua.md)

You can also connect these endpoints to various analytical applications and visualizations such as:

- <a href="https://github.com/EmersonDeltaV/jupyter-labs-for-edge">Jupyter Notebook
- [Power BI](developer-guide/power-bi/power-bi.md)
- [Microsoft Excel](developer-guide/microsoft-excel/microsoft-excel.md)




# Application Development

Sample code and related repositories


-	[delta-edge-sdk](https://github.com/EmersonDeltaV/deltav-edge-sdk) -- _C# Edge REST API Client SDK implemented via HttpClient to simplify Edge REST API consumption_

-	[edge-watch-it](https://github.com/EmersonDeltaV/simple-dockerapp-dotnet6) -- _C# sample app that demonstrates basic Edge functionalities such as User Authentication, connection, and runtime value updates._ 

## Creating and Packaging Edge Applications

You can also develop custom applications that can be packaged as containers and deployed within an Edge node that can be used by everyone in your Enterprise.

-	[simple-dockerapp-dotnet6](https://github.com/EmersonDeltaV/simple-dockerapp-dotnet6) -- _basic ASP.NET Core 6.0 web app created as a docker image that can be published into the DeltaV Edge Environment_





