---
title: Define default instructions for ServiceNow AI Lens
description: Create a system property to define default instructions for ServiceNow AI Lens execution on a specific form.
locale: en-US
release: zurich
product: ServiceNow Lens
classification: servicenow-lens
topic_type: task
last_updated: "2025-05-29"
reading_time_minutes: 1
breadcrumb: [Configure, ServiceNow AI Lens, Enable AI experiences]
---

# Define default instructions for ServiceNow AI Lens

Create a system property to define default instructions for ServiceNow AI Lens execution on a specific form.

## Before you begin

Role required: admin

## About this task

You can define default instructions for specific forms to create or update records using ServiceNow AI Lens in a ServiceNow instance. This helps streamline the request process by eliminating the need for users to manually enter the same instructions each time. The defined instructions are automatically included in all ServiceNow AI Lens requests for that form or table.

When users provide additional instructions through the ServiceNow AI Lens UI, those instructions are appended to the default instructions. If there is a conflict between user input, application-generated instructions, and system-defined defaults, ServiceNow AI Lens instructs the LLM to prioritize the user-provided input.

## Procedure

1.  In the filter navigator, enter **sys\_properties.list** and press **Enter**.

2.  Select **New**.

3.  On the System Property form, fill in the details.

<table id="table_gwc_cn3_mfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

sn\_lens.prompt.&lt;tablename&gt;Replace &lt;tablename&gt; with the internal name of the table. For example, sn\_lens.prompt.incident.

</td></tr><tr><td>

Value

</td><td>

Enter the default instructions. For example - Suggest a suitable start date for this incident based on the incidence type and urgency.

</td></tr></tbody>
</table>4.  Select **Submit**.


