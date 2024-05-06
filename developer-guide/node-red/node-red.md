# Display Charts and Trends of Edge Data using Node-RED 


## Initial Configuration

**Node-RED** is a web browser-based flow editor for visual programming and provides a graphical way to wire together different APIs and services, enabling event-driven logic implementations. 
Access Node-RED using a web browser at:

`http://{edge_ip}:1880/` 

where `{edge_ip}` is the IP address of the Edge node Enterprise network (eth0) and 1880 is the designated port for the application.

## Sample Templates for Charts and Trends

The following are templates for charts and trends of the data that are available in the DeltaV Edge Environment:

- Process History View on the Edge

- Edge Processing 

- PID Mode

- Control Module
 
<p>

**Process History View replica on the Edge**

![Figure 16-1](./16-1-phv-replica.png)



**Edge Processing**

Shows runtime data integrated with IT data from the web (for example, livestock market indices, crude oil price, etc.)

![Figure 16-2. ](./16-2-runtime-it-data.png)


 
**PID Mode information**
 
![Figure 16-3](./16-3-pid-mode-1.png)

![PID Mode information](./16-3-pid-mode-2.png)
 


**Control Module information**
 
![Figure 16-4. Control Module information](./16-4-control-module-info-1.png)
![Alarms and Events - Control Module](./16-4-control-module-info-2.png)


## Sample Codes

1.	Drag and drop the inject node (timestamp), http request node (GET history), function node (Process), and chart node (chart).

2.	Connect all four nodes in series.
 

**Node-RED uses blocks to describe data flow**

![Figure 16-5](./16-5-node-red-blocks.png). 

3.	Double-click the timestamp node and configure the settings.

**Configure timestamp**

![Figure 16-6](./16-6-configure-timestamp.png). 

 
4.	Double-click the **GET history** node and configure the settings.  

Set the URL endpoint to: `https://10.223.28.66/api/v1/history?path=DEMO-PROPLUS_S/PID-103/PID1/PV.CV&starttime=2023-01-17T19:00:00&endtime=2023-01-17T19:05:00`

Refer to _Disabling/Skipping SSL verification on HTTP Request_ for steps to disable or skip SSL verification.

**Configure GET history**

![Figure 16-7](./16-7-configure-get-history.png) 


 
5.	Double-click the **Process** node and configure the settings.

**Configure Process**

![Figure 16-8](./16-8-configure-process.png). 


 
6.	Double-click the **chart** node and configure the settings.

**Configure Chart**

![Figure 16-9](./16-9-configure-chart.png). 


 
7.	Click **Deploy** to save the changes.

8.	To open the dashboard window, select Dashboard in the drop-down menu.

**Dashboard options**
 
![Figure 16-10](./16-10-dashboard-options.png). 

 
9.	Click on the display launcher (square with arrow) icon on the upper-right corner of the page.

**Display output chart by clicking the display launcher**

![Figure 16-11](./16-11-display-output-chart.png). 

 
10.	 A new browser tab opens with the display.
 
**Output Chart**

![Figure 16-12](./16-12-output-chart.png). 


# Node-RED Integration with Edge REST API

Listed below are the steps for installing the prerequisite nodes for data visualization.

1.	Go to **Menu → Manage palette** to install the prerequisite Node-RED dashboard to install the following prerequisite nodes:

-	node-red-dashboard

-	node-red-contrib-moment

- 	node-red-node-ui-table

 
**Manage palette option**

![Figure 16-13](./16-13-manage-palette.png) 

	
	
2.	Search for **node-red-dashboard**, **node-red-contrib-moment**, and **node-red-node-ui-table**.
 
**Node-RED nodes**

![Figure 16-14](./16-14-node-red-nodes.png) 

	
3.	Click **Install**.
	

**Install dashboard**

![Figure 16-15](./16-15-install-dashboard.png)


	
4.	Once installed, the dashboard nodes are displayed in the node selection pane.

**Dashboard nodes** 

![Figure 16-16](./16-16-dashboard-nodes.png)



**Running a Sample Node-Red Dashboard**

1.	On a blank Node-RED flow, click **Menu → Import** to import Node Red_Edge_REST API.json file.
Import file 

![Figure 16-17](./16-17-import-file.png)



2.	On the Imported Node-RED flow, double-click on the following nodes to open the Edit http request node window.
- HISTORY_REQ
- GRAPH_REQ
- AE_REQ

**Imported nodes**

![Figure 16-18](./16-18-imported-nodes.png)



3.	You can edit the request **URL** of the specific DeltaV Edge Environment system you want to get data from, and the Token generated from Postman. Refer to Postman Authentication for more information.

4.	Click **Done**. Refer to _Disabling/Skipping SSL verification on HTTP Request_ for steps to disable or skip SSL verification.

**Update URL and Token**

![Figure 16-19](./16-19-update-url-token.png)



5.	 After editing all the nodes mentioned, click Deploy.

**Deploy imported Edge node** 

![Figure 16-20](./16-20-deploy-imported-node.png) 


 
6.	Launch the Node-RED Dashboard through any of the following:


**Accessing Node-RED dashboard** 

![Figure 16-21](./16-21-access-dashboard.png) 

 
7.	Click **GET_HIST_DATA** to read and display data from Edge REST API history endpoint

**GET_HIST_DATA from Edge REST API endpoint** 

![Figure 16-22](./16-22-get-hist-data.png) 



8.	Go to the Edge Alarms and Events page and click **GET_AE_DATA** to get data from Edge REST API A&E endpoint.

**GET_AE_DATA from Edge REST API A&E endpoint** 

![Figure 16-23](./16-23-get-ae-data.png) 



## Disabling/Skipping SSL verification on HTTP Request

1.	In Node-RED, click **HTTP Request Node** and select **Enable secure (SSL/TLS) connection**.

**Edit HTTP request node**
 
![Figure 16-24](./16-24-edit-http-request.png) 

 
2.	Click the **Pencil** icon to edit the configuration.

3.	Clear the **Verify server certificate** check box and make sure to click **Update**.

**Verify server certificate**

![Figure 16-25](./16-25-verify-server-certificate.png) 


4.	Click **Done**.

**Completing the HTTP request node edit**

![Figure 16-26](./16-26-complete-http-request.png) 


5.	Click **Deploy**.

**Deploy the HTTP request node edit**

![Figure 16-27](./16-27-deploy-http-request.png) 


