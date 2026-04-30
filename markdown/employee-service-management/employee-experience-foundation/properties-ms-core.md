---
title: Properties installed with Microsoft Integrations Core
description: The following properties are installed with the Microsoft Integrations Core plugin.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Properties installed with Microsoft Integrations Core

The following properties are installed with the Microsoft Integrations Core plugin.

**Note:** The following properties are located in the System Properties \[sys\_properties\] table. To access the table, enter `sys_properties.list` in the navigation filter.

<table id="table_hqx_h2w_y1c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_now\_teams.st\_activity\_oauth\_profile

</td><td>

Sys\_id of the OAuth profile used for single tenant setup.-   Type: string
-   Default value: none

</td></tr><tr><td>

sn\_now\_teams.link\_unfurl.view\_action\_choice

</td><td>

When the link unfurls in Microsoft Teams, provide an option to open URLs for the portal configured within the Teams tab in the app or in a browser. The options are displayed when a user selects the **View** action on the card.-   Type: true\|false
-   Default value: true

</td></tr><tr><td>

sn\_now\_teams.actionable\_notification\_approve\_or\_reject\_reason\_mandatory

</td><td>

Use this property to set the approval note or the reject reason as mandatory for actionable notifications sent in Microsoft Teams.-   Type: true\|false
-   Default value: false

</td></tr><tr><td>

sn\_now\_teams.portal.suffix

</td><td>

Use this property to set the portal to be embedded in Microsoft Teams when a user goes to **Your Hub** or **Employee Center**. You must enter the URL suffix of the portal that you want to use.-   Type: string
-   Default value: none

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow for Microsoft Teams reference](reference-sn-teams.md)

