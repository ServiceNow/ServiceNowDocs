---
title: Configure ServiceNow access control
description: Configure an access control record to specify one or more Customer Service and Support employees who have permission to log in your instance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ServiceNow access control, Access Management]
---

# Configure ServiceNow access control

Configure an access control record to specify one or more Customer Service and Support employees who have permission to log in your instance.

## Before you begin

Role required: admin

## About this task

**Note:** The SNC Access Control \(com.snc.snc\_access\_control\) plugin prevents Customer Service and Support personnel from accessing the instances without your express permission. However, other authorized ServiceNow Operations personnel, in their capacity to support and manage the product, are required to perform administrative actions on the underlying infrastructure. This infrastructure includes servers and databases, among other infrastructure components that make up the SaaS solution. This access method is fully auditable and tracked.

This plugin enables you to restrict access to your instance without your express permission, so it may affect support service levels and the Availability SLA. Availability SLA is then measured from the time that Support staff personnel are granted access to your instance.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **SNC Access Control**.

2.  Click **New**.

3.  Fill in the form fields \(see table\).

4.  Click **Submit**.

<table id="table_xgv_vj2_p5"><thead><tr><th>

Form fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Names each Customer Service and Support employee who has permission to log in this instance.

-   Express the names as firstname.lastname in lower case letters, separated by a period \(for example, `john.smith`\). Each name must have a corresponding user record in **support.servicenow.com**.
-   If more than one Customer Service and Support employee has permission to log in this instance, enter multiple names and separate them by commas.
-   To enable all Customer Service and Support employees login rights to access the instance, enter an asterisk \(**\***\) in place of the name.
-   If you intend on restricting Customer Service and Support employee access to the instance, the values in the **Name** field must not have an asterisk \(**\***\) anywhere in the field.


</td></tr><tr><td>

Reason

</td><td>

Human-readable field that describes why you are granting access permission. This field is optional.

</td></tr><tr><td>

Start

</td><td>

Specifies the start date and time of the period during which the specified Customer Service and Support employees have login access. This field is mandatory.

</td></tr><tr><td>

End

</td><td>

Specifies the ending date and time of the period during which the specified Customer Service and Support employees have login access. This field is mandatory.

</td></tr><tr><td>

Active

</td><td>

Controls whether this permission record is active. The default is Active.

</td></tr></tbody>
</table>
