---
title: Add a Safe Workplace audience for Emergency Outreach
description: Add a collection of users for Emergency Outreach notifications. Target specific users based on criteria such as location, department, or group.
locale: en-US
release: australia
product: Emergency Outreach
classification: emergency-outreach
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Emergency Outreach notifications, Emergency Outreach, Emergency Response Management, Employee Service Management]
---

# Add a Safe Workplace audience for Emergency Outreach

Add a collection of users for Emergency Outreach notifications. Target specific users based on criteria such as location, department, or group.

## Before you begin

The Safe Workplace audience feature is available if you have purchased Employee Readiness Core.

Role required: sn\_imt\_checkin.checkin\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Emergency Outreach** &gt; **Safe Workplace Audience** and click **New**.

2.  In the **Name** field, enter a descriptive name for the audience.

    For example, `Building C Network Group` or `Facilities employees reporting to Bob`.

3.  Indicate the users who should receive notifications.

<table id="choicetable_dwh_wnh_j4b"><thead><tr><th align="left" id="d75009e104">

Method

</th><th align="left" id="d75009e107">

Action

</th></tr></thead><tbody><tr><td id="d75009e113">

**Add users manually**

</td><td>

Select the users that you want to add to the audience in the **Users** field.

</td></tr><tr><td id="d75009e128">

**Upload a spreadsheet of users**

</td><td>

Select the link to add a file in the **Upload file** field.

 The header of the first column of the spreadsheet must be `user_name` if you upload a list of user IDs or `email` if you upload a list of email addresses.

 **Note:** If you have more than 500 entries, split the spreadsheet into multiple files.

</td></tr><tr><td id="d75009e155">

**Use additional criteria based on common User \[sys\_user\] table fields**

</td><td>

1.  Select values for the **Groups**, **Roles**, **Companies**, **Locations**, or **Departments** fields.
2.  Select a value in the **Audience criteria** field.
    -   Include all of the users listed in the Users field and any additional users who fulfill at least one of the other criteria by selecting **Any of the criteria \(OR\)**.
    -   Include only users who fulfill all selected criteria by selecting **All the criteria \(AND\)**. Any users listed in the **Users** field are included in the audience only if they also fulfill all the additional criteria.


</td></tr><tr><td id="d75009e208">

**Enter conditions in the condition builder**

</td><td>

1.  Either retain the default setting of the User \[sys\_user\] table or select a different table and select a column in that table to view its fields.

The condition builder lists fields based on your selection. Scroll to the bottom of the list and select **Show related fields** to view fields from related tables.

The number of users that the audience will contain is shown below the **Audience criteria** field. As you add criteria, check this number to ensure that users are added and filtered as you intend.

2.  Create the condition.

For example, you could specify one floor of a particular building or users who report to a particular manager.

</td></tr></tbody>
</table>4.  Select **Submit**.


