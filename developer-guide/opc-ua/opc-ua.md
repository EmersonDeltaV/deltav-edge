# Access DeltaV Data on the Edge Node using OPC UA

The OPC UA server provides access to DeltaV runtime parameters, alarms and events, and cached data. The OPC UA server also supports multiple aggregation methods to simplify comprehensive data queries. 


You can verify the functionality of the Edge OPC UA server by installing a free OPC UA client (for example, UaExpert, Integration Objects) on a computer with access to the Edge Node.

Use your defined access path and security settings to connect to the Edge OPC UA server.

After a successful connection, you can verify the following information in the OPC UA client:

- Initial connectivity structure

- DeltaV system hierarchy (under Objects folder) and into specific modules and configuration parameters

- Runtime parameters from the History Collection Points or imported CSV file are updating

- History data and multiple aggregation methods

- Alarms and Events



> **Note**: The complete hierarchy (system to function block) is accessible on the Edge OPC UA but only the subscribed parameters and fields are shown in the Edge OPC UA address space.


# Accessing via UaExpert

## Connect to the Edge OPC UA server

1. Connect the UaExpert OPC UA client application to the Edge OPC UA server 

- **UaExpert** → Add Server → Advanced

> **Note**: Make sure that the OPC UA settings configured here match the settings in: `DeltaV Edge Manager → Settings → OPC UA.`


2. Enter the following details in the Add Server dialog:

a. Server Information

Set Endpoint URL: 
```
opc.tcp://{edge_ip}:XXXX 
```

where ```{edge_ip}``` is the IP address of the Edge Node Enterprise network (eth0)
and ```XXXX``` is the designated port for the OPC UA server.

b. Security Settings - Specify the Security Policy and Message Security Mode
for communications between the Edge OPC UA server and clients.

c. Authentication Settings - Select Username Password and enter the available
and valid login credentials.

![Figure 7-1: UaExpert OPC UA client](7-1-uaexpert-client.png)

```
Note:
- You may select Anonymous for the Authorization Settings but this results in a limited view of the folders in the Address Space.

Make sure to select the Allow Anonymous Client Access check box in:
- DeltaV Edge Manager → Settings → OPC UA.

See Section 2.5 Settings of the DeltaV Edge Environment User Guide for more information.

- The Certificate Private Key logon is not supported in version 1 of the release.
```


3. Click OK.

![Figure 7-2: Enter Username and Password](7-2-opc-ua-login.png)

> Note: Profiles created in the DeltaV Edge Manager can login using their username and password as long as they are set as Available in the Settings menu. Refer to Login Methods for more information.

- If you get a connection error BadCertificateHostNameInvalid, refer to
Mapping the hostname to an IP Address for troubleshooting information.

![Figure 7-2a: Enter Username and Password](7-2-opc-ua-login-error.png)


## Access Control Hierarchy Data

1. On the Project pane, click Edge OPC UA (Project → Servers → Edge OPC UA). The
corresponding Address Space updates accordingly.

2. Browse the system hierarchy on the Address Space (Root → Objects → Root →
DeltaVSystems → {System name} → ControlStrategies → {List of Areas}).

![Figure 7-3: Unified Automation UaExpert Address Space](7-3-uaexpert-address-space.png)

```
Note:

- The complete hierarchy (system to function block) is accessible on the Edge OPC UA but only the subscribed parameters and fields are shown in the Edge OPC UA address space.

- The objects displayed in the hierarchy may vary for different profiles. For example, an administrator sees more folders under System than a non-administrator user.
```


## Access Runtime and Cached Parameter Values
The Edge OPC UA supports runtime and history data access. Follow the steps below to
monitor runtime parameter field values and to retrieve cached parameter field values from
the Edge Node using the UaExpert OPC UA client.

1. On the Address Space, navigate to the parameter field that you want to monitor.
For example, to monitor PID-101/PID1/PV.CV, 

```
Root → Objects → Root → System → Core → DeltaVSystems → PH-MS-EDGE-PP_S → ControlStrategies → THERMO_PULPING → PID-101 → PID1 → PV → CV
```

then click on the parameter fields and drag to the Data Access View section.

![Figure 7-4: Monitor parameter fields](7-4-monitor-parameter-fields.png)

2. On the Data Access View, you should see the list of monitored parameter fields.
Their values and timestamps change at a rate equal to the configured sampling
periods.

> **Note**: Verify that the values are consistent with those reported in DeltaV WatchIt.

3. On the Project pane, right-click Documents, then click Add History Trend View.

![Figure 7-5: Add History Trend View](7-5-add-history-view.png)

4. Click the History Trend View tab. Drag the parameter field that you want to access
history data to the History Trend View.

> **Note**: Verify that the history data are consistent with those reported in DeltaV Process History View.


![Figure 7-6: History Trend View](7-6-history-trend-view.png)

5. Configure the history trend update settings.
a. For Single Update, enter the trend's Start Time and End Time, then click
Update.

![Figure 7-7: History trend Single Update](7-7-history-trend-single-update.png)

b. For Cyclic Update, enter the trend's Timespan and Update Interval, then
click Start.

![Figure 7-8: History trend Cyclic Update](7-8-history-trend-cyclic.png)




