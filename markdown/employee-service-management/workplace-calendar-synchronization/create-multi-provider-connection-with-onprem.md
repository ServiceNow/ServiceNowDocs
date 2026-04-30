---
title: Create single or multiple providers with Microsoft Exchange On-Premises
description: Configure single or multiple providers to the Microsoft Exchange On-Premises calendar provider.
locale: en-US
release: zurich
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Microsoft Exchange On-Premises - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Create single or multiple providers with Microsoft Exchange On-Premises

Configure single or multiple providers to the Microsoft Exchange On-Premises calendar provider.

## Before you begin

[Connect Microsoft Exchange On-Premises MID server with ServiceNow](connect-on-premise-mid-server-with-servicenow.md)

Role required: admin

## Procedure

1.  Create connection and credential aliases.

    For multiple connections, create separate connection and credential records.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential aliases**.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name for the connection and credential alias.|
        |ID|The field is automatically generated after you save the form based on the specified **Name**.|
        |Application|Ensure that the application is set as **Microsoft Exchange Online Spoke**|
        |Parent alias|Select **sn\_exchange\_spoke.Exchange\_https**.|

    4.  Select **Submit**.

        The Connection and Credential alias record is created. As the next step, you must create a Basic Auth credential record.

2.  Create a Basic Auth credential to use in the newly created connection and credential alias records.

    For multiple connections, create a separate credential record.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Select **New**.

    3.  In the **What type credentials would like to create?** section, select **Basic Auth Credentials**.

    4.  Enter a **Name**.

    5.  Enter your **username** and **password**.

    6.  Select **Submit**.

3.  Configure connections to the connection and credential alias.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential aliases**.

    2.  Select the connection and credential alias record that you created in the initial steps.

        Depending on how you want to add connections, select the appropriate alias record.

    3.  On the form, in the **Connections** related list, select **New**.

    4.  On the form, fill in the fields.

<table id="table_ns5_4tf_15b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name to identify the record. For example, `Exchange on prem Connection`.

</td></tr><tr><td>

Credential

</td><td>

Select a credential record that you created. If you created multiple credentials, select the appropriate credential for this connection.

</td></tr><tr><td>

Connection alias

</td><td>

The connection alias is automatically filled with the connection and credential alias to which you are adding this connection.

</td></tr><tr><td>

URL builder

</td><td>

**Note:** Do not select the check box.

</td></tr><tr><td>

Connection URL

</td><td>

Connection URL. Enter `https://exchange2016.newlab.service-now.com/EWS/Exchange.asmx`.

</td></tr><tr><td>

Use MID server

</td><td>

Select the check box. An **Advanced MID Server Configuration** tab opens.

</td></tr><tr><td>

Active

</td><td>

Option to activate the connection.

</td></tr></tbody>
</table>    5.  In the **Advanced MID Server Configuration** tab, do the following:

        -   In the **MID Selection** field, select **Specific MID Server**.
        -   In the **MID Server** field, select your server from the lookup list.
    6.  Select **Submit**.

        The connection is added to the alias. Depending on the number of connections you want to add, repeat the steps.

4.  Configure calendar providers.

    Create a single provider or multiple providers for on-premises. If you want to create

    1.  Navigate to **All** &gt; **Workplace Calendar Synchronization** &gt; **Configurations** &gt; **Calendar Providers**.

    2.  Select **New**.

    3.  Fill in the form fields.

<table id="table_p1m_wdv_txb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter the name of the provider. For example: On Premises

</td></tr><tr><td>

Description

</td><td>

Enter a short description.

</td></tr><tr><td>

Active

</td><td>

Option to activate the On-premises calendar provider.

</td></tr><tr><td>

Calendar processor

</td><td>

Calendar processor for the synchronization. Select **Microsoft EWS** as the processor from **Provider Configuration**.

</td></tr><tr><td>

Override alias?

</td><td>

Option to enable selection of your own connection and credential alias from **Provider Configuration**. If the option is not enabled, then the default connection and credential alias is used.

</td></tr><tr><td>

Connection &amp; credential alias

</td><td>

Select the connection and credential alias that you created on your own for the calendar provider from **Provider Configuration**. This option appears only if you have selected the **Override alias?** option. If an alias is not specified, then the default connection and credential alias is used.

</td></tr><tr><td>

Page size

</td><td>

Page size of the calendar items. You can set the page size from 1 to 500.

</td></tr><tr><td>

Sync batch size

</td><td>

Size of batches during a synchronization. This field is automatically set to **500**, which means a sync batch handles 500 items at a time. If there are more than 500 items, the rest is displayed in the next sync batch.

</td></tr><tr><td>

Sync batch interval

</td><td>

Time interval between sync batches. This field is automatically set to **60** seconds.

</td></tr><tr><td>

Synchronize attendees

</td><td>

Enable this option to synchronize attendees as well while synchronizing reservations.

</td></tr><tr><td>

Sync start date time

</td><td>

the start date and time of the synchronization. The sync generates information from this date.

</td></tr><tr><td>

Sync end date time

</td><td>

End date and time of the synchronization. The sync generates information until this date. The recommended setting is at least 5 years from the **Sync start date time**,

</td></tr><tr><td>

Strict mode

</td><td>

Select the option to enable strict mode.If you enable this option, events are not directly created in the employee's calendar, instead, they are sent to a general email address. Employees are invited to the event. They can only make changes using the Workplace Reservation Management application.

</td></tr><tr><td>

Strict mode email

</td><td>

Strict mode email address used to create reservations and to receive reservation-related notifications. Employees are considered as invitees in the reservation.

</td></tr><tr><td>

Sync past reservations

</td><td>

Select the option to synchronize all the past reservations from the specified **Sync start date time** to the current date.**Note:** Ensure that the reservations that you want to sync from the past are not above 1000. If in cases the expected number of past events are more than 1000, it is recommended to modify the system property **sn\_wsd\_rsvsync.ewsPastSyncPeriodInMonths**. Specify the value in months keeping in mind the expected past reservations. A single sync syncs reservations from those many months. Ensure that the specified number of months do not have more than 1000 reservations.

</td></tr></tbody>
</table>    4.  Select **Submit**.

        The On-premises calendar provider is created. Repeat Step 4 to add another calendar provider.


## Result

Multiple connections and providers are created.

