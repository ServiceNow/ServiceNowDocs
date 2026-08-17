---
title: Grant UI Builder admin role
description: Assign the UI Builder administrator role to a user by editing the user record and adding the ui\_builder\_admin role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/grant-ui-builder-admin-role.html
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Configure, UI generation, UI Builder, Builder library, Developing your application, Building applications]
---

# Grant UI Builder admin role

Assign the UI Builder administrator role to a user by editing the user record and adding the ui\_builder\_admin role.

## Before you begin

Make sure that you install UI generation and that you have the ui\_builder\_admin role. For more information, see [Install UI generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/install-ui-generation.md) and [Grant UI Builder admin role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/grant-ui-builder-admin-role.md).

Configure UI Builder agent. For more information, see [Configure UI Builder Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/configure-ui-builder-agent.md).

Role required: admin

## Procedure

1.  In the application navigator, navigate to**All** &gt; **User Administration** &gt; **User**.

2.  Open the user record for the user you want to grant the role to.

3.  In the **Roles related** list, select **Edit**.

4.  From the **Collection** list, select ui\_builder\_admin, and then select \[Omitted image "app-tutorial-move-right-icon.png"\] Alt text: Add.

5.  Select **Save**.


## Result

The user is granted the `ui_builder_admin` role and can access UI generation features.

To grant this role to additional users, repeat this procedure for each user.

**Parent Topic:**[Configuring UI generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/configuring-ui-generation.md)

