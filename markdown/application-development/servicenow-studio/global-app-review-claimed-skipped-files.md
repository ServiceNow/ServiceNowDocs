---
title: Legacy - Review claimed or skipped global files
description: Review files when one or more of your files has been skipped or claimed by another application.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Legacy - Global application file management, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Review claimed or skipped global files

Review files when one or more of your files has been skipped or claimed by another application.

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [Building applications with ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

During the development of a global application, warnings about skipped or claimed files may display on various progress screens. Skipped or claimed files can occur when the files in one application are claimed by other application\(s\).

These warnings display during the installation of an application from the Application or Git repositories or when you publish your application. When you see that your application files have been either skipped or claimed by another application, contact the team that owns the other application to determine the best course of action for both teams.

## What your options are

Only one version can be loaded for production. The options are as follows.

-   Decide with the other team from which application the file should be removed so that only one file is loaded for production.
-   Use the Merge tool: If changes to files in both apps are needed in production, use the merge tool to pull the files into a new common application that serves both parties effectively.

To learn more see the [Legacy - Resolve conflicts](../task/t_ResolveConflicts.md) topic.

**Parent Topic:**[Legacy - Global application file management](manage_global_application_files.md)

