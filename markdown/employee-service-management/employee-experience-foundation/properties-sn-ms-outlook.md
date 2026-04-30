---
title: Properties installed with ServiceNow for Microsoft Outlook
description: The following properties are installed with the Outlook Actionable Messages plugin.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, ServiceNow for Microsoft Outlook, Unified Employee Experience, Employee Service Management]
---

# Properties installed with ServiceNow for Microsoft Outlook

The following properties are installed with the Outlook Actionable Messages plugin.

**Note:** The following properties are located in the System Properties \[sys\_properties\] table. To access the table, enter `sys_properties.list` in the navigation filter.

<table id="table_xmf_3yv_w1c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_ms\_oam.feedback\_survey\_question\_count

</td><td>

Use this property to set a limit for the number of questions to be displayed on a survey card. If the number of questions exceeds this value, the survey opens in the portal specified by the **sn\_ms\_oam.portal.suffix** property.-   Type: integer
-   Default value: 2

</td></tr><tr><td>

sn\_ms\_oam.portal.suffix

</td><td>

Use this property to set the portal in which the survey opens if the questions exceed the value of the **sn\_ms\_oam.feedback\_survey\_question\_count** property. You must enter the URL suffix of the portal that you want to use.-   Type: string
-   Default value: esc

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow for Microsoft Outlook reference](sn-ms-outlook-reference.md)

