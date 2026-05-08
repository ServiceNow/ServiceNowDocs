---
title: Approve application restricted caller access privileges
description: Approve restricted caller access \(RCA\) privileges in the target scope so that you can provide scope access privileges. Approving the RCA privileges enables the script includes in Universal Request scope to be accessed from the Universal Request integration with Microsoft Teams scope.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install Universal Request integration, Plan your installation, Integrating ServiceNow with Microsoft Teams and Microsoft 365, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Approve application restricted caller access privileges

Approve restricted caller access \(RCA\) privileges in the target scope so that you can provide scope access privileges. Approving the RCA privileges enables the script includes in Universal Request scope to be accessed from the Universal Request integration with Microsoft Teams scope.

## Before you begin

Role required: admin

## About this task

RCA privileges define cross-scope access to an application, an event, or an application resource. Application resources include access control roles, business rules, UI actions, and script includes. RCA privileges can also be used to allow or deny requests for access. Restricted caller access \[sys\_restricted\_caller\_access\] records track cross-scope applications or scripts that request access to an application, application resource, or event. For more information, see Requested restricted caller access \(RCA\).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Application Restricted Caller Access** &gt; **Restricted Caller Access Privileges**.

2.  In the **Source Scope** search, enter `Universal Request integration with Microsoft Teams`.

3.  Right-click on **Source Scope** column header, and select **Group By Source Scope**.

4.  Expand the **Universal Request integration with Microsoft Teams** source scope.

5.  Open the record.

6.  Change the **Status** to **Allowed**.

7.  Click **Update**.


## Result

The RCA is approved. The records get updated as shown in the following figure. The **Application** column and the **Target Scope** column now have the same values, and the **Status** column changes to **Allowed**.![Universal Request integration with MS Teams RCA approval.](../images/ur-mst-rca-result.png)

**Parent Topic:**[Install Universal Request integration with Microsoft Teams application](install-ur-ms-teams-app.md)

