---
title: Configure PaCE Restricted Caller Access Privileges \(RCA\)
description: Define cross-scope access to an application, application resource \(such as an access control role, a business rule, a UI action, or a script include\), or event. You can use a requested RCA to grant store apps access to protected resources in the ServiceNow AI Platform.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure PaCE Restricted Caller Access Privileges \(RCA\)

Define cross-scope access to an application, application resource \(such as an access control role, a business rule, a UI action, or a script include\), or event. You can use a requested RCA to grant store apps access to protected resources in the ServiceNow AI Platform.

## Before you begin

**Note:** This may have configuration implications across all ServiceNow applications in your instance. Verify the RCA settings of other applications after completing this procedure.

Role required: admin

## Procedure

1.  In the PaCE workspace, navigate to **All** &gt; **Policies** &gt; **My Policies**.

2.  Select **New**.

3.  Select **New blank policy**.

4.  Enter a Policy name, then select **Save**.

5.  Navigate to **System Application** &gt; **Application Restricted Caller Access Privileges**

6.  In Application column filter, enter `=Policy as Code Engine`.

7.  In the Source Scope column filter, enter `=Service Applicant Program Management`, and run the filter.

8.  Open each record and change the value of Status field to **Allowed**.


