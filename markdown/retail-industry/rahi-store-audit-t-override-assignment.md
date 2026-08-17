---
title: Audit assignment from workspace
description: As a Store Audit Manager, manually assign a Store Audit Case or Audit Task to a specific Auditor, or change the assignment group set by the automated assignment rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-store-audit-t-override-assignment.html
release: australia
topic_type: task
last_updated: "2026-07-07"
reading_time_minutes: 1
keywords: [override assignment, reassign audit, audit manager, assigned to]
breadcrumb: [Manage Store Audit, Retail]
---

# Audit assignment from workspace

As a Store Audit Manager, manually assign a Store Audit Case or Audit Task to a specific Auditor, or change the assignment group set by the automated assignment rules.

## Before you begin

-   The Store Audit Case or Audit Task to be reassigned exists and is not Closed.
-   Role required: `sn_rtl_store_audit.audit_manager` or `sn_rtl_store_audit.location_audit_manager`.

## About this task

Assignment rules automatically set the assignment group on Store Audit Cases and Audit Tasks when they're generated—they don't assign an individual Auditor. Use this procedure to assign a specific Auditor, correct a routing error, or redistribute workload. Store Audit Managers can view all cases and tasks regardless of assignment.

## Procedure

1.  Log in to CSM/FSM Workspace with your Store Audit Manager credentials and open the Store Audit Case or Audit Task you want to reassign.

    Store Audit Cases are in the Store Audit Cases list; Audit Tasks are on the **Audit tasks** tab of the parent case. Both are also visible from the **Retail cases** list.

2.  Update the **Assigned to** field to the new Auditor.

3.  If needed, update the **Assignment group** field.

4.  Click **Save**.

    The newly assigned Auditor receives a push notification if Retail Mobile is active.


## Result

The Store Audit Case or Audit Task is reassigned to the selected Auditor and the assignment change is logged in the activity stream.

**Parent Topic:**[Manage Store Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-manage.md)

**Related topics**  


[Retail Store Audit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-overview.md)

[Create and publish an audit plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-t-create-and-generate.md)

