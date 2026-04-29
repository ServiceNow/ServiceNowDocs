---
title: Configure script fields for a workspace
description: Configure a Configurable Workspace to support script fields.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Forms, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure script fields for a workspace

Configure a Configurable Workspace to support script fields.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table opens.

2.  Show script fields in forms with a code editor component.

    1.  Add a system property named **glide.ui.workspace.script.code\_editor.enable**.

        For more information on adding system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

    2.  Set the Value to **true**.

    3.  Select **Submit**.

3.  Configure the line number after which the scroll bar should appear for the code editor component.

    1.  Add a system property named **glide.ui.workspace.script.code\_editor.autoresize\_line\_limit**.

        For more information on adding system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

    2.  Select **Submit**.


