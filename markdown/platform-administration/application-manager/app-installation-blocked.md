---
title: App installation blocked when installing or updating Now Assist Suite
description: Unlicensed applications can block the installation or update of Now Assist Suites.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/application-manager/app-installation-blocked.html
release: zurich
product: Application Manager
classification: application-manager
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Application Manager, Administering applications, Get started, Administer]
---

# App installation blocked when installing or updating Now Assist Suite

Unlicensed applications can block the installation or update of Now Assist Suites.

## Symptom

When attempting to update or install a Now Assist application, another application that is part of the same Now Assist Suite displays an "Installation blocked" indicator in the installation details. The update or installation can't be completed.

\[Omitted image "app-mgr-installation-blocked.png"\] Alt text: The installation details for Now Assist for Customer Service Management show "Installation blocked" next to Flow Generation version 28.2.5. The option to Continue installing Now Assist for Customer Service Management is inactive.

## Cause

The application version that displays "Installation blocked" isn't licensed.

## Resolution: License the required application version

## Procedure

1.  If your organization uses the application, license the version required for the Now Assist Suite installation.

    To license the necessary application version, contact your account executive or request the license through the ServiceNow Store. For more information about licensing applications through the ServiceNow Store, see [Buy a ServiceNow application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/buy-servicenow-app.md).


## Resolution: Uninstall the application

## Procedure

1.  If your organization doesn't use the application that blocks installation, uninstall it through the Application Manager.

    For more information about uninstalling applications, see [Uninstall an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/application-manager/uninstall-application-app-mgr.md).


**Parent Topic:**[Application Manager reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/application-manager/app-mgr-reference.md)

