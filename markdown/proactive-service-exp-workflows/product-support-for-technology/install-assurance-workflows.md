---
title: Install Proactive Service Experience Workflows
description: Install the Proactive Service Experience Workflows application on a development or test instance to access demo data and dependent plugins.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/proactive-service-exp-workflows/product-support-for-technology/install-assurance-workflows.html
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: task
last_updated: "2026-07-02"
reading_time_minutes: 2
breadcrumb: [Getting started, Set up your environment, Configure, Proactive Service Experience Workflows, Product Support for Technology]
---

# Install Proactive Service Experience Workflows

Install the Proactive Service Experience Workflows application on a development or test instance to access demo data and dependent plugins.

## Before you begin

Verify that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Verify that the following plugins are installed:

-   Customer Service Management
-   Customer Service with Service Management
-   Service Operations Workspace

Role required: admin

## About this task

If the related plugins aren’t already active, the Proactive Service Experience Workflows plugin activates them. For more information, see [Plugins installed with Proactive Service Experience Workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/product-support-for-technology/psew-plugins.md). The Telecom core application is installed with Proactive Service Experience Workflows:

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Proactive Service Experience Workflows application \(sn\_ind\_tsm\_sdwan\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can't find the application, you might need to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    The dialog box lists all dependent plugins and applications that are included or must be installed.

4.  If demo data is available and you want to install it, select **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

5.  Select **Install**.


## Result

The Proactive Service Experience Workflows application and related plugins are activated. A confirmation message appears after installation is complete.

**Parent Topic:**[Getting started with Proactive Service Experience Workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/product-support-for-technology/getting-started-psew.md)

