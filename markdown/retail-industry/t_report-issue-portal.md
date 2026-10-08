---
title: Create work item for store on the Retail Portal
description: Create a case on the Retail Service Portal to quickly report an in-store issue, then add tasks to break down the work.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/t\_report-issue-portal.html
release: brazil
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 1
keywords: [create work item for store, create case, portal, store manager, record producer]
breadcrumb: [Quick case and task creation for in-store issues, Retail]
---

# Create work item for store on the Retail Portal

Create a case on the Retail Service Portal to quickly report an in-store issue, then add tasks to break down the work.

## Before you begin

Role required: `sn_rtl_instore_ops.associate`, `sn_rtl_instore_ops.manager`, or `sn_rtl_instore_ops.manager_contributor`. You must also be mapped to at least one store.

## About this task

If you're a store associate or store manager, the store is set from your own store mapping and doesn't appear on the form. If you're an area or region manager, you select the store.

## Procedure

1.  From the Retail Portal, select the **Create work item for store** catalog item.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Select store**|Required for area and region managers: the store that the issue is for. The list shows only the stores that you're mapped to. Store associates and store managers don't see this field.|
    |**Short Description**|A brief, one-line summary of the issue \(for example, "Broken freezer in aisle 3"\).|
    |**Priority**|Required. The urgency level of the issue. The default is 4 - Low.|
    |**Description**|Optional. A detailed explanation of the issue, including any context or location information.|
    |**Attachment**|Optional. Attach a photo or document to support the issue report.|
    |**Assign to**|Optional. The person to assign the case to. If you assign someone, the case opens in the Open state instead of New.|
    |**Due date**|Optional. When the issue should be resolved. You can't select a date earlier than today.|

3.  Select **Submit**.

    The case details page opens, with no confirmation message. The case is in the New state and unassigned, unless you filled in **Assign to**. Everyone mapped to the store can see the case.

4.  Optional: From the case details page, from the overflow menu, select **Add task** to break the work down.

    You can add multiple tasks to a single case. Each task represents a specific action item that one team member will complete. See [Add a task to a case on the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/t_add-task-portal.md).


**Parent Topic:**[Quick case and task creation for in-store issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/c_adhoc-case-task-creation.md)

