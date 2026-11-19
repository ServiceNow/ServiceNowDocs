---
title: Create a parameter value record
description: Create a Desktop action parameter value record to store the value that an AI agent retrieves during desktop action execution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/configure-parameter-value-record.html
release: zurich
topic_type: task
last_updated: "2026-05-25"
reading_time_minutes: 1
breadcrumb: [Enable AI agents to securely access parameters, Defined desktop actions, Configure, AI Desktop Actions, Enable AI experiences]
---

# Create a parameter value record

Create a Desktop action parameter value record to store the value that an AI agent retrieves during desktop action execution.

## Before you begin

Perform this task in the ServiceNow instance.

At least one Desktop action parameter record must exist.

Role required: sn\_aia.admin or now\_assist\_panel\_user

**Note:**

For shared parameters, only users with the sn\_aia.admin role can create Desktop action parameter value records.

## Procedure

1.  Navigate to **All** &gt; **AI Desktop Actions** &gt; **Desktop Action Parameters**.

2.  Select the Parameter record for which you want to store a value.

3.  In the Desktop action parameter values related list, select **New**.

4.  Fill in the following fields.

<table id="table_zht_ssg_jjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Read-only. Inherited from the parent Desktop action parameter record.

</td></tr><tr><td>

User

</td><td>

The user this value record belongs to. Defaults to the user creating the record. Users with the sn\_aia.admin role can change this field to assign the value record to a different user. **Note:**

This field is not shown for shared parameters.

</td></tr><tr><td>

Value

</td><td>

Enter the value the agent retrieves at execution time, such as a username, password, or other credential.**Note:**

The **Value** field displays as plain text or encrypted text depending on the **Mark As Sensitive** setting on the parent parameter record.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Result

The Desktop action parameter value record is created and appears in the Desktop action parameter values related list on the Parameter record.

