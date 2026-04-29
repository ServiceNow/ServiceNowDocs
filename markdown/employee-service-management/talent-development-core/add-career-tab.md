---
title: Add the Career tab and enable the Skills widget in the Employee Profile
description: Add the Career tab and enable the Skills widget in the Career tab to upload your resume/LinkedIn profile and work with skills-related data in your Employee Profile.
locale: en-US
release: australia
product: Talent Development Core
classification: talent-development-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Skills Foundation, Skills Foundation, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Add the Career tab and enable the Skills widget in the Employee Profile

Add the **Career** tab and enable the Skills widget in the Career tab to upload your resume/LinkedIn profile and work with skills-related data in your Employee Profile.

## Before you begin

Role required: sn\_skills\_int.admin, sn\_skills\_int.emp

## Procedure

1.  Navigate to **All** &gt; **Employee Profile** &gt; **Employee Definitions**.

    1.  Select sys\_user employee definition.

        **Note:** If you don't see an employee definition, create one by selecting **New** and saving it.

    2.  Select **Generate Employee Profiles**.

2.  Navigate to **All** &gt; **Employee Profile** &gt; **Setup**.

    1.  Select **Opt-in** to choose employee profiles.

3.  To enable Skills widget in the **Career** tab, navigate to **All** &gt; **System Properties** &gt; **All properties**.

    1.  Search the Name column with `*skill`.

    2.  Select the sn\_skills\_int.enable\_skills property.

    3.  Set the Value field to **True**.

    **Note:** Make sure that you have the appropriate Read roles and Write roles as displayed in the property.


## Result

The Career tab and Skills widget are added to your profile in the Employee Center.

