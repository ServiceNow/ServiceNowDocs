---
title: Opt in to the employee profile
description: Enable the new employee details and design by opting in to employee profile.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Employee profile, Setup task management, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Opt in to the employee profile

Enable the new employee details and design by opting in to employee profile.

## Before you begin

Role required: sn\_employee.admin

Before opting in, create an active employee definition. For more information, see [Create an active employee definition](generate-profile-definition.md).

**Note:** With Employee Profile \(com.sn\_employee\) plugin, employee profile opt-in is available for EC and EC Pro.

## Procedure

1.  Navigate to **All** &gt; **Employee Profile** &gt; **Setup**.

    The Opt-in to Employee Profile page appears.

2.  Select the **Yes, opt in to employee profiles** option, and select **Opt-in**.

    On the opt-in, employees can use the new employee profile and manage their contact info, bios, and more.

    **Note:** When you opt in to or opt out of the employee profile, the `sn_employee.employee_profile_enabled` value changes.

    Opting in helps with using employee profiles in AI and ML profile data models.

    -   For non-HR customers, AI and ML models are based on the Employee Profile \[sn\_employee\_profile\] table.
    -   The profile page on the portal \[user\_profile page for non-HR customers and hri\_user\_profile page for HR Customers\] uses the employee\_profile page, which is based on the employee profile table.

        **Note:** Customers with an HR license continue to use the HR profile ML model even if they have not opted in to the latest employee profile.

3.  You can opt out of the new employee profile and revert to the previous workflow by selecting **Opt-out** at any time.


## Result

When you opt in, your employees can have the following benefits:

-   View a customizable **Employee Profile** page that details the contact info, job description, and more.
-   Navigate through an enhanced **Org Chart** experience that offers organization chart, team hierarchy, and better search. For more information, see [Organization chart in Employee Center Pro](../concept/employee-profile-org-chart.md).
-   Use employee profile in AI and ML profile data models.

