---
title: Set up response templates in Configurable Workspace
description: Enable or disable agents to access response templates in the email composer.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-11-02"
reading_time_minutes: 1
breadcrumb: [Administering emails in Configurable Workspace, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Set up response templates in Configurable Workspace

Enable or disable agents to access response templates in the email composer.

## Before you begin

Role required: email\_client\_admin

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Select **glide.ui.enable\_response\_templates** from the list or add **glide.ui.enable\_response\_templates** as a system property.

    For instructions on adding a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

3.  Disable response templates by setting the Value field to **false**.

    **Note:** This system property is set to **true**and enabled by default.

4.  Select **Update**.


