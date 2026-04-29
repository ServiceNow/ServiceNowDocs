---
title: Install Proactive Service Experience Workflows
description: If you’re a user with the system administrator role, you can install the Proactive Service Experience Workflows application.
locale: en-US
release: australia
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Proactive Service Experience Workflow, Configure, Product Support for Technology]
---

# Install Proactive Service Experience Workflows

If you’re a user with the system administrator role, you can install the Proactive Service Experience Workflows application.

## Before you begin

Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

-   Role required: admin
-   Plugins required: The following plugins must have been installed:
    -   Customer Service Management
    -   Customer Service with Service Management
    -   Service Operations Workspace

## About this task

The Telecom core application is installed with Proactive Service Experience Workflows:

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Proactive Service Experience Workflows application \(sn\_ind\_tsm\_sdwan\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can't find the application, you may have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    All dependent plugins and applications that are included, or must be installed are listed in the dialog box.

4.  If demo data is available and you want to install it, select **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

5.  Select **Install**.


**Parent Topic:**[Configuring Proactive Service Experience Workflows](../concept/configure-assurance-workflows.md)

