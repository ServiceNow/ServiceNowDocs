---
title: Set up Navex EthicsPoint spoke spoke
description: Integrate the ServiceNow instance and Navex EthicsPoint spoke instance using the Basic Auth credentials to authenticate ServiceNow requests.Integrate the ServiceNow instance and the Navex EthicsPoint instance by using the Basic Auth credentials to authenticate ServiceNow requests.Create connection records to your Navex EthicsPoint instance. The Navex EthicsPoint spoke connection and credential alias uses these connections to perform actions in Navex EthicsPoint instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Navex EthicsPoint Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up Navex EthicsPoint spoke spoke

Integrate the ServiceNow instance and Navex EthicsPoint spoke instance using the Basic Auth credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate Navex EthicsPoint spoke.
-   Role required: admin

## Create basic auth credentials

Integrate the ServiceNow instance and the Navex EthicsPoint instance by using the Basic Auth credentials to authenticate ServiceNow requests.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

3.  Select **Basic Auth Credentials**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the record.|
    |User name|User name to be entered as credential.|
    |Password|Password to be entered as credential.|
    |Active|Option to actively use the credential record. Select the option.|
    |Order|Order that the credentials are used. For example, enter `100`.|

5.  Right-click the form header and click **Save**.


## Create connection records

Create connection records to your Navex EthicsPoint instance. The Navex EthicsPoint spoke connection and credential alias uses these connections to perform actions in Navex EthicsPoint instance.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the following records and create connections for each of the record.

    For each connection, you must also [Create basic auth credentials](setup-navex-spoke.md#).

    -   NavexConnection for Attachment
    -   NavexConnection for Case Management
    -   NavexConnection for Lookup List
3.  From the **Connections** tab, click **New**.

4.  On the form, fill in the fields.

    |Field|Value required|
    |-----|--------------|
    |Name|Name to uniquely identify the connection record.|
    |Credential|Basic Auth credential record that you created for Navex EthicsPoint.|
    |Connection alias|Alias record associated with this connection.|
    |Connection URL|URL of the Navex EthicsPoint instance.|
    |Active|Option to actively use the connection. Select the option.|
    |Domain|Domain that the action or activity runs in.|

5.  In the **Attributes** tab, fill in the value in the **Password** and **Username** fields.

6.  Click **Submit**.


