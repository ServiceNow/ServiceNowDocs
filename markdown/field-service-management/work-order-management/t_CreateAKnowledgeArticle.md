---
title: Create a knowledge article for a work order template
description: You can add knowledge articles and guides \(such as installation guides, maintenance procedures, and checklists\) to the default knowledge base for hardware, software, and consumable templates.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Templates, Work orders, Set up work orders and tasks, Configure, Field Service Management]
---

# Create a knowledge article for a work order template

You can add knowledge articles and guides \(such as installation guides, maintenance procedures, and checklists\) to the default knowledge base for hardware, software, and consumable templates.

## Before you begin

Role required: wm\_admin or model\_manager

## Procedure

1.  Navigate to one of the following:

    -   **Product Catalog** &gt; **Templates** &gt; **Work Order Templates**
    -   **Field Service** &gt; **Catalog &amp; Knowledge** &gt; **Work Order Templates**
2.  Click **New**.

3.  Fill in the fields on the Work Order Template form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Request information|
    |Name|\[Required\] Unique and descriptive name for this template.|
    |Short description|\[Required\] Content that is copied into the **Short description** field of a work order when this work order template is used. The exception to this is a work order created from an incident, problem, or change request, which always uses the short description of the source task, even when a template is applied.|
    |Description|More in-depth description of the purpose of the template.|
    |Checklist template|Select a checklist template to add a checklist to the work orders created from this work order template. For information on checklists, see [Checklists](https://www.servicenow.com/docs/access?context=c_Checklists&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).|
    |Workflow|The workflow for work orders created from this template.|
    |Qualification group|The qualification group for work orders created from this template.|

    Any hardware, software, and consumable assets you create and assign to the new template are displayed in the **Knowledge** related list on the template record.


