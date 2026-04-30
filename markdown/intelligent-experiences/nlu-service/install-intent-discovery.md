---
title: Install Intent Discovery
description: You can install the Intent Discovery application \(sn\_nlu\_discovery\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: zurich
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Intent Discovery, NLU Workbench - Advanced Features, Natural Language Understanding, Enable AI experiences]
---

# Install Intent Discovery

You can install the Intent Discovery application \(sn\_nlu\_discovery\) if you have the admin role.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Intent Discovery](https://store.servicenow.com/sn_appstore_store.do#!/store/application/abcdef8b072f00109c257a76fed300c1) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Intent Discovery requires the following plugins. Ensure that these plugins are activated before you install Intent Discovery.
    -   **Required ServiceNow plugins**
        -   **Predictive Intelligence \(com.glide.platform\_ml\)**

            Enables various Predictive Intelligence and Machine Learning capabilities for training models. See [Install Predictive Intelligence](../../predictive-intelligence/task/install-predictive-intelligence.md#).

        -   **NLU Workbench - Core \(com.glide.nlu\)**

            Adds NLU Model capabilities. See [Activate the NLU Workbench](activate-nlu-workbench.md).


Role required: admin

## About this task

Tables are installed with Intent Discovery:

For more information, see [Components installed with Intent Discovery](../reference/installed-with-intent-discovery.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Intent Discovery application \(sn\_nlu\_discovery\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install Intent Discovery.

4.  Select **Install**.


-   **[Components installed with Intent Discovery](../reference/installed-with-intent-discovery.md)**  
Several types of components are installed with activation of the sn\_nlu\_discovery plugin, including tables.

**Parent Topic:**[Intent Discovery](../concept/intent-discovery.md)

