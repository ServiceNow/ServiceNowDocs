---
title: Identify and add course items for a virtual coach
description: Define filters and add course items for automated virtual coaching. When a coaching assessment is triggered, the course items are automatically attached to the assessment.
locale: en-US
release: zurich
product: Coaching
classification: coaching
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Coaching, IT Service Management]
---

# Identify and add course items for a virtual coach

Define filters and add course items for automated virtual coaching. When a coaching assessment is triggered, the course items are automatically attached to the assessment.

## Before you begin

Role required: sn\_coaching.admin

## About this task

Typical assigned course item content includes micro trainings, best practices, tips, knowledge articles, videos, and community links.

## Procedure

1.  Navigate to **Coaching** &gt; **Virtual Coach** &gt; **All** and click **New** to create a record.

2.  Fill in the fields on the form.

<table id="table_v1s_sfr_kwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

The table from which a coaching opportunity is generating assessments.

</td></tr><tr><td>

Course Items

</td><td>

Course items you want to associate with the virtual coaching record. This could include a message, a link, a video, or source code.**Note:** The course items are automatically attached to the coaching assessment when the conditions in the virtual coaching record are met.

You can also access course items by navigating to **Coaching** &gt; **Course items**.

</td></tr><tr><td>

Advanced

</td><td>

Enable to set advanced conditions. See [Scripts](https://www.servicenow.com/docs/access?context=c_Script&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) for more information on scripting.

</td></tr><tr><td>

Condition

</td><td>

Set filter conditions that trigger virtual coaching.

</td></tr><tr><td>

Autofill fields

</td><td>

Set one or more fields and the value for each value that you want to automatically populate.

</td></tr></tbody>
</table>
## Coaching admin sets up learning content

<table id="table_oz3_qlb_gfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

CVC0000106

</td></tr><tr><td>

Short Description

</td><td>

Virtual Coach for the Incident Process

</td></tr><tr><td>

Table

</td><td>

Incident \[Incident\]

</td></tr><tr><td>

Course Items

</td><td>

Core Java

</td></tr><tr><td>

Active

</td><td>

Selected

</td></tr><tr><td>

Advanced

</td><td>

Cleared

</td></tr><tr><td>

Condition

</td><td>

-   Assigned to changes
-   Configuration item is empty

</td></tr><tr><td>

Autofill fields

</td><td>

-   State Resolved
-   Performance rating N/A

</td></tr></tbody>
</table>|Field|Value|
|-----|-----|
|Number|CR0000106|
|Title|Increase customer satisfaction by solving issues faster|
|Active|Selected|
|Category|Customer Experience|
|Content|Watch this video to increase customer satisfaction by solving issues faster.|

**Parent Topic:**[Configuring Coaching](../concept/cf-configuring-coaching.md)

**Related topics**  


[Coaching field descriptions](../reference/cf-coaching-field-descriptions.md)

