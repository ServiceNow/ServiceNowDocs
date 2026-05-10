---
title: Create COE security
description: Place security on a COE to prevent a group from accessing another group's cases.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [HR service categorization, HR Centers of Excellence data model, HR services, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Create COE security

Place security on a COE to prevent a group from accessing another group's cases.

## Before you begin

Role required: sn\_hr\_core.admin, sn\_hr\_le.admin

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **COE Security Configuration**.

2.  Select the COE \(table that extends the HR case table\) you want specified groups to have access to.

3.  Check **Applies to all services** if you want all the HR services under the selected COE to be included in the security policy.

4.  Leave this field blank to select specific HR services under a COE.

5.  If you leave this field blank, the **Services** field appears and you can select specific HR services.

6.  Ensure that the **Application** field displays the scope correctly.

    For more information, see [System settings for the user interface \(UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/r_UI16BannerFrame.md).

7.  Check **Active** to enable security on the COE.

8.  From the **Type** field, select how the policy you are defining controls security for the COE.

    Your choices are:

    -   Read
    -   Write
    -   Case Restriction
    **Note:** The Case restriction option is only displayed when Employee Relations is installed.

    Selecting Case Locking displays the following fields:

    -   Able to lock cases: Users that belong to the associated group can lock cases under the COE.
    -   Able to view locked cases: Users that belong to the associated group can view locked cases.
9.  Select the filter condition \(if configured\) the security policy must pass for the COE to be in effect.

    **Warning:** Selecting the filter condition might impact the security policy and affect all cases under a COE, including the non-active cases. Be sure you understand the full impact of the condition.

10. Select **Save** to remain on the security policy you are working on or **Submit** to return to the list of COE Security Policies.

    If you select **Save**, the Groups related list appears.

11. Select **Edit** to associate groups to the COE security policy.

    For more information on Groups, see [Manage HR Groups](../task/t_ManageHRGroups.md).

12. Move the groups you want associated with the COE security policy you are defining from the Collection column to the Groups List column.

13. Select **Save**.

    The COE Security Policy returns.

14. Select **Update**.


**Parent Topic:**[HR service categorization](hr-service-categorization.md)