## Access Alarms & Events Data
You can also use OPC UA to monitor runtime alarms & events streamed to the Edge Node
using the UaExpert OPC UA client.
1. On the Address Space, navigate to the event notifier node configured to receive
events. This node is the AlarmsAndEvents (Root → Objects → Root → System →
Core → AlarmsAndEvents).

![Figure 7-9: AlarmsAndEvents EventNotifier details](7-9-alams-events-notifier.png)

2. Drag the AlarmsAndEvents node to the configuration panel under the Event View
tab. Wait for 30 to 40 seconds for data to load.

![Figure 7-10: AlarmsAndEvents (Event View)](7-10-alarms-events-view.png)

3. Configure the monitored item and select the ForwardedEventType check box
(Edge OPC UA/AlarmsAndEvents → Simple Events under Server/Object).

![Figure 7-11: Enable ForwardedEventType](7-11-enable-forwarded-event.png)

4. Click Apply. The system displays all incoming alarms & events under the Events
panel.

![Figure 7-12: Incoming alarms & events list](7-12-incoming-alarms-events.png)

5. Click any of the incoming events to view the property details. These properties
include:

- AlarmMessage

- AreaName

- Category

- EventId

- Event type

- Level

- ModuleDesc

- ModuleName

- NodeName

- Parameter

- RawEventContent

- State

- Time

- UnitName

> **Note: ** Verify that the alarms and events are consistent with those reported in DeltaV Process History View or DeltaV Alarms List.


![Figure 7-13: Alarms & event details](7-13-alarms-events-details.png)


# Accessing via Integration Objects

Connect to the Edge OPC UA server
1. Connect the Integration Objects OPC UA client application to the Edge OPC UA server by clicking Connect.

> **Note:** Make sure that the OPC UA settings configured here match the settings in the DeltaV Edge Manager → Settings → OPC UA page.

2. Enter the following details, then click Apply.

a. On the Server Information group, set Endpoint URL:
```
opc.tcp://{edge_ip} 
```
where ```{edge_ip}``` is the IP address of the Edge Node Enterprise network (eth0).

b. Specify the following communication and security settings:

- Transport Protocol

- Message Encoding

- Security Mode

- Security Policy

c. On the User Authentication Mode group, click UserName, and enter the available and valid login credentials.

d. Click Apply.

![Figure 7-14: Integration Objects OPC UA client](7-14-integration-objects.png)

```
Note
- You may select Anonymous for the Authorization Settings but this results in a
limited view of the folders in the Address Space. Make sure to select the Allow
Anonymous Client Access check box in the DeltaV Edge Manager → Settings → OPC UA. 

See Section 2.5 Settings of the DeltaV Edge Environment User Guide for more information.

- The Certificate logon is not supported in version 1 of the release.
```

## Access Control Hierarchy Data

1. On the Sessions pane, click Edge OPC UA (Sessions → Edge OPC UA). The
corresponding Address Space updates accordingly.

2. Browse the system hierarchy on the Address Space 

```
Root → Objects → Root → System → Core → DeltaVSystems → {System name} → ControlStrategies → {List of Areas}
```

![Figure 7-15: Integration Objects OPC UA Client Address Space](7-15-integration-objects-address-space.png)

> **Note:** **The complete hierarchy (system to function block) is accessible on the Edge OPC UA but only the subscribed parameters and fields are shown in the Edge OPC UA address space.

## Access Runtime and Cached Parameter Values -Aggregate

In the Integration Objects OPC UA client, you can also monitor runtime values and
aggregated cached parameter field values on the DeltaV Edge Environment.

> **Note:** Aggregation of values is not available in the UaExpert OPC UA client.


1. On the Address Space, navigate to the parameter field that you want to monitor.
For example, to monitor PID-101/PID1/PV.CV:
```
Root → Objects → Root → System → Core → DeltaVSystems → PH-MS-EDGE-PP_S → ControlStrategies → THERMO_PULPING → PID-101 → PID1 → PV → CV
```
, then right-click Monitor.

![Figure 7-16: Monitor parameter fields](7-16-monitor-parameter-fields.png)

2. Fill in the Subscription Settings, then click OK.

3. On the Data View tab, you should see the list of monitored parameter fields. Their values and timestamps change at a rate equal to the configured sampling periods.

![Figure 7-17: List of monitored parameter fields (Data View)](7-17-list-monitored-parameter-fields.png)

4. Click the History View tab. Drag the parameter field that you want to access history
data.

5. To get raw parameter field values, select Read Type = Raw, then set the timespan
of the data via the Start Time and End Time.

![Figure 7-18: List of monitored parameter fields with Read Type = Raw (History View)](7-18-list-monitored-parameter-fields-raw.png)

6. To get aggregated parameter field values, set Read Type = Processed, select from
the list of Aggregate functions the function you want to apply (for example,
Average) over data values within set Processing Interval, then set the timespan of
data you want to retrieve via the Start Time and End Time.

![Figure 7-19: List of monitored parameter fields with Read Type = Processed (History View)](7-19-list-monitored-parameter-fields-processed.png)

> **Note:** All the aggregate functions on the drop-down list are supported by the Edge OPC UA server.
