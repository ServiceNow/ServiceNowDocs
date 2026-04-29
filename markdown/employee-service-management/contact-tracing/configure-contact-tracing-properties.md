---
title: Set up Contact Tracing properties
description: Configure system properties to adjust how contact tracing data is used.
locale: en-US
release: australia
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Set up Contact Tracing properties

Configure system properties to adjust how contact tracing data is used.

## Before you begin

Role required: admin

## About this task

Employers remain solely responsible for complying with their legal obligations under applicable law, including data protection laws on collection, use, disclosure, and retention of personal data, and should enable, choose not to enable, or customize any functionality available within the application to meet the Employers’ specific requirements.

**Note:** For system properties associated with tracing systems, see [System properties for tracing systems in Emergency Exposure Management](../../business-continuity/reference/list-of-tracing-system-sys-properties.md).

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Administration** &gt; **Properties**.

2.  Set the following property values.

<table id="table_lxd_w4y_cnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_imt\_tracing.data\_retention\_period**

</td><td>

Number of days after which the data collected for contact tracing is automatically deleted from the system. The retention period is calculated from the last updated date of the data. The retention policy applies to the following contact tracing data:-   Badge swipe data.
-   User daily contact logs, daily log notes, and daily log acknowledgment data.
-   All closed and canceled cases and associated potentially exposed contacts, case tasks, diagnostic requests and the underlying source data, and diagnostic events.

**Note:** A survey associated with cases eligible for deletion after the retention period is not deleted because surveys have their own retention period. For more information, see [Clean up assessment data](https://www.servicenow.com/docs/access?context=t_CleanUpAssessmentData&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

-   Wi-Fi access register data
 The default value is 90.

</td></tr><tr><td id="sysprop_auto_case_task">

**sn\_imt\_tracing.auto\_create\_case\_tasks**

</td><td>

Enables or disables automatic creation of a case task when a case manager adds a potentially exposed contact to a contact tracing case. If the property value is set to Yes, the base system workflow, **Create case tasks for exposed contacts**, triggers the creation of a case task when a potentially exposed contact is added to a case.

 The default value is Yes.

</td></tr></tbody>
</table>3.  Click **Save**.


**Parent Topic:**[Setting up Contact Tracing](../concept/set-up-contact-tracing.md)

