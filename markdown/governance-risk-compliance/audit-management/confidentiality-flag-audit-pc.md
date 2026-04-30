---
title: Confidentiality flag for audit and compliance records
description: You can set the confidentiality flag at the record level for an issue, engagement, observation, control test, activity, interview, and walkthrough records. The users whom you determine to view and update these records are allowed users.
locale: en-US
release: zurich
product: Audit Management
classification: audit-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Audit Management, Governance, Risk, and Compliance]
---

# Confidentiality flag for audit and compliance records

You can set the confidentiality flag at the record level for an issue, engagement, observation, control test, activity, interview, and walkthrough records. The users whom you determine to view and update these records are allowed users.

When the **Confidential** option is selected, a list of users who can be an engagement lead, auditors, and approvers are auto-populated as **Allowed users**.

As a system admin, you can add more audit users or GRC business users to the list or remove some of the existing users based on your access control criteria and can set them as allowed users.

Also, you can also add random users to the record, who are not audit users or GRC business users. However, an email notification is sent to all allowed users who have neither an audit user nor a GRC business user role intimating them to acquire the confidential role \(sn\_grc.confidential\_user\) from the admin if they are to access the record.

You can also select groups as **Allowed groups** who can access the record as well.

You can view all issues, remediation tasks, evidence request tasks, engagements, observations, and all audit tasks marked as confidential records from the application navigator as GRC confidential records. For more information, see Confidential records in common GRC features.

Similarly, if you are working in the Audit and Compliance workspaces, you can monitor the **Confidential records** in a separate tab in the Tasks page. For more information, see My tasks in the workspace.

To enable the Confidentiality property at the system level:

1.  Navigate to **Policy and Compliance** &gt; **Administration** &gt; **GRC Properties**.

    **Note:** The user must have sn\_grc.admin role.

2.  Select **Yes** for **Enable record level confidentiality**.
3.  Click **Save**.

