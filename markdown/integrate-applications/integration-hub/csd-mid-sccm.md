---
title: Configure the MID Server for SCCM activities
description: To use a MID Server with Microsoft System Center Configuration Management \(SCCM\) activities, configure it to communicate with the SCCM server.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring SCCM, Client software distribution from SCCM, Client Software Distribution using Integration Hub, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Configure the MID Server for SCCM activities

To use a MID Server with Microsoft System Center Configuration Management \(SCCM\) activities, configure it to communicate with the SCCM server.

## Before you begin

Role required: admin.

## Procedure

1.  In the navigation filter, enter **cmdb\_ci\_dns\_name.list**.

2.  Click **New**.

3.  Enter the fully-qualified domain name \(FQDN\) of the SCCM server in the **Name** field.

4.  Right-click in the form header and select **Save**.

5.  In the **IP Address** related list, click **New**.

6.  In the **IP Address** field, enter the IP address of the SCCM server.

7.  In the **Nic** field, select **eth0** or your preferred network interface controller.

8.  Leave the **Netmask** field blank.

9.  Click **Submit**.


**Parent Topic:**[Configuring SCCM](../concept/configure-sccm-ihub.md)

