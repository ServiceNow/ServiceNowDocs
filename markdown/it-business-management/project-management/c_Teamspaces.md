---
title: Teamspaces
description: A teamspace appears as an application in the instance application navigator. The teamspace includes module links that come from the Project Portfolio Management applications, such as the Project, Idea, Demand, Program and Portfolio applications.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Teamspaces

A teamspace appears as an application in the instance application navigator. The teamspace includes module links that come from the Project Portfolio Management applications, such as the Project, Idea, Demand, Program and Portfolio applications.

Use teamspaces to provide functional and data separation of these applications between different teams in your organization. The following is an example teamspace for a marketing team:

![An example teamspace for marketing](../image/marketing_teamspace.png "Example teamspace")

## Teamspace activation

You must activate a teamspace plugin to use the teamspace feature. Following teamspace plugins are available:

-   **Project Management TeamSpace 1** \(`com.snc.ppm_teamspace_1`\)
-   **Project Management TeamSpace 2** \(`com.snc.ppm_teamspace_2`\)
-   **Project Management TeamSpace 3** \(`com.snc.ppm_teamspace_3`\)
-   **Project Management TeamSpace 4** \(`com.snc.ppm_teamspace_4`\)
-   **Project Management TeamSpace 5** \(`com.snc.ppm_teamspace_5`\)

The teamspaces loaded with these plugins contain the same components, but the components have different prefixes. For example, teamspace 1 includes a project table named **Teamspace\_1 Project \[tsp1\_project\]** and teamspace 5 includes a project table named **Teamspace\_5 Project \[tsp5\_project\]**.

You can enable any or all of these teamspaces and assign the teamspace specific roles to relevant users in the group that should use the teamspace. Maximum five teamspaces can be created through plugins.

## Teamspace customization

You can customize the Project and Demand portions of a teamspace without affecting other teamspaces. This table summarizes what you can customize:

|Customization to Project or Demand within a teamspace|Supported?|
|-----------------------------------------------------|----------|
|Data model changes, such as adding a field to the Project or Demand form.|Yes|
|Changes to business rules, UI actions, UI policies, security rules, data policies, and workflows.|Yes|
|Changes to shared roles, such as project\_manager, demand\_manager, and so on.|Yes|
|Form and list layouts, list controls, and related lists|Yes|
|Dictionary overrides|Yes|

