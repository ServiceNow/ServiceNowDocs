---
title: Set the order of your workspaces in the Unified Navigation Workspaces menu
description: Set the order of your workspaces and control how they appear in the Unified Navigation Workspaces menu.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/configure-user-experiences/set-order-workspace-unified-navigation.html
release: zurich
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Set the order of your workspaces in the Unified Navigation Workspaces menu

Set the order of your workspaces and control how they appear in the Unified Navigation Workspaces menu.

## Before you begin

To enable ordering of your workspaces, you must create a system property **glide.ui.next\_experience.workspace\_sorting** and set the value to **Order**. For more information, see .

Role required: admin

## Procedure

1.  In the filter navigator field, enter `sys_ux_registry_m2m_category_list.do` and press **Enter**.

    The UX Application Category M2Ms table appears. This table is used to store the association between an application and the experience category.

2.  Select the Preview record icon \[Omitted image "next-exp-preview-record.png"\] Alt text: for the workspace that you want to order.

3.  Select **Open Record** to open the UX Application Category M2M form.

4.  In the **Order** field, enter a numerical value.

    **Note:** The lowest ordered workspace appears first in the Workspaces menu.

5.  Select **Update**.


**Parent Topic:**[Configuring the Next Experience UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/next-experience-ui-admin.md)

