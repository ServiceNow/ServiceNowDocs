---
title: Install or update the ServiceNow IDE
description: Install or update the ServiceNow IDE application \(sn\_glider\) from the ServiceNow Store.
locale: en-US
release: zurich
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Install or update the ServiceNow IDE

Install or update the ServiceNow IDE application \(sn\_glider\) from the ServiceNow® Store.

## Before you begin

Review the [ServiceNow IDE](https://store.servicenow.com/sn_appstore_store.do#!/store/application/fd254d9443a161100967247e6bb8f200) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

ServiceNow IDE is active by default on instances on the Zurich release. Update to the latest version of the ServiceNow IDE to use the latest features.

## Procedure

1.  Navigate to **Admin** &gt; **Application Manager**.

2.  Search for the ServiceNow IDE application \(sn\_glider\).

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

3.  Select the ServiceNow IDE application \(sn\_glider\).

4.  Select **Install** or **Proceed to Update**.

    In the Review Installation Details dialog box, you can select the version to install, review any dependencies that are installed along with your application, and select whether to install the application now or later.

5.  In the dialog box, select **Install**.


## What to do next

Create a workspace for your applications. For more information, see [Create a workspace in the ServiceNow IDE](create-workspace-servicenow-ide.md).

ServiceNow IDE uses the public npm registry \(`https://registry.npmjs.org`\) as its default package source. If your network blocks access to this registry, you must have access to an alternate registry to download packages and build applications in the ServiceNow IDE. If access to the public npm registry is blocked on your system, you must configure a private npm registry in your Package Manager user settings in the ServiceNow IDE. For more information, see [Install an npm package from a private registry with the ServiceNow IDE](use-library-private-npm-registry.md).

**Parent Topic:**[Configuring the ServiceNow IDE](../concept/configuring-servicenow-ide.md)

