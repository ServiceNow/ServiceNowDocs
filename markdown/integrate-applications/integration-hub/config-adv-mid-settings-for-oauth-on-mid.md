---
title: Set up MID Server for a spoke
description: Configure MID Server settings on your ServiceNow instance that enables it to integrate with a third-party application via MID Server after you have set up the connection record for a spoke.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-10-14"
reading_time_minutes: 2
breadcrumb: [Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up MID Server for a spoke

Configure MID Server settings on your ServiceNow instance that enables it to integrate with a third-party application via MID Server after you have set up the connection record for a spoke.

Demonstrates setting up MID Server for a spoke. 

## Before you begin

Role required: admin

Confirm that you have set up the connection record for the spoke.

## About this task

Setting up MID Server may be mandatory or optional for the spoke that you set up. For example, configuring MID Server is required for [Microsoft Active Directory v2 Spoke](../concept/ms-ad-v2-spoke.md) but optional for the [Jira Spoke](../concept/jira-spoke-v3-0-2.md). Use this procedure to set up the MID Server for your spoke after you have set up your spoke by filling the default connection alias form.

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connection &amp; Credential Alias**.

2.  Find the connection and credential alias of the spoke.

    Search the alias by entering its name in the **Name** field.![Enter alias name in the Name field.](../image/search-conn-alias.png)

3.  Under the **Name** column, select the connection and credential alias.

    ![Select alias from Connection & Credential Aliases.](../image/mid-settings-select-alias.png)

4.  In the **Connections** tab, select the default connection record for the spoke.

    ![New button.](../image/mid-settings-new-button.png)

5.  Select **Use MID server**.

    The **Advanced MID Server Configuration** tab is enabled.

    ![Advanced MID Server Configuration tab.](../image/adv-mid-server-config=tab.png)

6.  Fill the form under the **Advanced MID Server Configuration** tab.

<table id="table_cpw_z5c_zpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MID Selection

</td><td>

Option to select a specific MID Server or MID Cluster. Choose any one of the following options. -   **Auto-Select MID Server**: Your ServiceNow instance selects the MID Server without manual input.
-   **Specific MID Server**: Your ServiceNow instance uses MID Server that you specify.
-   **Specific MID Cluster**: Your ServiceNow instance uses the MID Cluster that you specify.

A MID Cluster is a group of MID Servers that enables your ServiceNow instance to handle multiple integrations, and improve integration speed. For more information, see [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Capabilities

</td><td>

The capabilities the MID Server must support to be eligible for selection. The system runs the action or activity from a MID Server that supports the selected capabilities. Only displays if **Use MID server** is selected. Required capabilities determine which MID Server is selected at runtime. To learn more about how a MID Server is selected during runtime, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

**Note:** This field is visible only when **Auto-Select MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

MID Application

</td><td>

The application the MID Server must support to be eligible for selection. The system runs the action from a MID Server that supports the selected application. Only displays if **Use MID server** is selected. To learn more about how a MID Server is selected during runtime, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

**Note:** This field is visible only when **Auto-Select MID Server** is selected from the MID Selection list.

</td></tr></tbody>
</table>7.  Select **Update**.

    The MID Server is enabled on the connection form of the spoke.

    ![HTTPS form.](../image/mid-settings-https-form.png)


## What to do next

Confirm that the spoke connection form has the Use MID option.

**Parent Topic:**[Building integrations in Integration Hub](../../integrationhub/concept/building-integrations-ih.md)

