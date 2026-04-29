---
title: Upgrade to Employee Center Pro from Employee Service Center \(HR\)
description: Migrate to the Employee Center Pro portal to provide employees with a unified portal and content experiences.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Upgrading to Employee Center Pro, Admin configurations, Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Upgrade to Employee Center Pro from Employee Service Center \(HR\)

Migrate to the Employee Center Pro portal to provide employees with a unified portal and content experiences.

## Before you begin

Role required: admin

## About this task

Employee Center is delivered to all customer as a default application, and Employee Center Pro is a licensed application and must be separately installed. For more information, see [Install Employee Center Pro](install-ec-pro.md).

**Note:** If you are an existing customer using Employee Service Center, to experience the enhanced content experience capabilities, you must update to the latest Employee Center Pro application from ServiceNow Store. For more information on the installation steps, see [Install Employee Center Pro](install-ec-pro.md).

## Procedure

1.  [Install Employee Center Pro](install-ec-pro.md) to get the latest features.

2.  Navigate to **System Definition** &gt; **Fix Scripts**.

    **Note:** Run the **Fix Scripts** only if you want to reset the existing portal home page and the topic pages to the default Employee Center home page.

3.  Ensure your application scope is set to **Employee Center Core**.

4.  Click open the **Employee Center Easy Install** fix script.

5.  On the line `"var runManually = false"`, change the value **false** to **true**.

6.  Run the fix script.

7.  [Clone taxonomy for employee content](clone-taxonomy-content.md).

8.  [AI Search for Curated Experiences](align-search-for-curated-exp.md)

9.  Configure **My Active Items** widget.

    For more information, see [My active items widget configuration](../concept/my-activity-config.md).

10. Configure **Quick Links**.

    For more information, see [Quick links](../concept/emp-center-quick-link-config.md).

11. Configure the portal footer.

    For more information, see [Footer configuration](../concept/emp-center-footer-config.md).


## Result

This upgrades the Employee Service Center with the latest Employee Center Pro themes and capabilities.

**Parent Topic:**[Upgrading to Employee Center Pro](../concept/upgrade-steps.md)

