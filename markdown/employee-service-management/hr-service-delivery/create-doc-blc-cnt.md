---
title: Create block content in Document Templates
description: Each document template block can have multiple block contents. Each content mapping to a condition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/create-doc-blc-cnt.html
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Document blocks in Document Templates, Document Templates of type HTML, Configuring Document Templates, Document Templates, HR Documents, HR Service Delivery, Employee Service Management]
---

# Create block content in Document Templates

Each document template block can have multiple block contents. Each content mapping to a condition.

## Before you begin

Role required: sn\_doc.admin

## About this task

Using document block content in an HTML template:

Consider an employee offer letter template as an example. While most of the content applies to all employees, the leave policy clause may vary by geographical region. In this case, a document block can be created with two block contents, one for each regional leave policy, and added to the body field of the offer letter. This enables dynamic generation of the appropriate leave policy content based on the employee's location.

## Procedure

1.  Navigate to **All** &gt; **Document Templates** &gt; **Document Template Blocks**.

2.  Select a document template block.

3.  In the **Document Templates Block Contents** related list, click **New**.

4.  On the form, fill in the fields:

<table id="table_lld_cps_ypb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Suitable name for the block content.

</td></tr><tr><td>

Block

</td><td>

Name of the document template block to which you want to associate the document block content.

</td></tr><tr><td>

Order

</td><td>

Order in which the conditions are matched. The first block content that matches the condition is considered.

</td></tr><tr><td>

Active

</td><td>

Option to indicate that the block content is available to use.

</td></tr><tr><td>

Applies when

</td><td>

Conditions are applied on the selected table on document template block.

</td></tr><tr><td>

Applies to

</td><td>

User criteria to which the block content is applicable.

</td></tr><tr><td>

Applies to user

</td><td>

User to whom the selected user criteria is applicable.**Note:** If no value is selected in the **Applies when** and **Applies to** fields, then the block content will be applicable for the HTML template irrespective of the user and selected table.

</td></tr><tr><td>

Body

</td><td>

Text that you want to include in the block content.**Note:** The output of the HTML block content is automatically sanitized when the **Sanitize** option is enabled in the HTML template. For more details, refer to the **Sanitize** field in [Configure an HTML document template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/configure-HTML-doc-template.md).

</td></tr></tbody>
</table>5.  Click **Submit**.


