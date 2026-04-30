---
title: Configure MID Server for Exchange
description: Configure a MID Server with defined IP ranges to use Exchange.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exchange activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure MID Server for Exchange

Configure a MID Server with defined IP ranges to use Exchange.

## Before you begin

Role required: admin

## About this task

If the MID Server manages resources within defined IP ranges, instead of all computers on your network, you must perform additional configuration steps to run Exchange activities. You do not need to perform these steps if your MID Server uses the default configuration.

## Procedure

1.  In the navigation filter, enter `cmdb_ci_dns_name.list`.

2.  Click **New**.

3.  Enter the fully-qualified domain name \(FQDN\) of your Exchange server in the **Name** field.

4.  Right-click the form header and select **Save**.

5.  In the **IP Address** related list, click **New**.

6.  In the **IP Address** field, enter the IP address of your Exchange server.

7.  In the **Nic** field, select **eth0** or your preferred network interface controller.

8.  Leave the **Netmask** field blank.

9.  Click **Submit**.


**Parent Topic:**[Exchange activity pack](../concept/c_OrchestrationExchangeActivities.md)

