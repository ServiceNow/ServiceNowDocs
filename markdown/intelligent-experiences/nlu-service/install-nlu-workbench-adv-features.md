---
title: Install NLU Workbench - Advanced Features
description: You can install the NLU Workbench - Advanced Features application \(com.snc.nlu.workbench.advanced\) if you have the admin role.
locale: en-US
release: xanadu
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [NLU Workbench - Advanced Features, Natural Language Understanding, Enable AI experiences]
---

# Install NLU Workbench - Advanced Features

You can install the NLU Workbench - Advanced Features application \(com.snc.nlu.workbench.advanced\) if you have the admin role.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [NLU Workbench - Advanced Features](https://store.servicenow.com/sn_appstore_store.do#!/store/application/31f5f491c3a710100bf407720f40ddf4) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   NLU Workbench - Advanced Features requires the following plugins. Ensure that these plugins are activated before you install NLU Workbench - Advanced Features.
    -   **Required ServiceNow plugins**
        -   **Predictive Intelligence \(com.glide.platform\_ml\)**

            Enables various Predictive Intelligence and Machine Learning capabilities for training models. See [Predictive Intelligence](../../predictive-intelligence/concept/predictive-intelligence-landing.md).

        -   **NLU Workbench - Core \(com.glide.nlu\)**

            Adds NLU Model capabilities. See [Activate the NLU Workbench](activate-nlu-workbench.md)

        -   **NLU Workbench \(com.snc.nlu\_studio\)**

            Create and train NLU models. See [Activate the NLU Workbench](activate-nlu-workbench.md).


Role required: admin

## About this task

Tables are installed with NLU Workbench - Advanced Features.

For more information, see [Components installed with NLU Workbench - Advanced Features](../reference/installed-with-nlu-wrkbnch-adv-features.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the NLU Workbench - Advanced Features application \(com.snc.nlu.workbench.advanced\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install NLU Workbench - Advanced Features.

4.  Select **Install**.


## What to do next

The following available ServiceNow Store application is installed separately from NLU Workbench - Advanced Features:

-   **Intent Discovery**

    Discover user intents from requests, incidents, or cases to help maximize deflection with Virtual Agent and NLU. For more information, see [Install Intent Discovery](install-intent-discovery.md).


-   **[Components installed with NLU Workbench - Advanced Features](../reference/installed-with-nlu-wrkbnch-adv-features.md)**  
Several types of components are installed with activation of the com.snc.nlu.workbench.advanced plugin, including tables.

**Parent Topic:**[NLU Workbench - Advanced Features](../concept/nlu-workbench-advanced-features.md)

