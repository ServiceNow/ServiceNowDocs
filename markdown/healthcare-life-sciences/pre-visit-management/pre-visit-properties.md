---
title: Pre-Visit Management properties
description: There are several advanced Pre-Visit Management properties that you can configure to schedule a pre-visit procedure for a patient.
locale: en-US
release: australia
product: Pre-Visit Management
classification: pre-visit-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Pre-Visit Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Pre-Visit Management properties

There are several advanced Pre-Visit Management properties that you can configure to schedule a pre-visit procedure for a patient.

**Important:**

Starting with the Yokohama release, Pre-Visit Management is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

These properties are available for Pre-Visit Management.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_rdv_m43_tqb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number of days before the procedure appointment date when the procedure consent form is sent to the patient for review or signature

 sn\_previsit.procedure\_consent\_lead\_time

</td><td>

Set to numeric value to indicating the number of days before the procedure appointment date when the procedure consent form is sent to the patient for review or signature.

-   Type: Integer
-   Default value: 3
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Configure when to send the procedure consent form to a patient](../task/pre-visit-config-proc-consent-time.md)

</td></tr></tbody>
</table>**Parent Topic:**[Pre-Visit Management reference](pre-visit-reference.md)

