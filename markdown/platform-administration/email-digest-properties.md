---
title: Email digest properties
description: Several properties are available to manage digest intervals for email digests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/email-digest-properties.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Email properties, Configure, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Email digest properties

Several properties are available to manage digest intervals for email digests.

The following properties are available for the [email digest feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/email-digests.md).

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_ant_ppl_rbb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.email.digest.default\_interval

</td><td>

The sys\_id of the default email digest interval available to users.-   **Type**: string
-   **Default value**: 28d157e07f1332007f005212bdfa9116
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

glide.email.digest.max\_intervals

</td><td>

The maximum number of email digest intervals that can be defined. -   **Type**: integer
-   **Default value**: 100
-   **Location**: System Property \[sys\_properties\] table
-   **Learn more**: For details on digest intervals, see [Create or modify email digest intervals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/create-digest-intervals.md).

</td></tr></tbody>
</table>**Parent Topic:**[Email properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_EmailProperties.md)

**Related topics**  


[Outbound email configuration]()

[Inbound email configuration]()

[Email image filtering properties]()

[Advanced email properties]()

