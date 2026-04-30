---
title: Configure Google as calendar provider
description: Configure Google as calendar provider to start synchronizing reservation. Link it to the connection and credential alias and configure rooms to start synchronizing.
locale: en-US
release: yokohama
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Google Calendar - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure Google as calendar provider

Configure Google as calendar provider to start synchronizing reservation. Link it to the connection and credential alias and configure rooms to start synchronizing.

## Before you begin

Ensure the following:

-   You have created the connection and credential alias. If not, do one of the following:
    -   Configure the default connection and credential alias. Refer to [Create a Connection and credential record for Google](create-connection-configuration-with-google.md).
    -   Create your own connection and credential alias if you do not want to use the default alias. Refer to [Configure your own Google connection and credential alias](../concept/configure-your-own-google-connection-and-credential-alias.md).
-   Application scope is set to **Google Calendar Spoke**. Otherwise, do the following:
    1.  Select the Application scope icon \(![Application scope icon.](../image/application-scope-globe-icon.png)\) on the top-right corner of your Employee Center homepage.
    2.  In the drop- down, select the option consisting **Application scope:**.
    3.  In the filter navigator, search and select **Google Calendar Spoke**.
    4.  Refresh the page.

**Note:** For calendars to synchronize successfully, you must have an email address that matches that of the provider.

Role required: admin

## About this task

Configure Google Calendar as a calendar provider. If you want to use your own alias, enable the **Override alias** option and specify the alias.

## Procedure

1.  Navigate to **All** &gt; **Workplace Calendar Synchronization** &gt; **Configuration** &gt; **Calendar Providers**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_o1q_frp_5nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the calendar service. For example, Google Calendar.

</td></tr><tr><td>

Description

</td><td>

Description of the calendar service.

</td></tr><tr><td>

Active

</td><td>

Option to activate the calendar provider.

</td></tr><tr><td colspan="2">

**Provider Configuration**

</td></tr><tr><td>

Calendar processor

</td><td>

Calendar processor for the synchronization. Select **Google Calendar**.

</td></tr><tr><td>

Override alias?

</td><td>

Option to enable selection of a Connection and credential alias. Select this option if you want to use your own connection and credential alias only. If the option is not selected, the default connection and credential alias, **Google\_Calendar** is used.

</td></tr><tr><td>

Connection &amp; credential alias

</td><td>

Select the Connection and credentials alias that you created on your own. This option appears only if you have selected the **Override alias?** option. If an alias is not specified, then the default connection and credential alias is used.

</td></tr><tr><td>

Page size

</td><td>

Page size of the calendar items.

</td></tr><tr><td>

Sync batch size

</td><td>

Size of batches during a synchronization. This field is automatically set to **500**, which means a sync batch handles 500 items at a time. If there are more than 500 items, the rest is displayed in the next sync batch.

</td></tr><tr><td>

Sync batch interval

</td><td>

Time interval between sync batches. This field is automatically set to **60** seconds.

</td></tr><tr><td>

Sync start date time

</td><td>

The start date and time of the synchronization. The sync generates information from this date.**Important:** The past sync duration must not exceed 1825 days.

</td></tr><tr><td>

Sync end date time

</td><td>

End date and time of the synchronization. The sync generates information until this date. The recommended setting is at least 5 years from the **Sync start date time**.**Important:** The past sync duration must not exceed 1825 days.

</td></tr><tr><td>

Sync past reservations

</td><td>

Select the option to synchronize all the past reservations from the specified **Sync start date time** to the **Sync end date time**.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

Google Calendar is configured as calendar provider.

## What to do next

-   Set the scheduled job, **WSDRS Sync Calendar items** to **True**. The scheduled job is set to **False** by default and it must be enabled to start synchronizing. You can set the scheduled job time as you want. At any time, you can also manually execute it.
-   If you enabled the **Sync past reservations** field, you must perform the following actions:

    1.  Scroll down to Reservable Sync Configurations related list
    2.  In the **Location** column, select location.
    3.  On the Location form, select **Sync Location**.
    Perform Step 2 and Step 3 on all the Reservable sync config records.

-   [Add multiple Reservable Sync Configurations](add-reservable-sync-config.md)

