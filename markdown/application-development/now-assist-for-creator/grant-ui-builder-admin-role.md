---
title: Grant UI Builder admin role
description: Assign the UI Builder administrator role to a user by editing the user record and adding the ui\_builder\_admin role.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Configure, UI generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Grant UI Builder admin role

Assign the UI Builder administrator role to a user by editing the user record and adding the ui\_builder\_admin role.

## Before you begin

Make sure that you install UI generation and that you have the ui\_builder\_admin role. For more information, see [Install UI generation](install-ui-generation.md) and [Grant UI Builder admin role](grant-ui-builder-admin-role.md).

Configure UI Builder agent. For more information, see [Configure UI Builder Agent](configure-ui-builder-agent.md#).

Role required: admin

## Procedure

1.  In the application navigator, navigate to**All** &gt; **User Administration** &gt; **User**.

2.  Open the user record for the user you want to grant the role to.

3.  In the **Roles related** list, select **Edit**.

4.  From the **Collection** list, select ui\_builder\_admin, and then select ![Add](../../../build/app-engine-studio/image/app-tutorial-move-right-icon.png).

5.  Select **Save**.


## Result

The user is granted the `ui_builder_admin` role and can access UI generation features.

To grant this role to additional users, repeat this procedure for each user.

**Parent Topic:**[Configuring UI generation](../concept/configuring-ui-generation.md)

