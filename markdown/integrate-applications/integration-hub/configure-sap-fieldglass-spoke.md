---
title: Configure SAP Fieldglass connection record
description: Configure the connection record to enable your ServiceNow instance to connect with the SAP Fieldglass tenant.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SAP Fieldglass Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure SAP Fieldglass connection record

Configure the connection record to enable your ServiceNow instance to connect with the SAP Fieldglass tenant.

## Before you begin

-   Request an Integration Hub subscription.
-   Ensure you’ve generated the API key from the SAP Fieldglass tenant.
-   Activate the SAP Fieldglass spoke.
-   Role required: admin.

## Procedure

1.  Configure the connection record for the SAPFieldGlassBuyer alias.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

    2.  Select Connections.

    3.  Turn on the Outbound tab.

    4.  In the Search all connections field, enter `SAP Fieldglass`.

    5.  On the SAP SAPFieldGlassBuyer card, select **View Details**.

    6.  Select **Configure**.

    7.  Fill the form.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the connection record. The default and read-only name of the first connection record is the SAPFieldglassBuyer Connection. To create a record with your custom name, select **Add Connection**.|
        |Connection URL|URL to connect to SAP Fieldglass APIs in the format `https://<SAP Fieldglass environment URL>.com/api`.|
        |Name|Custom name of the credentials to access the SAP Fieldglass tenant.|
        |User name|User name to log in to the SAP Fieldglass tenant.|
        |Password|Password to log in to the SAP Fieldglass tenant.|
        |APIKey|API key of the buyer.|

    8.  Select **Configure Connection**.

2.  Configure the connection record for the SAPFieldGlassSupplier alias.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

    2.  Select Connections.

    3.  Turn on the Outbound tab.

    4.  In the Search all connections field, enter `SAP Fieldglass`.

    5.  On the SAP SAPFieldGlassSupplier card, select **View Details**.

    6.  Select **Configure**.

    7.  Fill the form.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the connection record. The default and read-only name of the first connection record is the SAPFieldGlassSupplier Connection. To create a record with your custom name, select **Add Connection**.|
        |Connection URL|URL to connect to SAP Fieldglass APIs in the format `https://<SAP Fieldglass environment URL>.com/api`.|
        |Name|Custom name of the credentials to access the SAP Fieldglass tenant.|
        |User name|User name SAP Fieldglass buyer tenant.|
        |Password|Password of SAP Fieldglass buyer tenant.|
        |APIKey|API key of the supplier.|

    8.  Select **Configure Connection**.


