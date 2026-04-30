---
title: Provider form
description: The Provider form includes calendar provider details and provider configuration field details.
locale: en-US
release: zurich
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Provider form

The Provider form includes calendar provider details and provider configuration field details.

<table id="table_u2w_vs2_22c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the calendar provider.

</td></tr><tr><td>

Description

</td><td>

Description of the calendar provider.

</td></tr><tr><td>

Active

</td><td>

Option to activate the calendar provider.

</td></tr><tr><td>

Calendar processor

</td><td>

Calendar processor for the synchronization. Select **Microsoft Graph** from the **Provider Configuration** tab.

</td></tr><tr><td>

Override alias?

</td><td>

Option to enable the selection of your own connection and credential alias from the **Provider Configuration** tab. If the option isn’t enabled, then the default connection and credential alias are used

</td></tr><tr><td>

Connection &amp; credential alias

</td><td>

Select the connection and credential alias that you created on your own for the calendar provider. This option appears only if you have selected the **Override alias?** option. If an alias isn’t specified, then the default connection and credential alias are used

</td></tr><tr><td>

Sync start date time

</td><td>

The start date and time of the synchronization. The synchronization generates information from this date. Specify the **Sync start date time** manually from the subscription record of the reservable sync record that you’re syncing the past reservations for.**Important:** The past sync duration must not exceed 1825 days.

</td></tr><tr><td>

Sync end date time

</td><td>

End date and time of the synchronization. The sync generates information until this date. You should set this date to at least 5 years from the **Sync start date time**.**Important:** The past sync duration must not exceed 1825 days.

</td></tr><tr><td>

Delegated user email

</td><td>

Delegated user email address that is used to create reservations and to receive updates on room calendars as notifications.**Note:** If multiple delegated users manage multiple rooms, a separate calendar provider record must be created for each user to manage their respective rooms. This process requires retrieving individual tokens for each user, creating separate connections and credential aliases, and mapping them to the respective calendar provider.

</td></tr></tbody>
</table>