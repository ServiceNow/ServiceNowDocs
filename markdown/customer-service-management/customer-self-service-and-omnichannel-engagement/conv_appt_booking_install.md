---
title: Install Conversational Appointment Booking
description: Install the Conversational Appointment Booking application \(sn\_va\_appt\_schedul\) if you have the admin role. The application installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: zurich
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure Conversational Appointment Booking, Set up self-service, Configure, Customer Service Management]
---

# Install Conversational Appointment Booking

Install the Conversational Appointment Booking application \(sn\_va\_appt\_schedul\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## About this task

Conversational Appointment Booking requires the following plugins. Ensure that these plugins are activated before you install Conversational Appointment Booking.

-   **Required ServiceNow plugins**
    -   **Walk-Up for CSM \(com.snc.walkup\_for\_csm\)**

        **Note:** Conversational Appointment Booking can be used without the Walk-Up for CSM plugin. However, custom control and Virtual Agent topic blocks shown in [Configure Conversational Appointment Booking](conv-appt-booking-config.md) cannot be used without this plugin.

        The following items are installed with this plugin:

        -   NLU model for Conversational Appointment Booking.

            **Note:** In order to use the NLU model, you need to train and publish the model. See [Natural Language Understanding](https://www.servicenow.com/docs/access?context=nlu-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

        -   Virtual Agent topics: Schedule a Walk-up appointment, Reschedule a Walk-up appointment, and Cancel a Walk-up appointment.
        -   Virtual Agent topic blocks: Get Walk-up location and Walk-up appointment scheduling.
    -   **Appointment Booking \(com.snc.appointment\_booking\)**

        Enables the appointment booking feature for Walk-up Experience.

    -   **Glide Virtual Agent \(com.glide.cs.chatbot\)**

        Activates the Virtual Agent platform. Virtual Agent requires additional licensing. See [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) for more information.

    -   **NLU Workbench \(com.snc.nlu\_studio\)**

        Enables the creation of custom ServiceNow Natural Language Understanding models used by Virtual Agent.

    -   **Studio \(com.glide.dev-studio\)**

        Used for adding and updating application files.


For information about plugin activation, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Conversational Appointment Booking application \(`sn_va_appt_schedul`\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install Conversational Appointment Booking.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


