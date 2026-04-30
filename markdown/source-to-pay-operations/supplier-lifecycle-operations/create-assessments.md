---
title: Create assessments from assessment templates
description: After mapping the assessment templates with segmentation rules, supplier managers manually trigger batch creation of assessments.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure smart assessments, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Create assessments from assessment templates

After mapping the assessment templates with segmentation rules, supplier managers manually trigger batch creation of assessments.

## Before you begin

Role required: sn\_slm.manager or sn\_slm.admin

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Open the segmentation rule for which assessment templates have been created.

3.  In the **Assessment templates** tab, select the assessment template mapping record for which assessments have to be triggered.

4.  Select **Create assessments** to trigger assessments to the users.

    ![Create assessments](../image/slo-create-assmnt.png)


## Result

The assessment is created and runs in the background. The status of the assessment changes as it progresses.

|State|When it occurs|
|-----|--------------|
|**New**|When the Assessment Template Relationship record is created.|
|**In Progress**|When **Create Assessment** is clicked, all UI validations are completed, the selected record is validated as eligible, and the assessment instance creation process begins.|
|**Complete**|When the assessment creation process is successfully completed for all valid assignees.|
|**Cancelled**|When cancelled using the **Cancel** related list action. The Assessment Template Relationship record and all related assessment instances move to the Cancelled state.|
|**Error**|When an error occurs during assessment creation, or when assessment instance creation fails for one or more assignees. The Assessment Template Relationship record moves to the Error state.|

**Parent Topic:**[Configure smart assessments](configure-smart-assessments.md)

