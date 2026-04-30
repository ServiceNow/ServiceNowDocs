---
title: Service Graph Connector for Nokia Altiplano
description: Use the Service Graph Connector for Nokia Altiplano Access Network SDN Controller to pull in data from the Nokia Altiplano software into your ServiceNow instance using REST APIs.The Import Sets are the input for the IntegrationHub ETL, where the transformation maps create and model relationships. When data is loaded into the Import Set, the transformation process is triggered.Data from data sources in the Nokia Altiplano software is mapped and transformed into ServiceNow CMDB tables using the Robust Transform Engine \(RTE\). Data is inserted into ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).Service Graph Connector for Nokia Altiplano installs special system properties that control various behaviors of the application.Examples of Retrieving Data from Nokia Altiplano via REST API.
locale: en-US
release: yokohama
product: Telecom Visibility
classification: telecom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Telecom Discovery using Service Graph Connectors \(SGC\), Exploring Telecom Discovery, Telecom Discovery, TSOM Visibility, Telecommunications Service Operations Management]
---

# Service Graph Connector for Nokia Altiplano

Use the Service Graph Connector for Nokia Altiplano Access Network SDN Controller to pull in data from the Nokia Altiplano software into your ServiceNow instance using REST APIs.

The Service Graphs Connector for Nokia Altiplano pulls in asset inventory data \(physical network resources\) from the Nokia Altiplano database.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Nokia Altiplano SGC Architecture

![nokia altiplano architecture.](../images/telecom-service-graph-connector-nokia-altiplano.png)

Data Source defined as the following:

-   Custom load by script
-   Data in single column

