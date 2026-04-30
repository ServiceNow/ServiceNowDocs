---
title: View alerts in the SAP Solution Manager inbox
description: You can view alerts generated in SAP Solution Manager to see any pressing issues. All alerts also forward to Event Management automatically.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SAP Solution Manager setup configurations, Enable SAP connector configurations, Configure SAP Solution Manager connector, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# View alerts in the SAP Solution Manager inbox

You can view alerts generated in SAP Solution Manager to see any pressing issues. All alerts also forward to Event Management automatically.

## Before you begin

Role required: evt\_mgt\_admin

## Procedure

1.  On the SAP UI, open Solution Manager and select the **System Alerts** tab.

    ![Solution Manager UI](../image/sap-solman-solution-mgr-ui.png)

    The system alerts are listed on the page.

2.  Navigate to \(**Event Management** &gt; **All Alerts\)** to view the alerts in Event Management.

    ![Alerts in Event Management UI](../image/sap-solman-alerts-in-em.png)

    The following table describes the field mapping between SAP Solution Manager and Event Management for alerts.

    |SAP Field|Event Management Field|Description|
    |---------|----------------------|-----------|
    |severity|severity|SAP uses a number from 1 \(less critical\) to 9 \(more critical\)|
    |message\_key|message\_key|SAP message group ID, messageGUID|
    |description|description|Event description|
    |source|source|SAP system ID|
    |managed\_object\_type|type|The type of the object, such as Host or Instance|
    |node|node|Object name|
    |managed\_object\_name|resource|Solution manager node name|
    |N/A \(there is no value provided by SAP. Event Management generates the indicated field.\)|source instance|The event class must match the connector pull instance name, with the structure &lt;Source&gt;\_&lt;Client&gt;.|
    |source|additional\_info.sid|SAP system ID|
    |rating|additional\_info.rating|Event color in SAP|
    |resource|additional\_info.mandant|SAP mandant|
    |metric\_name|metric\_name|Metric name for the SAP event|
    |time\_of\_event|time\_of\_event|Time of event in SAP|


## High CPU Usage on SAP Host

Scenario: An alert is generated in SAP Solution Manager when the CPU usage on a critical host exceeds 90% for more than 10 minutes.

|Field|Value|
|-----|-----|
|Severity|8 \(Critical\)|
|Message Key|CPU\_Overload\_12345|
|Description|High CPU usage on SAPHost01|
|Source|SAP\_Prod|
|Type|Host|
|Node|SAPNode\_01|
|Time|2024-07-31T14:23:00Z|

Here’s how the alert is mapped in Event Management:

|Field|Value|
|-----|-----|
|Severity|8|
|Message Key|CPU\_Overload\_12345|
|Source|SAP\_Prod|
|Type|Host|
|Node/Resource|SAPNode\_01|
|Source Instance|SAP\_Prod\_100|
|SID|SAP\_Prod|
|Rating|Red|
|Mandant|100|

**Parent Topic:**[SAP Solution Manager setup configurations](../concept/sap-solman-configurations.md)

