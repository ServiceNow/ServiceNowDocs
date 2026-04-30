---
title: Specify a user segment group for a bulk case request in Agent Workspace for HR Case Management
description: Create a user segment group to specify in a bulk case request the users for whom a case will be created. You can specify values for a group of users or specify multiple segments with different values for different groups of users.
locale: en-US
release: xanadu
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a bulk case request using Agent Workspace for HR Case Management, Using Agent Workspace for HR Case Management, Agent Workspace for HR Case Management \(Configurable\), HR Service Delivery, Employee Service Management]
---

# Specify a user segment group for a bulk case request in Agent Workspace for HR Case Management

Create a user segment group to specify in a bulk case request the users for whom a case will be created. You can specify values for a group of users or specify multiple segments with different values for different groups of users.

## Before you begin

Role required: sn\_hr\_core\_admin

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **Agent Workspace for HR Case Management**.

2.  Select the **Lists** icon \(![HR Workspace Lists icon](../image/agent-ws-hr-list-icon.png)\).

3.  Select **Bulk case requests**.

4.  Select the bulk case request.

5.  Select **Create segment group**.

6.  On the form, fill in the fields.

<table id="table_b5f_bhz_bbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Label that describes the user segment group.

</td></tr><tr><td>

Opened for

</td><td>

Employee to be assigned as the Opened for person on each case.For example, for an onboarding bulk case request, you would select the hiring manager.

</td></tr><tr><td>

Work notes

</td><td>

Further details about the user segment.

</td></tr></tbody>
</table>7.  Select **Next**.

8.  Indicate how you will indicate which users the bulk case request will create cases for in the **Filter by** field.

<table id="choicetable_nwr_13z_bbc"><thead><tr><th align="left" id="d384732e198">

Data source

</th><th align="left" id="d384732e204">

Description

</th></tr></thead><tbody><tr><td id="d384732e210">

**File**

</td><td>

Upload a file with user names or email addresses.1.  Select the file type in the **Template file type** or, for a pre-formatted Excel spreadsheet, select **Download template**.
    -   **User name template** - A file containing user names.
    -   **Email template** - A file containing email addresses.
2.  Find and select the file you’re uploading by selecting **+Add File**.
3.  Select **Upload**.
4.  Select **Process file**.


</td></tr><tr><td id="d384732e265">

**HR criteria**

</td><td>

Criteria based on conditions defined by the HR Profile \[sn\_hr\_core\_profile\] or User \[sys\_user\] tables.

</td></tr><tr><td id="d384732e274">

**User criteria**

</td><td>

Criteria based on role, department, group, location, or company.

</td></tr><tr><td id="d384732e283">

**HR profile**

</td><td>

Condition based on the HR profile \[sn\_hr\_core\_profile\] table.

</td></tr><tr><td id="d384732e293">

**Users**

</td><td>

Conditions based on the User \[sys\_user\] table.

</td></tr></tbody>
</table>9.  Select **Create segment group**.

    The **Bulk Case Request** form is displayed with the user segment group you created.

    **Note:** You can still review and edit your user segment group. For more information, see [Review users in a user segment group](manage-group-aws.md).