For a general overview of Service Graph Connector technology, see [Getting started with Service Graph Connectors](https://www.servicenow.com/docs/access?context=cmdb-sgc-intro&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

## Supported versions

Supported Nokia Altiplano Controller minimum versions: 24.6.

## Use cases

The following are examples on how you can use the Nokia Altiplano Service Graph Connector:

-   **The Nokia Altiplano Service Graph Connector** can be used to pull data from the Nokia Altiplano Access Controller via REST API \(through a MID Server\), confirming that the CMDB is populated with accurate, up-to-date information about physical network resources such as OLTs and ONTs, among others. This integration provides a telecom-model-aligned view of network resources and their relationships.
-   **Future Capabilities**: In upcoming releases, the Nokia Altiplano Service Graph Connector expands its capabilities to discover not only physical resources but also logical resources and services/connections, enabling a more comprehensive view of both the physical and logical aspects of the network. It will also support event-driven discovery, where the Altiplano Controller notifies the ServiceNow instance \(via the MID Server\) about a change and sequentially triggers a discovery task.
-   Ability to configure and save synchronization schedules.

## Guided setup

The guided setup for the Service Graphs Connector for Nokia Altiplano provides an organized sequence of tasks to configure the integration on your instance. To access the guided setup, see [Configure Service Graph Connector for Nokia Altiplano](configuring-service-graph-connector-nokia-altiplano.md#).

## CMDB Integrations Dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed Service Graph Connectors. You can see metrics for all integration runs. You can filter the view to a specific integration, a specific time duration, or a specific integration run. For more details about monitoring SolarWinds integrations in the CMDB Integrations Dashboard, see [Integration Commons for CMDB](https://www.servicenow.com/docs/access?context=integration-commons-for-cmdb&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[Telecom Discovery using Service Graph Connectors \(SGC\)](telecom-discovery-using-service-graph-connector.md)

## Import Sets

The Import Sets are the input for the IntegrationHub ETL, where the transformation maps create and model relationships. When data is loaded into the Import Set, the transformation process is triggered.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Import sets** &gt; **Administration** &gt; **Import Sets**.

    The Data Source script automatically creates staging tables.

    ![staging table.](../images/import-sets-sgc-nokia.png) ![import set.](../images/import-sets-sgc-2.png)


## Data Mapping

Data from data sources in the Nokia Altiplano software is mapped and transformed into ServiceNow CMDB tables using the Robust Transform Engine \(RTE\). Data is inserted into ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete the guided setup, you can configure the integration to periodically pull data from the SolarWinds software.

The data is loaded into staging tables, then inserted into the following CMDB target tables with the following relationships:

### Mapping CMDB CIs and CI Relationships \(Physical Layer\)

<table id="table_dfm_5hg_12c"><thead><tr><th>

CIs

</th><th>

CI Relationships

</th></tr></thead><tbody><tr><td>

OLT CI

</td><td>

OLT Device is represented by the OLT CI.

 Table name: **__cmdb\_ci\_optical\_line\_terminal__**

 OLT CI contains Slot CIs.

</td></tr><tr><td>

ONT CI

</td><td>

ONT Device is represented by the ONT CI.

 Table name: **__cmdb\_ci\_optical\_network\_terminal__**

 ONT CI contains Network Interface CIs.

 ONT Network Interface CIs is contained by the ONT CI.

</td></tr><tr><td>

Slot CI

</td><td>

Chassis slots are represented by the Slot CI.

 Table name: **cmdb\_ci\_container\_slot**

 Slot CI is contained by OLT CI.

 Slot CI contains the Interface Card CI \(LT/NT cards, Fan/PSU units\).

</td></tr><tr><td>

Subslot CI

</td><td>

LT/NT card cages are represented by the Subslot CI.

 Table name: **cmdb\_ci\_container\_subslot**

 Subslot CI is contained by OLT LT card CI.

 Subslot CI is contained by OLT NT card CI.

 Subslot CI contains the Interface Card CI \(transceiver cards\).

</td></tr><tr><td>

Interface Card CI

</td><td>

LT and NT cards are represented by the Interface Card CI.

 Transceiver cards are represented by the interface Card CI.

 Fan and Power Supply Units are represented by the Interface Card CI. \(Special cards, Fan, and Power Supply Units CI might be changed in the next releases\).

 Table name: **cmdb\_ci\_interface\_card**

 LT Card contains the Subslots CIs.

 NT Card contains the Subslots CIs.

 NT cards CIs contains Network Interface CIs

 LT/NT transceiver cards CIs contains Network Interface CIs.

 LT/NT Card CI is contained by the LT/NT Slots CI.

 LT transceiver Card CI is contained by the subslot CI \(LT Card\).

 NT transceiver Card CI is contained by the Subslot CI \(NT card\).

</td></tr><tr><td>

Network Interface CI

</td><td>

LT card PON access ports as well as NT card network ports are represented by the Network Interface CI.

 Table name: **cmdb\_ci\_ni\_interface**

 Network Interface CIs contained by LT transceiver/NT transceiver/NT cards CIs.

 ONT Network Interface CI is contained by ONT CIs.

</td></tr></tbody>
</table>You can use the **IntegrationHub ETL** application to view and manage data maps.

For more information, see [IntegrationHub ETL](https://www.servicenow.com/docs/access?context=integrationhub-etl&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

### Supported xNFs

-   Lightspan MF-2 \(OLT\)
-   Lightspan ISAM FX-4 \(OLT\)
-   Lightspan XS-010X-Q \(ONT\)
-   Lightspan XS-010X-R \(ONT\)

## Special System properties

Service Graph Connector for Nokia Altiplano installs special system properties that control various behaviors of the application.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Nokia Altiplano** &gt; **Properties**.

    ![system properties.](../images/telecom-special-systemproperties.png)

    You can also access these properties by entering **sys\_properties.list** and filtering by the name ‘\*altiplano’.

    ![properties list.](../images/telecom-system-properties-list.png)

<table id="table_xyy_pwg_12c"><thead><tr><th>

Property Name

</th><th>

Recommended / Default Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_sgc\_altiplano.olt\_batch\_size

</td><td>

300

</td><td>

The OLT Datasource batch size for REST Calls. The number represents number of Altiplano response entities. \(Increasing may cause failure in the REST actions execution\)

</td></tr><tr><td>

sn\_sgc\_altiplano.onu\_batch\_size

</td><td>

3

</td><td>

The ONU Datasource batch size for REST Calls. The number represents number of LT cards related ONU data.

 \(Increasing may cause failure in the REST actions execution\)

</td></tr><tr><td>

sn\_sgc\_altiplano.onu\_ci\_class

</td><td>

ONT

</td><td>

ONU CI Class, Valid values: ONU or ONT

</td></tr></tbody>
</table>
## Examples of Retrieving Data from Nokia Altiplano via REST API

Examples of Retrieving Data from Nokia Altiplano via REST API.

### URL format

Versioned URL: POST: `altiplano-indexsearch/latestcompleted-inv/_search`

### For OLT

```

{
    "_source": [
        "deviceAVmetadata",
        "inventorymetadata",
        "inventorydata.ietf-hardware:hardware",
        "inventorydata.ietf-hardware:hardware-state",
        "inventorydata.nokia-state:state"
    ],
    "sort": [{"_id": {"order": "asc"}}],    
    "from": 0,  
    "size":300
}

```

### For ONU

```

{
      "query": {
            "bool": {
                "should": [
                    {
                        "exists": {
                            "field": "inventorydata.ietf-interfaces:interfaces-state.interface.bbf-xponvani:v-ani.onu-present-on-this-olt.detected-serial-number"
                        }
                    }
                ]
            }
    },
    "_source": [
         "inventorydata.ietf-interfaces:interfaces-state.interface.bbf-xponvani:v-ani.onu-present-on-this-olt.detected-serial-number",
        "inventorydata.bbf-fiber-onu-emulated-mount:onus.onu.root.ietf-hardware-mounted:hardware-state",
        "inventorydata.bbf-fiber-onu-emulated-mount:onus.onu.name"
     ],
    "sort": [{"_id": {"order": "asc"}}],    
    "from": 0,  
    "size": 3
}
```

