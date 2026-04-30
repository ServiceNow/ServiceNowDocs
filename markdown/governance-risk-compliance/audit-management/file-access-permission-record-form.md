---
title: File access permission record form
description: Update the File access permission record form for a Cloud file.
locale: en-US
release: yokohama
product: Audit Management
classification: audit-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a File access permission record to manage the permissions, Create a Cloud file configuration on engagements and audit tasks, Manage your documents and work papers with Audit Management as cloud files, Using Audit Management, Audit Management, Governance, Risk, and Compliance]
---

# File access permission record form

Update the File access permission record form for a Cloud file.

## File access permission record form

For a description of the field values, see the following table.

<table id="table_h21_nyj_4zb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Name of the table for which the access permissions are configured. For example, Control Test \[sn\_audit\_control\_test\].

</td></tr><tr><td>

Access for

</td><td>

Access for the users or a group. For example, Engagement \[sn\_audit\_engagement\]. For all the files used in this table, the access permissions are configured in this form.

</td></tr><tr><td>

Userfield

</td><td>

Access permissions that can be configured for the users. Displays a tree structure of all the user fields for the selected record. When the permissions are refreshed, they’re automatically refreshed and assigned to the users.**Note:** The field appears if you'd selected Users in the **Access for** field.

</td></tr><tr><td>

Groupfield

</td><td>

Access permissions that can be configured for the users of a group. Displays a tree structure of all the group fields for the selected record. When the permissions are refreshed for the first time, every group member in the group who wants to have access to the document, should select the engagement record and select the **Request access** action manually to access the document.

 The users of a group do not automatically receive an access to the record for the first time. They must request an access for the first time.

 For the subsequent operations on the record, access for the users \(who requested it for the first time\) is also refreshed.

 **Note:** The field appears if you'd selected Group in the **Access for** field.

</td></tr><tr><td>

Access permission

</td><td>

Type of access permission to be configured for the selected user. For example, Read or Write.

</td></tr><tr><td>

Access condition

</td><td>

Condition that describes when the file access permissions are applied.

</td></tr></tbody>
</table>