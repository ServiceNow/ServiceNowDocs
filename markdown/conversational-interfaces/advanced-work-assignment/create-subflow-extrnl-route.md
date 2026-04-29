---
title: Create a subflow
description: Create a subflow for the Workflow Studio for enabling external routing.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Create a subflow

Create a subflow for the Workflow Studio for enabling external routing.

## Before you begin

Role required: admin

## Procedure

1.  On your ServiceNow instance, navigate to **All** &gt; **Flow Designer** &gt; **Subflows**.

2.  From the Actions list, select **Template - AWA Send Event**.

3.  Select **Copy subflow** from the More Actions menu ![More actions menu.](../../../product/service-catalog-management/image/more-actions-ne-icon.png), copy the contents of the **Template - AWA Send Event** subflow and provide a name to it.

4.  Configure the action that you created in [Create a custom flow action](create-custom-action.md).

    1.  Select the Add an Action, Flow Logic, or Subflow.

    2.  Select the action that you created and in the Actions form, fill in the fields.

<table id="table_wtz_nrx_dcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action

</td><td>

The custom action that you created.For more information, see [Create a custom flow action](create-custom-action.md).

</td></tr><tr><td>

Payload

</td><td>

Input the variables for the action.

</td></tr><tr><td>

Connection Alias \[Connection &amp; Credential Aliases

</td><td>

The HTTP\(s\) Connection that you created.For more information, see [Create a connection Alias for third-party provider](create-cnctn-alias.md).

</td></tr><tr><td>

Resource Path

</td><td>

The endpoint URL of the third-party CAAS provider.

</td></tr></tbody>
</table>    3.  Select **Done**.

5.  Select **Publish**.


