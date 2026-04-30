---
title: Install Conversational Integration with Facebook Messenger
description: You can install the Conversational Integration with Facebook Messenger application \(sn\_va\_fb\_messenger\) if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Conversational Integration with Facebook Messenger, Conversational Integration with Facebook Messenger, Integrating Virtual Agent with consumer messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Install Conversational Integration with Facebook Messenger

You can install the Conversational Integration with Facebook Messenger application \(sn\_va\_fb\_messenger\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## About this task

The following applications or plugins are installed with Conversational Integration with Facebook Messenger:

-   **Conversational Custom Chat Integration \(com.glide.cs.custom.adapter\)**

    Provides custom chat integration framework of scriptable APIs to enable the Virtual Agent application on any conversational interface.

    For more information on this plugin, see [Creating conversational custom chat integrations in Virtual Agent](../concept/va-custom-adapter-framework.md).

-   **ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)**

    Enables execution of Integration Hub actions and flows.


## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Conversational Integration with Facebook Messenger application \(sn\_va\_fb\_messenger\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install Conversational Integration with Facebook Messenger.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


