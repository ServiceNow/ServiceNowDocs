---
title: Set up the Redox Electronic Health Record Spoke
description: Integrate your ServiceNow instance and the Redox engine with both inbound and outbound configuration.Enable your ServiceNow instance to connect with the Redox engine by setting up a connection and credential record.Enable the Redox Electronic Health Record Spoke to send data to the external Redox healthcare system by configuring the source and destination IDs of the system in your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Redox Electronic Health Record Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Redox Electronic Health Record Spoke

Integrate your ServiceNow instance and the Redox engine with both inbound and outbound configuration.

## Before you begin

**Important:**

Starting with the Yokohama release, Redox Electronic Health Record Spoke is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

-   Request an Integration Hub subscription.
-   Ensure you have the admin access to the Redox engine dashboard [https://dashboard.redoxengine.com/\#/login](https://dashboard.redoxengine.com/#/login).
-   Activate the Redox Electronic Health Record Spoke.
-   Role required: admin.

## About this task

This task gives the procedure to set up both the inbound and outbound transactions between your ServiceNow instance and the Redox engine. After you configure the inbound transactions, the Redox engine can make calls to the ServiceNow REST Application Programming Interface \(API\). The outbound setup enables the ServiceNow instance to get authenticated and connect with the Redox engine.

## Procedure

1.  [Create a Redox Electronic Health Record Spoke connection and credential record](redox-setup.md#).

    This procedure enables the outbound transactions.

2.  [Configure the external Redox healthcare system as a source system for the Redox Electronic Health Record Spoke](redox-setup.md#).

    This procedure enables the inbound transactions.


## Create a Redox Electronic Health Record Spoke connection and credential record

Enable your ServiceNow instance to connect with the Redox engine by setting up a connection and credential record.

### Before you begin

**Important:**

Starting with the Yokohama release, Redox Electronic Health Record Spoke is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Role required: admin

### Procedure

1.  Log in to your ServiceNow instance.

2.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

3.  On the Flow Designer page, select Connections.

4.  In the Search all connections field, enter `Redox`.![Enter Redox spoke name in search field.](../image/redox-spoke-search-redox.png)

5.  On the Redox Electronic Health Record Spoke card, click **View Details**.

6.  Click **Configure**.![Redox connection and credential configure button.](../image/redox-configure-button.png)

7.  In the Configure Connection form, fill details.

<table id="table_xd2_qht_lnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection.**Note:** If you're creating the first record, then Redox Electronic Health Record Spoke is the default name and it's read-only. If you create any record after that, you can provide custom connection name.

</td></tr><tr><td>

Connection URL

</td><td>

The URL to connect to the Redox engine. Enter [https://api.redoxengine.com/](https://api.redoxengine.com/).

</td></tr><tr><td>

Name

</td><td>

Name of the Redox Electronic Health Record Spoke credential. The default name is Redox credential but you can update it.

</td></tr><tr><td>

API Key

</td><td>

The API key to access the Redox engine dashboard. You must generate the key on the Redox engine dashboard [https://dashboard.redoxengine.com/\#/login](https://dashboard.redoxengine.com/#/login). **Tip:** To learn how to generate the API key, see the Redox developer documentation.

</td></tr><tr><td>

Secret

</td><td>

The source secret to access the Redox engine dashboard. You must generate the secret on the Redox engine dashboard [https://dashboard.redoxengine.com/\#/login](https://dashboard.redoxengine.com/#/login). **Tip:** To learn how to generate the secret, see the Redox developer documentation.

</td></tr></tbody>
</table>8.  Click **Configure Connection**.

    The connection and credential record is created.

9.  Click **View connection alias**.![View connection alias button on Redox spoke record.](../image/redox-spoke-click-connection-alias.png)

10. In the **Credential** column, select **Redox Credential**.![Credential column value in the Connections tab.](../image/redox-spoke-click-creds.png)

11. On the Redox credential page, click **Get Token** to generate a token for raising authenticated requests from the spoke actions.


## Configure the external Redox healthcare system as a source system for the Redox Electronic Health Record Spoke

Enable the Redox Electronic Health Record Spoke to send data to the external Redox healthcare system by configuring the source and destination IDs of the system in your ServiceNow instance.

### Before you begin

**Important:**

Starting with the Yokohama release, Redox Electronic Health Record Spoke is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Role required: admin

### Procedure

-   Configure the Source system \[sn\_hcls\_source\_system\] table to send data to an external Redox healthcare system by using the Redox Inbound Integration application.

    For more information, see [Configure an external Redox healthcare system as a source system for a custom integration](https://www.servicenow.com/docs/access?context=hcls-config-source-system&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US).

-   Specify the destination ID used in the Source system \[sn\_hcls\_source\_system\] table for each spoke action in your flow.


