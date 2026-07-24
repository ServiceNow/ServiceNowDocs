---
title: Override audit assignment
description: As a Store Audit Manager, manually reassign a Store Audit Case or Audit Task to a different Auditor when the automated assignment rules have routed a record incorrectly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-store-audit-t-override-assignment.html
release: australia
topic_type: task
last_updated: "2026-06-29"
reading_time_minutes: 1
keywords: [override assignment, reassign audit, audit manager, assigned to]
breadcrumb: [Manage Store Audit, Retail]
---

# Override audit assignment

As a Store Audit Manager, manually reassign a Store Audit Case or Audit Task to a different Auditor when the automated assignment rules have routed a record incorrectly.

## Before you begin

-   The Store Audit Case or Audit Task to be reassigned exists and is not Closed.
-   Role required: `sn_rtl_store_audit.audit_manager` or `sn_rtl_store_audit.location_audit_manager`.

## About this task

Store Audit Cases and Audit Tasks are automatically assigned to Auditors via platform-native assignment rules when generated. Use this procedure when you need to correct routing errors, cover for an unavailable Auditor, or redistribute workload. Store Audit Managers can view all cases and tasks regardless of assignment.

## Procedure

1.  To override a Store Audit Case assignment:
2.  Log in to CSM/FSM Workspace with your Store Audit Manager credentials and navigate to the Store Audit Cases list.

    All cases across all Auditors are visible to Store Audit Managers.

3.  Open the Store Audit Case you want to reassign.

4.  Update the **Assigned to** field to the new Auditor.

5.  If needed, update the **Assignment group** field.

6.  Click **Save**.

    The case is assigned to the new Auditor. If Retail Mobile push notifications are active, the newly assigned Auditor receives a notification with the case number and a deep link to the case record.

7.  To override an Audit Task assignment:
8.  Open the parent Store Audit Case and click the **Audit tasks** tab.

9.  Open the Audit Task you want to reassign.

10. Update the **Assigned to** field and optionally the **Assignment group** field, then click **Save**.

    The task is reassigned. The newly assigned Auditor receives a push notification if Retail Mobile is active.


## Result

The Store Audit Case or Audit Task is reassigned to the selected Auditor and the assignment change is logged in the activity stream.

**Related topics**  


[Components installed with Store Audit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-reference.md)

