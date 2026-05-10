---
title: Set up Metrikus spoke
description: Integrate the ServiceNow instance and Metrikus Spoke. Create a connection and credential alias in the Metrikus spoke to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Metrikus spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Metrikus spoke

Integrate the ServiceNow instance and Metrikus Spoke. Create a connection and credential alias in the Metrikus spoke to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Ensure that you have activated the Metrikus Spoke plugin dependencies.
-   Activate the Metrikus Spoke plugin \(sn\_wsd\_metrikus\_spoke\).
-   Metrikus Client ID and Client secret key.
-   Role required: admin.

## Integrate Metrikus with your ServiceNow instance

Create the connection records to your Metrikus account. The Metrikus Spoke connection and credential aliases use these connections to perform actions in Metrikus.

## Procedure

1.  Navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials** &gt; **Metrikus**.

2.  Select the **Create New Connections &amp; Credential** related link.

3.  On the form, fill in the fields:

<table id="table_k3k_f4k_x1c"><thead><tr><th>

Field

</th><th>

Description and value required

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to identify the connection. This field is automatically set to Metrikus Spoke connection.

</td></tr><tr><td>

Connection URL

</td><td>

The URL to make connection to the spoke. This field is automatically set to [https://nextgen-api.metrikus.io](https://nextgen-api.metrikus.io).

</td></tr></tbody>
</table>    |Field|Description and value required|
    |-----|------------------------------|
    |Credential Name|Name of the Metrikus Spokec credential. For example, **Metrikus Credential**|
    |Token URL|Token URL address [https://nextgen-api.metrikus.io/oauth/token](https://nextgen-api.metrikus.io/oauth/token).|
    |OAuth Client ID|Client ID of the Metrikus application to register in the registration portal.|
    |OAuth Client Secret|Client Secret key that is generated while registering the Metrikus application in the Metrikus portal.|

4.  Select **Create and Get OAuth Token**.

    The Metrikus Spoke is set up and integrated with your ServiceNow® Store instance.


## What to do next

Navigate to **All** &gt; **Workplace Connectors** &gt; **Provider Connector Configuration** table. The Workplace Core locations provided in this table are mapped with the external Ids provided by Metrikus. The external IDs provided by Metrikus are transformed to retrieve workplace occupancy data in Workplace Connectors Space Occupancy Data table.

