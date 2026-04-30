---
title: Create a user segment group
description: User segment groups allow you to specify values for a group of users, or with multiple segments specify different values for different groups of users. Segments allows you to ensure that your bulk case creation is correct before executing.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Creating bulk cases, HR Case Management, Explore and use HR Case and Knowledge Management, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Create a user segment group

User segment groups allow you to specify values for a group of users, or with multiple segments specify different values for different groups of users. Segments allows you to ensure that your bulk case creation is correct before executing.

## Before you begin

Role required: admin

## About this task

After you create a bulk case request, you create a user segment to define the users a case will be created for.

**Note:** You can have multiple user segments associated with a bulk case request.

## Procedure

1.  From the **User segment groups** tab on the **Bulk Case Request** form, select **New**.

2.  On the form, fill in the fields.

    **Note:** The **Label**, **Opened for**, and **Filter by** fields

<table id="table_g4s_b52_hpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

The label that describes the user segment.**Note:** When cases are created, the short description from the HR Case Template appears. The label describes the segment.

</td></tr><tr><td>

Opened for

</td><td>

The employee you choose as the **Opened for** person on each case. For example, you can select the hiring manager for an onboarding bulk case request.

</td></tr><tr><td>

Work notes

</td><td>

Information that provides further details about the user segment.

</td></tr><tr><td>

Additional fields

</td><td>

Depending on the HR service selected when creating a bulk case request, additional fields may appear. For example, if **Tuition Reimbursement Request** was entered in the HR service field on the Bulk Case Request form, the following fields appear:-   School or Program name
-   Course title
-   Course justification
-   Course start date
-   Course end date
-   Course cost
For more information on what fields appear, see [Configure the HR case creation form for an HR service](configure-case-creation-form-for-hr-service.md). The base system only provides additional fields for the Tuition Reimbursement Inquiry and Tuition Reimbursement Request HR services.

</td></tr><tr><td>

Filter by

</td><td>

Determines who to create the bulk HR case for:-   Upload file:
    -   Upload a file with user names or email addresses. Select **Download Template** for a pre-formatted Excel spreadsheet.

**Note:** The header of the first column must contain user\_name or email.

    -   Check the **user\_name template** to indicate you’re uploading a file with user names.
    -   Check email template to Indicate you’re uploading a file with email addresses.
    -   Select **Choose File** to find and select the file you’re uploading.
    -   Select the **Upload** button after you choose a file.
    -   After uploading the file, the number of users appears. This number represents the number of users that fulfill your criteria.
-   HR criteria: Use pre-defined HR criteria. Criteria based on conditions defined by the **HR Profile \[sn\_hr\_core\_profile\]** or **User \[sys\_user\]** tables. The base system provides examples that you can select from the **Select HR Criteria** list.

**Note:** Only available to users with the sn\_hr\_core.content\_reader, sn\_hr\_core.content\_writer, or sn\_hr\_core.admin roles.

-   User criteria: Criteria based on role, department, group, location, or company. User criteria is a platform feature. See [User criteria for Service Portal](https://www.servicenow.com/docs/access?context=user-criteria&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) .

**Note:** Only available to users with the sn\_hr\_core.content\_reader, sn\_hr\_core.content\_writer, or sn\_hr\_core.admin roles.

-   HR profiles: Use conditions based on the **HR profile \[sn\_hr\_core\_profile\]** table with conditions that you choose.
-   Users: Use conditions defined by the **User \[sys\_user\]** table with conditions that you choose.
 After selecting a filter, the number of matching users appears in green as a link. Click the link to view all users selected based on the filter.

 For the **HR Profile** and **Users** filter, you can refine the selection. Right-click on a column, select **Filter Out** or **Show Matching**.

**Note:** When defining conditions like case sensitivity or null values, see API[GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

</td></tr></tbody>
</table>3.  Select **Save**.

    The **Bulk Case Request** form returns with the user segment group you created. If your user group segment has many cases, the status for the segment is **Processing**.

    **Note:** You can still review and edit your user segment group. For more information, see [Manage a user group segment](bulk-case-segment-manage.md).

4.  When the status is **Processed**, the **Create cases** button appears at the top right and above the related list tabs.

5.  Select the **Create cases** button.

    Your request is queued and asynchronously updated in the background.

    **Note:** After selecting the **Create cases** button, all users with a status of **Included** are rechecked against the filter criteria used. Cases aren’t created for users that no longer match the filter criteria. Cases are also not created for users that match the criteria after the user segment was created.

6.  Select the **Cases created** tab to view a list of cases created.


**Parent Topic:**[Creating bulk cases](../concept/bulk-case.md)

