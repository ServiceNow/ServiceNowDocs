---
title: Use a custom tab for the Career tab in Skills Foundation
description: Use a custom tab as a replacement for the Career tab in Employee Profile by updating the tab ID so employees are redirected to this custom tab.
locale: en-US
release: australia
product: Talent Development Core
classification: talent-development-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Skills Foundation, Skills Foundation, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Use a custom tab for the Career tab in Skills Foundation

Use a custom tab as a replacement for the **Career** tab in Employee Profile by updating the tab ID so employees are redirected to this custom tab.

## Before you begin

Create a custom tab to display skills-related content in the employee profile. For more information on creating a tab, see [Manage profile tabs and visibility in Employee Profile](../../employee-center/task/manage-employee-profile-tabs-visibility.md).

Role required: sn\_skills\_int.admin, sn\_hr\_sp.esc\_admin

## Procedure

1.  Access the sys\_id of the custom tab.

    1.  Navigate to **All** &gt; **Employee Profile** &gt; **Profile Tabs**.

    2.  Select the tab that you want to use instead of the **Career** tab.

    3.  Select the Additional actions icon \(![Additional actions icon](../../human-resources/image/additional-actions-icon.png)\) and select **Copy sys\_id**.

2.  Access the sn\_skills\_int-tab\_id system property.

    1.  Select **All**.

    2.  In the navigation filter, type `sys_properties.list`.

    3.  Search for `*skill` in the **Name** field.

    4.  Select sn\_skills\_int.tab\_id.

    5.  In the **Value** field, replace the existing value with the sys\_id of the customized tab.

    6.  Select **Update**.


## Result

The employee will be directed to the customized tab to view and modify the skills in Employee Profile.

