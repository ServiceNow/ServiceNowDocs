---
title: Properties installed with Workplace Visitor Management
description: There are several properties available with Workplace Visitor Management.
locale: en-US
release: yokohama
product: Workplace Visitor Management
classification: workplace-visitor-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, Workplace Visitor Management, Workplace Service Delivery, Employee Service Management]
---

# Properties installed with Workplace Visitor Management

There are several properties available with Workplace Visitor Management.

**Note:** All of these properties are located in the System Properties \[sys\_properties\] table. To access the table, enter `sys_properties.list` in the navigation filter.

<table id="table_hmv_lzr_cnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_wsd\_visitor.policy\_response\_due\_in\_days

</td><td>

This property enables you to send emails to visitors to remind them to submit their visitor policy acceptance or rejection. If a visitor doesn’t respond, the reception staff is notified to check the same when the visitor visits the reception desk. **Note:** The visitor registration isn’t canceled if the visitor doesn’t provide their response toward visitor policy.

-   Type: integer
-   Default value: **1**

</td></tr><tr><td>

sn\_wsd\_visitor.visitor\_inbound\_email

</td><td>

This property enables you to specify a generic email address to send or receive visitor requests.-   Type: string
-   Default value: **askvisitor@example.com**

</td></tr><tr><td>

sn\_imt\_core.visitor\_syncing

</td><td>

This property enables visitor synchronization between the Safe Workplace and Workplace Visitor Management applications.

 When a visitor is registered with the Workplace Visitor Management application, the visitor details are also sent to the Safe Workplace application so that other visitor-related actions can be performed.

 -   Type: true/false
-   Default value: **true**
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_wsd\_visitor.default\_badge\_template

</td><td>

This property specifies the sys\_id of the badge template that is used if no badge is found in the location hierarchy of the visitor registration.

 The default value is the sys\_id of the **Visitor Badge \(Black and White\)** template.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Visitor Management references](../concept/workplace-visitor-mgmt-references.md)

**Related topics**  


[Components installed with Workplace Visitor Management](components-installed-with-workplace-visitor-mgmt.md)

[Kiosk Check-in Flow Configuration form](kiosk-check-in-config-form.md)

[Kiosk Check-out Flow Configuration form](kiosk-check-out-config-form.md)

[Kiosk Page Configuration form](kiosk-page-config-form.md)

[Kiosk Page Customizations](kiosk-page-customizations.md)

[Location Policy form](location-policy-form.md)

