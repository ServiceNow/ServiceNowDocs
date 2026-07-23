---
title: Complete a store audit
description: As an Auditor, open your assigned Store Audit Case in CSM/FSM Workspace, visit the physical store, record observations in work notes and comments, close each Audit Task using Close Complete, then close the Store Audit Case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-store-audit-t-fulfill-audit.html
release: australia
topic_type: task
last_updated: "2026-06-30"
reading_time_minutes: 2
keywords: [fulfill audit, complete store audit, close complete, auditor, work notes]
breadcrumb: [Manage Store Audit, Retail]
---

# Complete a store audit

As an Auditor, open your assigned Store Audit Case in CSM/FSM Workspace, visit the physical store, record observations in work notes and comments, close each Audit Task using **Close Complete**, then close the Store Audit Case.

## Before you begin

-   A Store Audit Case is assigned to you.
-   Role required: `sn_rtl_store_audit.auditor` or `sn_rtl_store_audit.location_auditor`.

## About this task

Auditors access assigned work from the CSM/FSM Workspace. Work notes capture internal observations visible to Auditors and Store Audit Managers; comments are customer-facing and visible to Plan Authors. Cases progress through New → Open → Closed. Close each Audit Task before closing the parent Store Audit Case.

**Note:** HQ Auditors \(`sn_rtl_store_audit.auditor`\) fulfil exclusively via CSM/FSM Workspace. Location Auditors \(`sn_rtl_store_audit.location_auditor`\) can also fulfil via Retail Mobile.

## Procedure

1.  Open and accept the Store Audit Case
2.  Log in to CSM/FSM Workspace and navigate to the Store Audit Cases list.

    The list shows only cases assigned to you.

3.  Open the Store Audit Case for the store you are visiting.

4.  If the case is in **New** state, set **State** to **Open** and click **Save**.

    The case state transitions to Open.

5.  Record observations and close Audit Tasks
6.  Add your case-level observations in the **Work notes** field and click **Save**.

7.  Click the **Audit tasks** tab to view the tasks associated with this case, then open the first Audit Task.

8.  Add task-level observations in the **Work notes** field.

9.  If a questionnaire is present, click the **Questionnaire** tab and complete all mandatory questionnaires.

    The **Close Complete** button is hidden while any mandatory questionnaire is incomplete. Non-mandatory questionnaires do not block closure.

10. Click **Close Complete** in the action bar.

    The button is visible only when the task is in an active state \(Draft, Pending Dispatch, Scheduled, Assigned, Accepted, or Work In Progress\), the **Assigned to** field is not empty, and the task is linked to a Store Audit Case.

    A confirmation popup appears.

11. Click **Proceed** in the confirmation popup.

    The Audit Task transitions to Closed Complete and the **Close Complete** button is hidden.

12. Repeat steps 5–8 for each remaining Audit Task on the case.

13. Close the Store Audit Case
14. Return to the Store Audit Case record, set **State** to **Closed**, and click **Save**.

    The Store Audit Case transitions to Closed. The **Save** button is hidden on Closed cases.


## Result

All Audit Tasks are Closed Complete, observations are recorded in the activity stream, and the Store Audit Case is Closed. The Store Audit Manager has full visibility into all recorded findings.

**Parent Topic:**[Manage Store Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-manage.md)

**Related topics**  


[Retail Store Audit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-overview.md)

[Override audit assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-t-override-assignment.md)

