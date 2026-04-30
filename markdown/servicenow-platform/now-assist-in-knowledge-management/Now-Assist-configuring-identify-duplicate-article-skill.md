---
title: Configure and activate the Now Assist Identify duplicate articles skill
description: Configure the Knowledge content management skill to enable admins and managers to activate the Now Assist Identify duplicate articles skill.
locale: en-US
release: zurich
product: Now Assist in Knowledge Management
classification: now-assist-in-knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Now Assist in Knowledge Management, Now Assist in Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure and activate the Now Assist Identify duplicate articles skill

Configure the Knowledge content management skill to enable admins and managers to activate the Now Assist Identify duplicate articles skill.

## Before you begin

Role required: knowledge\_admin and knowledge\_manager

## About this task

This skill enables admins and managers to identify and review duplicate content.

## Procedure

1.  Navigate to **All** &gt; **Admin Center** &gt; **Now Assist Admin** &gt; **Now Assist Skills** &gt; **Platform**.

2.  In the Now Assist Skills for Platform list view, scroll down to the Identify duplicate articles skill.

3.  Navigate to the skill configuration page by selecting **Activate**.

4.  In the Choose input section, select **Switch scope** and specify the following fields.

<table id="table_erk_jmw_gfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table name

</td><td>

The table on which the skill is configured. This is a read-only field with a default value.

</td></tr><tr><td>

Fields

</td><td>

Select the fields that will be used to identify duplicate articles. These fields can be configured in both OOB and custom templates. The duplicate detection job will use these configured fields to find duplicate articles.

</td></tr><tr><td>

Filter

</td><td>

Build a filter by adding knowledge related conditions such as Article ID, Base version and, Knowledge base.

</td></tr><tr><td>

Duplicates generation frequency

</td><td>

Set the frequency at which the job for identifying the duplicate articles is run. **Note:**

-   The skill must be reset every time the frequency is set.
-   When you select the **Run once** option and activate the skill, the application runs the job immediately after its activation. Selecting any other option, runs the job soon after its activation and, as per the selected frequency in the subsequent runs.


</td></tr></tbody>
</table>5.  Select **Save and continue**.

6.  Review your inputs in the Review and activate section and select **Done**.


## Result

The Now Assist Identify duplicate articles skill is configured.

**Parent Topic:**[Configuring Now Assist in Knowledge Management](../concept/configuring-now-assist-km.md)

