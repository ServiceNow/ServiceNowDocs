---
title: Edit a question in Catalog Builder
description: Edit an existing question if you want to improve it by adding UI policies.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating or editing catalog item template, Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Edit a question in Catalog Builder

Edit an existing question if you want to improve it by adding UI policies.

## Before you begin

Role required: catalog\_builder\_editor, catalog\_admin, or admin

## About this task

Set values for the fields and condition-based field messages. Make the question mandatory, visible, or read-only based on your requirements. You can also deactivate the question.

You can’t edit the questions that belong to single-row and multi-row variable sets.

-   If the question is used in a published catalog item, you can’t delete it but you can mark it as inactive. You can include such questions again in the catalog item by using the **Insert De-activated questions** option.
-   Removing a new question that has never been published deletes the question.
-   You can’t remove questions of types that aren't allowed in the template or supported in the Catalog Builder.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Builder**.

2.  Select the **Catalog items** tab.

3.  Select a catalog item and navigate to the **Questions** tab.

4.  Deactivate a question.

    1.  Move to the question and select the deactivate icon \(![Deactivate icon.](../image/deactivate-quest.png)\).

    2.  In the dialog box, select **Deactivate**.

5.  Edit a question.

    1.  Move to the question and select the edit icon \(![Edit icon.](../image/edit-quest-builder.png)\).

    2.  Make the required changes and select **Save**.

    **Note:** If you want to add UI policies to the question, use UI Policy tab to add them.


**Parent Topic:**[Creating or editing catalog item template](create-cat-item-template-cat-builder.md)

**Related topics**  


[Create UI policies in Catalog Builder](create-ui-policies-in-catalog-builder.md)

[UI policy form in Catalog Builder](ui-policy-form-in-catalog-builder.md)

