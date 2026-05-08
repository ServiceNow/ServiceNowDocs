---
title: Connect Microsoft Exchange On-Premises MID server with ServiceNow
description: Configure connection between the MID server of Microsoft Exchange On-Premises and ServiceNow to synchronize reservations.
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a normal mode connection for Microsoft Exchange On-Premises, Microsoft Exchange On-Premises - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Connect Microsoft Exchange On-Premises MID server with ServiceNow

Configure connection between the MID server of Microsoft Exchange On-Premises and ServiceNow® to synchronize reservations.

## Before you begin

Ensure the following:

-   Install Microsoft Exchange Server Spoke.
-   Set up the Microsoft Exchange Server spoke
-   You must have the Microsoft Exchange Server login credentials.
-   A user is configured in the ServiceNow® instance with the role mid\_server.

Role required: admin

## Procedure

1.  Download the MID server from your ServiceNow® instance on the system where the Microsoft Exchange Server is hosted.

    1.  Navigate to **All** &gt; **MID Server** &gt; **Downloads**.

    2.  Select and download the suitable MID server.

2.  Go to your system's **Downloads** folder and unzip the file.

3.  Open &gt; **agent** &gt; **config.xml**.

4.  In the config.xml file, do the following:

    1.  Specify your ServiceNow® instance details in `<parameter name="url" value="https://YOUR_INSTANCE.service-now.com/"/>`.

    2.  Enter the credentials of the user with the mid\_server role in `<parameter name="mid.instance.username" value="YOUR_INSTANCE_USER_NAME_HERE"/>` and `<parameter secure="true" name="mid.instance.password" value="YOUR_INSTANCE_PASSWORD_HERE"/>`.

        Enter the credentials of the user with the mid\_server role.

    3.  Enter a unique name in `<parameter name="name" value="YOUR_MIDSERVER_NAME_GOES_HERE"/>.`

    4.  Save the file.

5.  After performing the changes, start or run the MID server.

6.  Open ServiceNow® instance.

    **Note:** Ensure that you are logged in as an admin.

7.  Navigate to **All** &gt; **MID Server** &gt; **Servers**.

    You notice that the mid server that you configured is created.

8.  Select the MID server to open.

    On the form, initially, you notice that the **Status** is set to **Down** and the **Validated** field is set to **No**.

9.  To validate the server, in the Related links, select **Validate**.

    After a few seconds, the server is validated. The **Status** is set to **Up** and the **Validated** field is set to **Yes**.


## Result

A platform is set to communicate with the Microsoft Exchange On-Premises MID server and ServiceNow® instance.

## What to do next

[Create a Connection and credential alias for Microsoft Exchange On-Premises](create-a-connection-and-credential-alias-for-ms-exch-onprem.md)

