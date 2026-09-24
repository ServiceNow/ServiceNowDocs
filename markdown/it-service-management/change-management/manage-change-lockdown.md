---
title: Manage a change lockdown
description: Manage a change lockdown by previewing affected change requests, submitting for approval, reverting to draft, or canceling it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/manage-change-lockdown.html
release: brazil
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [change lockdown, lockdown approval, Revert to Draft, Cancel Lockdown, Preview]
breadcrumb: [Change lockdown, Configure, Change Management, IT Service Management]
---

# Manage a change lockdown

Manage a change lockdown by previewing affected change requests, submitting for approval, reverting to draft, or canceling it.

## Before you begin

Create the change lockdown and add at least one schedule entry, because the **Preview** action becomes available only after a schedule entry is saved. For more information, see [Create a change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-change-lockdown.md).

Role required: `change_manager`

## About this task

A lockdown progresses through the **Draft**, **Awaiting Approval**, and **Enforced** states. Only an enforced lockdown places change requests on hold. You can preview affected change requests and cancel the lockdown at any point before it closes. For details about available actions in each state, see [Change lockdown states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-lockdown-states.md).

## Procedure

1.  Open the change lockdown record.

2.  Select **Preview** to review the change requests that the lockdown affects.

    The **Lockdown Change Requests** dialog box displays matching change requests with their number, short description, model, type, state, planned start date, and planned end date. To adjust the preview limit, see [Set the lockdown preview maximum](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/set-lockdown-preview-maximum.md).

3.  Select **Close**.

    If the preview dispalys the change requests that the lockdown should not affect, adjust the **Condition** or **Change Request Condition** field, or edit the schedule entry, then preview again.

4.  Select **Request Approval**.

    The **State** field moves to **Awaiting Approval** and a message confirms that approval has been requested for the lockdown. Reload the record to see the approval record on the **Approvers** tab.

5.  Select **Revert to Draft** to refine the lockdown before it is approved.

    The **State** field returns to **Draft** and the generated approval becomes no longer required. The conditions and the schedule are editable again, so you can adjust the criteria, preview the result, and select **Request Approval** again. Repeat this cycle until the matched change requests are correct.

6.  Ask the approver to approve or reject the lockdown.

    An approval, the change lockdown moves to **Enforced** state and the approval becomes no longer required. The matched change requests are written to the **Schedule Lockdown Changes** related list with the **On hold** column set to `true`.

    A rejection returns the lockdown to the **Draft** state, so that you can shorten the period or narrow the conditions and request approval again.

7.  Select **Cancel Lockdown** and confirm the cancellation.

    |State when you cancel|Result|
    |---------------------|------|
    |**Before approval**|The lockdown ends without placing any change request on hold. Use this option when the critical period is called off while the lockdown is in the **Draft** or **Awaiting Approval** state.|
    |**After approval**|The lockdown releases the change requests that it holds. On the **Schedule Lockdown Changes** tab, the **On hold** column changes from `true` to `false`. A change request that is on hold for another reason stays on hold.|

    **Note:** A cancelled lockdown cannot be reverted or reused. To lock down changes again, create a new lockdown record.


**Parent Topic:**[Change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-lockdown.md)

**Related topics**  


[Change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-lockdown.md)

[Create a change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-change-lockdown.md)

[Change lockdown states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-lockdown-states.md)

