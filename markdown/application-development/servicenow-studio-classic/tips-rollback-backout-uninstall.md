---
title: Legacy - Roll back, back out, and uninstall
description: The application installation from the application repository is recorded for rollback, which means as an administrator, you can roll back the last installation of a selected application. When you roll back an application, you remove all code, table, and file updates from the initial installation.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Legacy - Production deployment tips, Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Roll back, back out, and uninstall

The application installation from the application repository is recorded for rollback, which means as an administrator, you can roll back the last installation of a selected application. When you roll back an application, you remove all code, table, and file updates from the initial installation.

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

Source control installations are not recorded for rollback, which means that the rollback feature to undo an application repository, store installation, or an in-family upgrade is not available for source control installations. They also cannot be uninstalled in the same sense that ServiceNow® Store applications can be \(that is, with the option to retain tables and columns\). They can be deleted by deleting the **sys\_app** record. However, for scoped applications, this destroys the underlying schema and its data.

You cannot delete global applications until all application files are moved to another global application. Deleting a **sys\_app** record for an application also creates **sys\_update\_xml** records with **DELETE** payloads. These payloads can generate skips if the same application is then installed via the application repository or ServiceNow Store.

To avoid these skips, the **sys\_update\_xml** records must be manually deleted before the application is installed from the application repository. Installing from source control also does not have the [Back out](../../system-update-sets/task/t_BackOutUpdateSet.md) option that update sets contain to remove a subset of new changes. That means that recoverability in this model is limited to installing a corrected version \(older or newer\) of the application on top of the current version. This action restores only metadata or configuration. Data lost as a result of a poor installation must be recovered from a database restore.

**Parent Topic:**[Legacy - Production deployment tips](tips-production-deployment.md)

