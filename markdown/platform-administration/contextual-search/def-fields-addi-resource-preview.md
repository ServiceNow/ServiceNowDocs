---
title: Specify fields for the Cxs\_popup view
description: Edit the Cxs\_popup view to specify the fields to be shown for addition resources in the preview window of a task record. The preview helps you with the summary of the record.
locale: en-US
release: yokohama
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing contextual search, Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Specify fields for the Cxs\_popup view

Edit the Cxs\_popup view to specify the fields to be shown for addition resources in the preview window of a task record. The preview helps you with the summary of the record.

## Before you begin

Role required: admin

## About this task

If a Cxs\_popup view isn't defined for the additional resource table, the sys\_popup view is used. If the sys\_popup view is also not defined, the default view is considered.

## Procedure

1.  Navigate to **Incident** &gt; **All**.

2.  Open the incident record whose view you want to change to Cxs\_popup.

3.  Select the additional actions icon \(![Additional actions icon](../image/additional-actions.png)\) and in the **View** option, select **Cxs\_popup**.

    ![Incident form in Cxs_popup view.](../image/cxs-popup-view.png)

    The view of the incident record changes to Cxs\_popup view.

4.  Select the additional actions icon \(![Additional actions icon](../image/additional-actions.png)\), and in the **Configure** option, select **Form Layout**.

5.  From the **Available** list of fields, select the fields that you want to be available in the Cxs\_popup view and move them under **Selected**.

6.  Select **Save**.


**Parent Topic:**[Managing contextual search](../concept/working-with-contextual-search.md)

