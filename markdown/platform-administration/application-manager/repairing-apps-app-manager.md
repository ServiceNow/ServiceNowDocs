---
title: Repairing applications and plugins
description: Repairing an application or plugin returns it to its original state without needing to uninstall and reinstall it manually. Repairing applications or plugins can help resolve issues related to accidental modifications or corrupted files.
locale: en-US
release: australia
product: Application Manager
classification: application-manager
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Repairing applications and plugins

Repairing an application or plugin returns it to its original state without needing to uninstall and reinstall it manually. Repairing applications or plugins can help resolve issues related to accidental modifications or corrupted files.

## Overview of repairing applications and plugins

When you repair an application or plugin, all the files with sys\_update\_xml records are added to the remote update set. The remote update set is named with the format: "Repair/Upgrade app &lt;app scope name&gt; at &lt;timestamp&gt;".

## Repairing applications with customizations

When you repair an application with a customization, the customization is also repaired unless it's linked to a source control repository.

It’s assumed the complete set of customizations for an application is within the application customization. When repairing, installing, or upgrading the underlying application or plugin that has an associated app customization, changes made outside of that application customization are overwritten.

For more information about customizations, see [Customization vs. configuration with Creator Studio](https://www.servicenow.com/docs/access?context=creator-studio-custom-vs-config&version=australia&pubname=australia-application-development&ft:locale=en-US).

-   **[Repair an application or plugin](../task/repair-application-app-mgr.md)**  
Repair an application procured through the ServiceNow Store or a plugin included in your instance. Repairing apps or plugins can resolve issues caused by unintentional modifications, corrupted files, or partial deletion.

**Parent Topic:**[Administering applications](../../../build/applications/reference/administering-applications.md)

