---
title: Create and define filter groups in Security Operations
description: Create and use filter groups to locate records from any table on your instance. For example, you can create a group of all computers by the same manufacturer. You can also filter configuration items \(CIs\) that have similar vulnerabilities or that fall within a particular subnet IP address range.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Security Operations common functionality, Security Operations]
---

# Create and define filter groups in Security Operations

Create and use filter groups to locate records from any table on your instance. For example, you can create a group of all computers by the same manufacturer. You can also filter configuration items \(CIs\) that have similar vulnerabilities or that fall within a particular subnet IP address range.

## Before you begin

Role required: sn\_sec\_cmn.write

## About this task

Filter groups can contain dynamically updated records, a series of static records that are not filtered using conditions, or a combination of dynamically updated and static records. Some filter groups are included in the base system, for example, CI exclusions.

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Groups** &gt; **Filter Groups**.

2.  Click **New**.

3.  Fill in the fields on the form, as appropriate.

<table id="table_vks_thr_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the filter group.

</td></tr><tr><td>

Active

</td><td>

Box to activate the group.

</td></tr><tr><td>

Description

</td><td>

Description for the filter group.

</td></tr><tr><td>

Network IP Address

</td><td>

The network IP address that contains the IP addresses of the CIs you want to add to the group. This field appears only if you selected Configuration Item \[cmdb\_ci\] or a table that extends configuration item in the **Table** field.

</td></tr><tr><td>

Subnet Mask

</td><td>

The subnet that contains the IP addresses of the CIs you want to add to the group,for example, 255.255.255.0. This field appears only if you selected Configuration Item \[cmdb\_ci\] or a table that extends configuration item in the **Table** field.

</td></tr><tr><td>

Table

</td><td>

The table to be filtered on.

</td></tr><tr><td>

Condition

</td><td>

Use the [condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) to define the criteria to be filtered.

</td></tr></tbody>
</table>4.  Right-click the form header and select **Save**.

    An **Advanced Conditions** tab appears.

    More tabs appear depending on the type of table you specified in the **Table** field, as follows:

    |Table|Tabs Displayed|
    |-----|--------------|
    |Configuration Item \[cmdb\_ci\] or a table that extends the configuration item table|**Manually Added CIs** and **Matching CIs**|
    |Task \[task\] or a table that extends the task table|**Manually Added Tasks** and **Matching Tasks**|
    |A table not related to a CI or task|**Manually Added Record**|

5.  To define more conditions for your filter group:

    1.  Click **Advanced Conditions**.

    2.  Insert a new row into the **Additional Filter Group Conditions** embedded list to select other prebuilt filter groups that you want to combine with the filter group being updated.

        If you want the selected filter group to filter records based on a reference field, a mapped field is automatically selected when the current record is saved.

        **Note:** The **Mapped field** value cannot be edited from the **Additional Filter Group Conditions** embedded list. To change the field, click the information icon ![Information](../../vulnerability-response/image/i-icon.png) to open the record.

    3.  Click **Update**.

6.  To manually add more CIs or tasks to the filter group:

    1.  Click the **Manually Added CIs** or **Manually Added Tasks** tab.

    2.  Click **Edit**.

    3.  Select the CIs or tasks you want to add.

    4.  Click **Save**.

7.  To view the CIs or tasks that match your selection criteria:

    1.  Click the **Matching CIs** or **Matching Tasks** tab.

    2.  If you changed the criteria, refresh the list by right-clicking in the form header and selecting **Refresh List**.


**Parent Topic:**[Security Operations common functionality](../concept/sec-ops-common-functionality.md)

