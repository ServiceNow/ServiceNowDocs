---
title: Retire a change template
description: Retire change templates that you no longer need.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create and propose a change template, Create a Change model, Configure, Change Management, IT Service Management]
---

# Retire a change template

Retire change templates that you no longer need.

## Before you begin

Role required: change\_manager

You must have a role with the following access with regard to the change model to modify or retire a change template:

-   Access to read
-   Access to modify

## About this task

Before retiring a template, you can analyze the template usage by viewing the **Change Template Metrics** tab. View the change template usage trend and related statistical data by selecting **Closed Change count**.

## Procedure

1.  Navigate to **All** &gt; **Models** &gt; **Change Templates**.

2.  Select the template you want to retire.

3.  Retire and discontinue the template or retire it and create a copy you can modify.

<table id="choicetable_zqg_rlx_5w"><tbody><tr><td id="d163839e101">

**Retire and discontinue a change template**

</td><td>

Select **Retire**.The retirement request is sent for approval. The template moves to Pending Retirement state, and is no longer be available for modifications.

After approval, the template moves to the **Retired** state, and is unavailable for use. If rejected, the state of the template changes to **Published**.

</td></tr><tr><td id="d163839e123">

**Copy and retire the parent template**

</td><td>

Select **Copy and retire** in the Additional actions menu.A template copy is created and the Previous template field displays the template from which the copy was created. The copied template is created in the **Draft** state, and all the fields and field policies of the original template are available.

After the copied template is published, the original template moves to the **Retired** state and is unavailable for use.

</td></tr></tbody>
</table>4.  Save the template information for later approval or send it for approval immediately.

    -   To save the modifications but not send them for approval, select **Save**.
    -   To send the template for approval, select **Publish**.
5.  View the list of approvers who have been configured to review the modifications made to the template in the **Approvers** tab.


**Parent Topic:**[Create and propose a change template](create-change-template.md)

**Related topics**  


[Review a change template](review-change-template.md)

