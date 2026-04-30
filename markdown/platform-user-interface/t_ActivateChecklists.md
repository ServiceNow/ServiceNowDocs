---
title: Activate checklists
description: Checklists are active by default on new instances. For instances upgrading from a previous version, the Checklist plugin must be activated.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Checklists, Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Activate checklists

Checklists are active by default on new instances. For instances upgrading from a previous version, the Checklist plugin must be activated.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Checklist plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Checklists](../concept/c_Checklists.md)

**Related topics**  


[Create a checklist](t_CreateAChecklist.md)

[Delete checklist or a template](t_DeleteAChecklist.md)

