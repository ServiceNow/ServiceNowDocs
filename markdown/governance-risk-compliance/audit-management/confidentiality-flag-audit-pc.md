---
title: Confidentiality flag for audit and compliance records
description: You can set the confidentiality flag at the record level for an issue, engagement, observation, control test, activity, interview, and walkthrough records. The users whom you determine to view and update these records are allowed users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/audit-management/confidentiality-flag-audit-pc.html
release: australia
product: Audit Management
classification: audit-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Audit Management overview, Audit Management, Governance, Risk, and Compliance]
---

# Confidentiality flag for audit and compliance records

You can set the confidentiality flag at the record level for an issue, engagement, observation, control test, activity, interview, and walkthrough records. The users whom you determine to view and update these records are allowed users.

When the **Confidential** option is selected, a list of users who can be an engagement lead, auditors, and approvers are auto-populated as **Allowed users**.

As a system admin, you can add more audit users or GRC business users to the list. You can also remove existing users based on your access control criteria.

You can also add users to the record who are not audit users or GRC business users. An email notification is sent to these allowed users. The notification informs them to acquire the confidential role \(sn\_grc.confidential\_user\) from the admin to access the record.

You can also select groups as **Allowed groups** who can access the record as well.

You can view all issues, remediation tasks, evidence request tasks, engagements, observations, and all audit tasks marked as confidential records from the application navigator as GRC confidential records. For more information, see Confidential records in common GRC features.

Similarly, if you are working in the Audit and Compliance workspaces, you can monitor the **Confidential records** in a separate tab in the Tasks page. For more information, see My tasks in the workspace.

To enable the Confidentiality property at the system level:

1.  Navigate to **Policy and Compliance** &gt; **Administration** &gt; **GRC Properties**.

    **Note:** The user must have sn\_grc.admin role.

2.  Select **Yes** for **Enable record level confidentiality**.
3.  Click **Save**.

