---
title: Install the application and configure a server for the McAfee ePO integration
description: Before you invoke the workflows for the integration, install and configure the McAfee ePO application from the ServiceNow Store on your ServiceNow AI Platform instance. The configuration is required to connect to the McAfee ePO console.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install the application and configure a server for the McAfee ePO integration

Before you invoke the workflows for the integration, install and configure the McAfee ePO application from the ServiceNow Store on your ServiceNow AI Platform instance. The configuration is required to connect to the McAfee ePO console.

## Before you begin

Role required: ServiceNow AI Platform administrator \(admin\)

## About this task

The integration supports multiple servers, however, to avoid conflicts in profiles that share the same triggering conditions, you cannot share a McAfee ePO capability with multiple profiles that use the same McAfee ePO server. For example, as shown in the following figure, you can have capability 1 in more than one profile as long as each McAfee ePO server is mapped to a unique profile that has capability 1.

![Shared profile limitations.](../image/mcafee-shared-profile.png "McAfee Shared Profile limitations")

## Procedure

1.  Download the McAfee ePO for Security Operations from the ServiceNow Store and install it.

2.  Navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

3.  Search for the McAfee ePO for Security Operations integration tile, and click **Configure**.

    ![McAfee ePO Integration tile.](../image/mcafee-config-tile.png)

4.  On the form, fill in the fields.

<table id="table_evw_xjl_gxd"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the integration, for example, `demo-1`.

</td></tr><tr><td>

ePO Server Name

</td><td>

Name for the McAfee ePO server. If you use one server, an example is, `McAfee HQ` \(McAfee Head Quarters\). This name is how the server and related credentials are recognized.If your organization requires support for multiple servers, enter the name for each server and repeat the process.

</td></tr><tr><td>

McAfee ePO REST API URL

</td><td>

Base URL hosting the McAfee ePO REST API. Enter the URL with the https:// protocol, for example, `https://corp.epo_server:8443`.

</td></tr><tr><td>

API account username

</td><td>

Unique account username, for example, `ServiceNow API`.

</td></tr><tr><td>

API account password

</td><td>

Unique password for the API account.

</td></tr><tr><td>

MID Server

</td><td>

Select the name of the MID Server that you configured during the setup of your ServiceNow AI Platform instance. You can select a specific MID Server from the list or select **Any** to enable an auto-selection of a valid MID Server from the list for this integration.

**Note:**

-   The MID Server selected during this configuration time applies throughout this integration.
-   Only MID Servers that are active and validated are displayed on this list. By default, the value is set to **Any**.
An example name is, `secops_local_midserver`.

</td></tr></tbody>
</table>    ![McAfee ePO Integration Configuration settings](../image/mcafee-epo-configtile.png "McAfee ePO Integration Configuration")

5.  Click **Submit**.

    The McAfee ePO Configurations list is displayed with your new configuration record. You have successfully completed the configuration for a McAfee ePO server.

    **Note:** If your organization requires support for multiple servers, then repeat the steps.


**Parent Topic:**[McAfee ePO integration](../concept/mcaffee-epo-overview-arch.md)

**Previous topic:**[Set up your McAfee ePO console to integrate with Security Incident Response \(SIR\)](mcafee-epo-setup-mcafee.md)

**Next topic:**[Edit security tags in the ServiceNow AI Platform for the McAfee ePO integration](mcafee-epo-match-tags.md)

