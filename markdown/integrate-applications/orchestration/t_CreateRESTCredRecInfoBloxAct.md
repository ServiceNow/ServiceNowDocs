---
title: Create a REST credential for Infoblox activities
description: All Infoblox activities require a REST credential to manage IP addresses from the Infoblox DDI server.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Infoblox DDI activity pack, Orchestration activity packs, Classic Orchestration, Data and Automation]
---

# Create a REST credential for Infoblox activities

All Infoblox activities require a REST credential to manage IP addresses from the Infoblox DDI server.

## Before you begin

Before starting this procedure, make sure you have the following:

-   A properly configured and running Infoblox DDI Grid Server.
-   REST credentials defined on the Infoblox DDI server.

Role required: admin

## About this task

You must create a REST credential record on the ServiceNow instance that each Infoblox activity can use to access management features on the Infoblox server.

## Procedure

1.  Navigate to **All** &gt; **Orchestration** &gt; **Credentials** and click **New**.

2.  In the list of credential types, select **Basic Auth Credentials**.

3.  Create the credential record with a logical name, such as **InfobloxCred**.

4.  Right-click in the header bar of your new credential record and select **Copy sys\_id** from the context menu.

    Follow browser instructions to copy the sys\_id if browser security measures restrict this function.

5.  Paste the sys\_id into the **restCredentials** input field of each activity you use.


**Parent Topic:**[Infoblox DDI activity pack](../concept/c_InfobloxDDIActivityPack.md)

