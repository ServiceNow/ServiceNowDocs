---
title: Create an EVAM action definition
description: You can associate a declarative action with a view template. EVAM also enables user interactions to trigger a server script or UXF client action.
locale: en-US
release: xanadu
product: Entity View Action Mapper \(EVAM\)
classification: entity-view-action-mapper-evam
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [View configurations, view templates, and configuration bundles, Entity View Action Mapper, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create an EVAM action definition

You can associate a declarative action with a view template. EVAM also enables user interactions to trigger a server script or UXF client action.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Entity View Action Mapper** &gt; **Action Definition**, and then click **New**.

2.  On the form, fill in the fields.

<table id="table_nsb_spy_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action label

</td><td>

Display label of the EVAM action.

</td></tr><tr><td>

Action name

</td><td>

Database name for the EVAM action name.

</td></tr><tr><td>

Implemented as

</td><td>

Implementation of the EVAM action definition. Select one of the following:-   **Server Script**

Executes a script on the server, for example, to assign a record to someone, or delete a record.

-   **UXF Client Action**

Takes action on the client side, such as opening a record or making a phone call.

</td></tr><tr><td>

Specify client action

</td><td>

You can choose a pre-defined action. For example, SC Content Items KB Article Navigation, to display KB articles.

**Note:** This field appears only if you select to implement the action as a UXF client action.

</td></tr><tr><td>

Application

</td><td>

Application scope of the EVAM action.

</td></tr><tr><td>

Active

</td><td>

Option to activate the EVAM action.

</td></tr><tr><td>

Description

</td><td>

Description of the EVAM action.

</td></tr></tbody>
</table>3.  Click **Submit**.


