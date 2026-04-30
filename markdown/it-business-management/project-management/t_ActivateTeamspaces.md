---
title: Activate teamspaces
description: You can activate one or all teamspace plugins to use the teamspaces feature.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Teamspaces in Project Management, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Activate teamspaces

You can activate one or all teamspace plugins to use the teamspaces feature.

## Before you begin

Role required: admin

## About this task

You must activate a teamspace plugin to use the teamspace feature. Following teamspace plugins are available:

-   **Project Management TeamSpace 1** \(`com.snc.ppm_teamspace_1`\)
-   **Project Management TeamSpace 2** \(`com.snc.ppm_teamspace_2`\)
-   **Project Management TeamSpace 3** \(`com.snc.ppm_teamspace_3`\)
-   **Project Management TeamSpace 4** \(`com.snc.ppm_teamspace_4`\)
-   **Project Management TeamSpace 5** \(`com.snc.ppm_teamspace_5`\)

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Using Teamspaces in Project Management](../concept/c_Teamspaces.md)

**Related topics**  


[Installed with teamspaces](../reference/r_InstalledWithTeamspaces.md)

[Configure teamspace settings](../reference/t_EnableATeamspace.md)

