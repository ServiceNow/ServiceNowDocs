---
title: Set up SAP S4 HANA OData spoke
description: Integrate the ServiceNow instance and SAP S4 HANA OData spoke by using the Basic Auth credentials to authenticate ServiceNow requests.Create a credential record for the SAP S4 HANA OData spoke. The SAP S4 HANA OData spoke connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SAP S4 HANA OData spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up SAP S4 HANA OData spoke

Integrate the ServiceNow instance and SAP S4 HANA OData spoke by using the Basic Auth credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the SAP S4 HANA OData spoke.
-   Role required: admin.

## Create a connection record for the SAP S4 HANA OData spoke

Create a credential record for the SAP S4 HANA OData spoke. The SAP S4 HANA OData spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the **SAP S4 HANA OData** record.

3.  From the Related Links tab, select **Create New Connection &amp; Credential**.

4.  On the Create Connection and Credential form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to uniquely identify the connection record. For example, `SAP S4 HANA OData Connection`.|
    |Connection URL|Fully qualified domain name of the target host where the SAP S4 HANA OData server is installed.|
    |Use MID server|Option to select MID server. This field selected by default.|
    |User Name|User name of your SAP S4 HANA OData account.|
    |Password|Password of your SAP S4 HANA OData account.|

5.  Click **Create**.


