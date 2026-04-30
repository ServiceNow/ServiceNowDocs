---
title: Create an audience
description: Create or modify an audience record to define the conditions or criteria that users must meet to view content.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Audiences, Reusable components, Setup employee communications, Configure, Employee Center, Employee Service Management]
---

# Create an audience

Create or modify an audience record to define the conditions or criteria that users must meet to view content.

## Before you begin

Role required: sn\_cd.content\_admin

Each audience record is configured based on user conditions, user criteria, HR profile conditions, HR criteria, or an uploaded file. You can apply them to portal content or lifecycle event activities. For example, a lifecycle event activity for a work visa transfer is targeted only to employees that need a visa transfer.

## Procedure

1.  Navigate to **All** &gt; **Content Publishing** &gt; **Re-usable Components** &gt; **Audiences**.

2.  Click **New** or open a record.

3.  Fill in the fields on the form.

<table id="table_ykv_ngg_wfb"><thead><tr><th>

Field

</th><th colspan="2">

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td colspan="2">

Name of the audience record.

</td></tr><tr><td rowspan="6">

Audience type

</td><td colspan="2">

The audience the content is directed to. Use one of the following selections to define an audience.

</td></tr><tr><td>

Users \[sys\_user\]

</td><td>

Use conditions defined by the User \[sys\_user\] table with custom conditions you choose.Use the **OR** button to define multiple conditions. Any of the conditions you define can be met when using **OR**.

Use the **AND** button to evaluate all conditions you define. All conditions must be met when using **AND**.

Select the **New Criteria** button to add conditions.

</td></tr><tr><td>

User Criteria \[user\_criteria\]

</td><td>

Criteria based on role, department, group, location, or company. User criteria is a platform feature. See [User criteria for Service Portal](https://www.servicenow.com/docs/access?context=user-criteria&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

HR Profiles \[sn\_hr\_core\_profile\]

</td><td>

\(HR Service Delivery only\) Use conditions based the HR profile \[sn\_hr\_core\_profile\] table with conditions you choose.

</td></tr><tr><td>

HR Criteria \[sn\_hr\_core\_criteria\]

</td><td>

\(HR Service Delivery only\) Use pre-defined HR criteria. HR criteria is based on conditions defined by the HR Profile \[sn\_hr\_core\_profile\] or User \[sys\_user\] tables. The base system provides examples that can be used.**Note:** For more information, see [HR criteria](../../human-resources/concept/hr-criteria.md#) and [Configure an HR criteria record](../../human-resources/concept/hr-criteria.md#).

</td></tr><tr><td>

Upload File

</td><td>

Browse and choose a file with populated with user names or email addresses. -   user\_name template: Indicates that you are uploading a file with user names.
-   email template: Indicates that you are uploading a file with email addresses.

**Note:** The header of the first column must contain user\_name or email.

</td></tr></tbody>
</table>    **Note:** After audience type and conditions are selected, a blue link appears with the number of users that meet the criteria. Click this link to view all users by audience type.

    Select the **View users** link to view the users that meet your conditions.

4.  Click **Save**, **Submit**, or **Update**.


## What to do next

If you click **Save** and the **Allow Ownership for Audiences** property is set to **Yes**, the **Restrict audience by user** and **Restrict audience by group** related lists appear.

**Note:** For more information on restricting an audience by user or group, see [Content Ownership](../concept/ecpro-content-restriction.md) and [Assign ownership of an audience](ecpro-ca-cd-audience-delegation.md).

