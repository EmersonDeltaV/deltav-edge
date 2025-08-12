
# DeltaV Edge Environment v2.0 Release Info


|Specification|Description|
|---|---|
| Compatibility | DeltaV v14.LTS, v14.FP1, v14.FP2, v14.FP3, v15.LTS, v15.FP1 and v15.FP2 |
| Number of Supported Data Items | 20k, 100k, 300k |
| Supported Sampling Periods | 1s, 2s, 5s, 10s, 60s |
| Alarms and Events Handling | 100 events/second, 4K peak alarm burst handling |
| Batchy Events | Supports data from up to 4 active Batch Executives, each handling up to 100 active batches |
| Data Types Supported | DeltaV S88 Plant Hierarchy, Configuration Data, Process Values, Alarms & Events, SIS Module Data |
| DeltaV Objects/Entities Supported | System, Area, Process Cell, Unit Module, Equipment Module, Control Module, Function Block, Fieldbus Shadow Block, Parameter, Alarm, Named Set, SIS Module, Named State, Engineering Unit, SIS Named Set, SIS Named State, Folder, Field, #Properties, #Config |
| Edge Node's Operating System | [EVE-OS v12.0.7-LTS](https://github.com/EmersonDeltaV/lf-edge-eve) (Linux-based OS)|



## Edge Server (Dell PowerEdge R660xs XL)

DeltaV Edge Environment utilizes the Dell PowerEdge R660xs XL server as its hosting hardware platform. The server is available in two configurations, as shown in the table below:

| DeltaV™ Edge Environment Server based on Dell PowerEdge R660xs XL Rack Mounted Server |
| --- |
| ![Dell PowerEdge R660xs XL](images/edge-server.png) |

| Specifications | Details |
| --- | --- |
| Part Number | SE2742C02 |
| Supported Capabilities | Core DeltaV™ Edge applications, DeltaV Live Enterprise View, and third-party app hosting |
| Memory (RAM) | 256GB RAM |
| CPU | Dual Intel Xeon Gold 6526Y 2.8G, 16C/32T, 20GT/s, 37.5M Cache, Turbo, HT (195W) DDR5-5200 |
| Storage |  12TB SSD (7 x 1.92TB SATA Read-Intensive SSD, RAID 5) |
| Chassis | 2.5" Chassis with up to 8 Hard Drives (SAS/SATA), 2 CPU |
| RAID Controller | PERC H755 SAS Front |
| Network Interface | Broadcom 5720 Quad Port 1GbE BASE-T Adapter, OCP NIC 3.0 |
| Power Supply | Dual, Hot-Plug, Redundant (1 +1 ), 800W |
| Management | iDRAC9, Enterprise 16G |
| Form Factor | 1U Rack-Mounted Server (Height: 42.8mm (1.68in), Width: 482mm (18.97in), Depth: 748.79mm (29.47in)) |
| Operating System | EVE-OS 12.0.7 LTS |
| Warranty | Up to 5 Years |

The Dell PowerEdge R660xs XL server replaces the previously supported Dell PowerEdge R650xs (SE2741C01) in this configuration. However, the R650xs model still includes a five-year warranty from Dell, applicable from the original date of purchase.
                                                                   

## Data Diode	(Optional)

The OPSWAT MetaDefender Optical Diode. 
 
<img src="images/opswat-data-diode.png" width=750>

For the DeltaV Edge Environment, MetaDefender Optical Diode 100MB and 1GB data transfer rates are supported options. This solution enables you to connect the Data Provider directly to the Edge Node for a secure and simplified IT network solution.




