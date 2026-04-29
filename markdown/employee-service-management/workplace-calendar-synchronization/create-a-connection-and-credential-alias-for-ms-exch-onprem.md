---
title: Create a Connection and credential alias for Microsoft Exchange On-Premises
description: Establish a connection and credential alias for Microsoft Exchange On-Premises so that you can synchronize reservations. Ensure that the values for the connection and credentials alias are set as specified.
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2026-03-23"
reading_time_minutes: 1
breadcrumb: [Create a normal mode connection for Microsoft Exchange On-Premises, Microsoft Exchange On-Premises - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Create a Connection and credential alias for Microsoft Exchange On-Premises

Establish a connection and credential alias for Microsoft Exchange On-Premises so that you can synchronize reservations. Ensure that the values for the connection and credentials alias are set as specified.

## Before you begin

[Connect Microsoft Exchange On-Premises MID server with ServiceNow](connect-on-premise-mid-server-with-servicenow.md)

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Select **Exchange\_https**.

3.  On the form, create a connection.

    1.  In the **Connections** related list, select **New**.

    2.  On the form, enter the following details:

        -   **Name**: Enter a name for the connection.
        -   **Credentials**: Create a credential.
            1.  Select the **Lookup using list** icon.
            2.  On the Credentials window that opens, select **New**.
            3.  In the **What type credentials would like to create?** section, select **Basic Auth Credentials**.
            4.  Enter a **Name**.
            5.  Enter your **username** and **password**.
            6.  Select **Submit**.
        -   In the **Connection alias** field, enter `sn_exchange_spoke.Exchange_https`.
        -   In the **Connection URL** field, enter the URL in the `<hostname>.<domain>.com/EWS/Exchange.asmx` format. Enter the respective host and a fully qualified domain where the Microsoft Exchange Server is installed. For example, `https://exchange2016.newlab.service-now.com/EWS/Exchange.asmx`.
        -   Select the **Use MID server** check box.

            An **Advanced MID Server Configuration** tab opens.

        -   In the **Advanced MID Server Configuration** tab, do the following:
            -   In the **MID Selection** field, select **Specific MID Server**.
            -   In the **MID Server** field, select your server from the lookup list.
        -   Select **Submit**.

## Result

The Connection and Credentials alias is created.

## What to do next

[Configure Microsoft Exchange On-Premises as calendar provider](configure-ms-exchange-on-prem-as-calendar-provider.md)

