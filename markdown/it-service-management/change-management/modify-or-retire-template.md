---
title: Modify a template
description: Copy and modify change templates.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create and propose a change template, Create a Change model, Configure, Change Management, IT Service Management]
---

# Modify a template

Copy and modify change templates.

## Before you begin

Role required: change\_manager

You must have a role with the following access with regard to the change model to modify or retire a change template:

-   Access to read
-   Access to modify

## About this task

Before modifying a template, you can analyze the template usage by viewing the **Change Template Metrics** tab. View the change template usage trend and related statistical data by selecting **Closed Change count**.

You can modify only templates in the Draft state. To modify templates that are in the Proposed state, or are already published, create a copy. If you want to discontinue the existing template after creating a modified copy, use the **Copy and retire** option.

## Procedure

1.  Navigate to **All** &gt; **Models** &gt; **Change Templates**.

2.  Select the template you want to modify, copy, or retire.

<table id="choicetable_zqg_rlx_5w"><tbody><tr><td id="d87077e104">

**Modify a change template**

</td><td>

Modify the information available in the template.**Note:** You can modify any field and field policy in the change template, and send for approval. After the modifications are approved, a new version of the change template is created. Change requests created from the modified change template reflects the modifications made.

You can modify only templates in the Draft state.

</td></tr><tr><td id="d87077e121">

**Create a copy of a published template for retirement or modification**

</td><td>

Select **Copy**.**Note:** A template copy is created and the Previous template field displays the template from which the copy was created. The copied template is created in the **Draft** state, and all the fields and field policies of the original template are available.

</td></tr></tbody>
</table>3.  Either save the template information for later approval or send it for approval immediately.

    -   To save the modifications but not send them for approval, select **Save**.
    -   To send the template for approval, select **Publish**.
    **Note:** In the **Approvers** tab, you can view the list of approvers who have been configured to review the modifications made to the template, and the details of proposed and reviewed modifications.


**Parent Topic:**[Create and propose a change template](create-change-template.md)

**Related topics**  


[Create and propose a change template](create-change-template.md)

[Review a change template](review-change-template.md)

