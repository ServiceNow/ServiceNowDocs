---
title: Add a contractor from the Health and Safety Workspace
description: Onboard a contractor to a company listed in the Health and Safety Workspace workspace.
locale: en-US
release: australia
product: Health and Safety Contractor Management
classification: health-and-safety-contractor-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage contractors, Health and Safety Contractor Management, Health and Safety, Employee Service Management]
---

# Add a contractor from the Health and Safety Workspace

Onboard a contractor to a company listed in the Health and Safety Workspace workspace.

## About this task

A new contractor can be added to an existing contractor company in the company list that can be viewed in the Health and Safety Workspace.

For more information about adding a contractor company, see [Add a contractor company from Health and Safety Workspace](../../hs-contractor-management/task/hs-add-contractor-company-from-workspace.md)

## Before you begin

Role required: sn\_hs\_crm.contractor\_coordinator

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Add a contractor.

<table id="choicetable_v4f_5dw_bdc"><thead><tr><th align="left" id="d546301e101">

Option

</th><th align="left" id="d546301e104">

Steps

</th></tr></thead><tbody><tr><td id="d546301e110">

**From a contractor company record**

</td><td>

1.  Select the contractor management icon \(![Contractor management icon](../../hs-contractor-management/image/icon-contractor-mgmt.png)\) to open the **Contractor Management** tab.
2.  In the **Lists** tab, select **Contractor companies** and then select **Active**.
3.  Open the company that you want the contractor added to.
4.  In the **Workers** tab, select **Add**.

**Note:** A list of all users with the \[snc\_external\] role is displayed. Selecting a user from this list creates a Health and Safety profile for them and add them to the contractor company.

5.  Select the check box for one or more contractors to add to the contractor company and select **Add**.


</td></tr><tr><td id="d546301e169">

**From Health and Safety user profile list**

</td><td>

1.  Select the configuration icon \(![Configuration icon](../../hs-risk-management/image/icon-config.png)\).
2.  In the **Lists** tab, select **Health and safety profiles** and then **Active** and then select **New**.
3.  On the form, fill in the fields and select **Save** to add the contractor in the workers list.

**Note:**

    -   The **Type** field must be set to contractor. Only the users with \[snc\_external\] role appear in the **User** list. When the form is saved, the role \[sn\_hs\_csc.contractor\] is assigned to the contractor. This role is needed to access the Contractor Service Center.
    -   Select the company in the **Company** field for the contractor to appear in the company's worker tab.

**Note:** If the company isn’t selected, the Health and Safety profile for the contractor is still created with the correct roles to access to the Contractor Service Center, but the contractor doesn’t appear under any contractor company.

</td></tr></tbody>
</table>
## Result

-   The contractor is added to the workers tab of the contractor company with the correct roles.
-   An email is sent to the contractor with the log in user name and password and a link to access the Contractor Service Center.

## What to do next

You can assign a task to the contractor or upload any documents obtained from the contractor to complete the onboarding for the contractor.

-   For more information to assign a task to a contractor, see [Assign a task to a contractor worker](../../hs-contractor-management/task/hs-assign-tasks-contractor-worker.md).
-   For more information to add a document for a contractor, see [Add a document to a contractor worker](../../hs-contractor-management/task/hs-add-document-contractor-worker.md).
-   To configure the Health and Safety profile for a contractor, see [Assign Health and Safety profile to a contractor worker](../../hs-contractor-management/task/hs-assign-hs-user-profile-contract-worker.md).

