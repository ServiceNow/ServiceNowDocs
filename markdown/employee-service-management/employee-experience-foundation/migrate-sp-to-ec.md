---
title: Migrate to Employee Center from Service Portal
description: Migrate to the Employee Center portal to provide employees with a unified portal experience.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Admin configurations, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Migrate to Employee Center from Service Portal

Migrate to the Employee Center portal to provide employees with a unified portal experience.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  [Install Employee Center](activate-ec.md) from Store.

2.  Create a unified taxonomy for catalog items and knowledge articles to implement the unified browsing capability.

    For more information, see [Unified Taxonomy for Employee Center](../concept/config-taxonomy.md).

    **Note:** Copy and modify the default taxonomy that comes with the demo data for your business needs.

3.  Add banner and thumbnail images for each topic.

4.  Ensure all request types are captured in **My Request Filters** to consolidate request types.

    For more information, see [Employee requests page](../concept/employee-center-requests-page-configuration.md).

5.  Configure tasks using **To-dos configuration** to include approvals.

    For more information, see [Employee tasks page](../concept/employee-center-to-dos-page-configuration.md).

6.  Modify the portal theme.

    For more information, see [Customize Employee Center portal theme](customize-theme.md).

7.  Use the Email notification layout and template that is shipped with the Employee Experience Foundation \(com.snc.sn\_ex\_emp\_fd\) plugin to deliver notifications that are consistent.

    For more information, see [Modify email notification layout](activate-notification-template.md).

8.  Navigate to **Service Portals** &gt; **Portals** and change the existing portal URL suffix to prevent any breakage of old URL references that an employee has.

9.  If you have any custom built pages, use the page route maps to redirect to appropriate pages of new portal.

10. If any page in new portal doesn’t have equivalent old portal experience, use page route maps to redirect to appropriate pages or portal landing page.

11. Install **Service Portal Analytics** for web analytics.

    1.  Navigate to **Service Portal** &gt; **Portals**.

    2.  Click **Employee Center**.

    3.  Click **Create Analytics Settings**.

        If analytics are already set up, the button updates to View Analytics Settings


