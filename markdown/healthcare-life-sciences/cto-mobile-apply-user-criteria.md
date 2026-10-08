---
title: Apply user criteria to Field Service Management Mobile quick actions
description: Apply the user criteria records provided with Care Team Operations to Field Service Management Mobile quick-action icons so that each care team role sees only the icons relevant to its work.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/cto-mobile-apply-user-criteria.html
release: brazil
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
breadcrumb: [Configure Care Team Mobile, Care Team Mobile, Healthcare Operations, Healthcare and Life Sciences]
---

# Apply user criteria to Field Service Management Mobile quick actions

Apply the user criteria records provided with Care Team Operations to Field Service Management Mobile quick-action icons so that each care team role sees only the icons relevant to its work.

## Before you begin

For the list of available user criteria records and the role each one maps to, see [User criteria for Care Team Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/cto-mobile-user-criteria.md).

Role required: admin

## Procedure

1.  Navigate to **Mobile App Builder**.

2.  Select **Care Team Mobile App**.

3.  Select the quick-action icon that you want to restrict.

    For example, My Group Tasks or My task map.

4.  Navigate to **User criteria access** and select **Choose**.

5.  In the user criteria picker, select one or more user criteria records.

    For example, select **Biomed Support Agent** to show the icon to Biomed support agents, or **HCO Location Support Agent** to show it to support agents in all four departments.

6.  Select **Apply**.


## Result

The icon is visible to users who match the selected user criteria, with no additional configuration needed.

