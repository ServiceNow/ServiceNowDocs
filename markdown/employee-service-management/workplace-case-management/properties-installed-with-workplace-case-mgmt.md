---
title: Properties installed with Workplace Case Management
description: Customize the properties available with Workplace Case Management.
locale: en-US
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Properties installed with Workplace Case Management

Customize the properties available with Workplace Case Management.

These properties are available for Workplace Case Management.

**Note:** All of these properties are located in the System Properties \[sys\_properties\] table. To access the table, enter `sys_properties.list` in the navigation filter.

<table id="table_cqn_gcl_kmb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_wsd\_case.wsd\_inbound\_email

</td><td>

Checks for email received for Workplace Case Management.This property is available only for Workplace Case Management version 1.0.1.

 This property will no longer be available if you upgrade to Workplace Case Management version 1.0.2 or later.

 This property is available as sn\_wsd\_core.wsd\_inbound\_email for Workplace Case Management version 1.0.2 and later.

.-   Type: String
-   Default value: askwsd@example.com
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_wsd\_case.acceptance\_timeout

</td><td>

If a Workplace case has 'Enable user acceptance' set to True and no 'Acceptance Timeout' specified, this property applies the default timeout to 172800 seconds \(two days\). -   Type: Integer
-   Default value: 172800 Seconds
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Case Management references](../concept/workpalce-case-mgmt-references.md)

**Related topics**  


[Components installed with Workplace Case Management](components-installed-with-workplace-case-mgmt.md)

[Workplace Service form](workplace-service-form.md)

[Workplace Location Assignment service](location-assignment-service.md)

