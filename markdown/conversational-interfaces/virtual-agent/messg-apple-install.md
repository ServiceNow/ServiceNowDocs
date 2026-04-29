---
title: Install Conversational Integration with Apple Messages for Business
description: Install the Conversational Integration with Apple Messages for Business so that your business can interact with requesters on the Apple Messages for Business app. The application installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Conversational Integration with Apple Messages for Business, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Install Conversational Integration with Apple Messages for Business

Install the Conversational Integration with Apple Messages for Business so that your business can interact with requesters on the Apple Messages for Business app. The application installs related ServiceNow Store applications and plugins if they are not already installed.

## Before you begin

-   Review the [Conversational Integration with Apple Messages for Business](https://tpp.servicenow.com/sn_appstore_store.do#!/tpp/application/previewapplication/2c8e70a91b06a1103ee8a8ea234bcb9f) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Create an Apple Messages for Business account at [Apple Business Register](https://register.apple.com/login?returnTo=/business/ui).

Role required: admin

## About this task

The following applications or plugins are installed with Conversational Integration with Apple Messages for Business:

-   **Conversational Custom Chat Integration \(com.glide.cs.custom.adapter\)**

    Provides custom chat integration framework of scriptable APIs to enable the Virtual Agent application on any conversational interface.

    For more information on this plugin, see [Creating conversational custom chat integrations in Virtual Agent](../concept/va-custom-adapter-framework.md).

-   **ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)**

    Enables execution of Integration Hub actions and flows.

-   **IHUB Spoke Util Pack \(com.snc.ihub\_spoke\_util\_pack\)**

    Enables utility or global scripts that can be invoked from the Integration Spokes.

-   **Conversational Messaging \(com.glide.messaging.awa\)**

    Enables messaging actions that are performed when an event occurs.


The following applications and plugins are not installed with Conversational Integration with Apple Messages for Business, but are required in order to use specific features.

-   **Conversational Appointment Booking \(sn\_va\_appt\_schedul\)**

    Book, reschedule, and cancel appointments from Virtual Agent conversations. This application is required in order to use the time picker feature in Apple Messages for Business.

-   **Payment framework for conversational channels \(sn\_va\_payment\_ctrl\)**

    Enables the payment framework custom control for live agent and virtual agent conversations in Apple Messages for Business.


## Procedure

1.  Make sure that your Apple Messages for Business account is set up and active.

    See the [Apple documentation](https://register.apple.com/resources/messages/messaging-documentation/) for more information.

2.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

3.  Find the Conversational Integration with Apple Messages for Business application \(sn.va.abc.adapter\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

4.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

5.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

6.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

7.  Select **Install**.


