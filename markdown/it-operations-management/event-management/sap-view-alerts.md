---
title: View alerts in the SAP Solution Manager inbox
description: You can view alerts generated in SAP Solution Manager to see any pressing issues. All alerts also forward to Event Management automatically.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SAP Solution Manager setup configurations, SAP configurations enabling the SAP Solution Manager connector, Configure SAP Solution Manager connector, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
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
    |managed\_object\_name|node|Object name|
    |node|resource|Solution manager node name|
    |N/A \(there is no value provided by SAP. Event Management generates the indicated field.\)|source instance|The event class must match the connector pull instance name, with the structure &lt;Source&gt;\_&lt;Client&gt;.|
    |source|additional\_info.sid|SAP system ID|
    |rating|additional\_info.rating|Event color in SAP|
    |resource|additional\_info.mandant|SAP mandant|
    |time\_of\_event|time\_of\_event|Time of event in SAP|


**Parent Topic:**[SAP Solution Manager setup configurations](../concept/sap-solman-configurations.md)

