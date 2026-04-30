---
title: Configure Now Assist in Virtual Agent for Workplace Service Delivery
description: Enable your employees to submit a reservation request using a conversational experience based on generative AI.
locale: en-US
release: zurich
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: task
last_updated: "2026-02-04"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Configure Now Assist in Virtual Agent for Workplace Service Delivery

Enable your employees to submit a reservation request using a conversational experience based on generative AI.

## About this task

Workplace users can leverage the Now Assist in Virtual Agent by configuring the Now Assist for WSD. Now Assist for Workplace Service Delivery \(WSD\) can be configurted to reserve workplace items, invite visitors, and add extra services. The Now Assist in Virtual Agent application provides conversational experiences for Workplace Service Delivery flows.

For more information about Now Assist in Virtual Agent, see [Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

## Before you begin

Make sure that you have installed the following applications from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home):

-   Installing Now Assist for Workplace Service Delivery \(WSD\) activates and installs Now Assist for Platform \(sn\_genai\_platform\)
-   Workplace Reservation Management
-   Workplace Visitor Management

    Workplace Visitor Management is applicable for the **Add Visitors to Reservation** topic block and is optional.

-   Workplace Case Management

    Workplace Case Management is applicable for the **Add Catering to Reservation** topic blocks, and is optional.


**Note:** The following topic blocks are published by default.

-   Add Catering to Reservation
-   Add Zoom to Reservation
-   Add Visitor to Reservation

To run the related subflows, the required application must be installed and the feature must be enabled in the reservable module configuration.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  From the **LLM Assistant** list, select **Now Assist in Virtual Agent**.

3.  Publish the **Reserve Space** topic.

    For more information about publishing a topic, see [Publish a Virtual Agent topic](https://www.servicenow.com/docs/access?context=publish-virtual-agent-topic&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

    The Reserve Space topic is published and can be used from the Virtual Agent.


## What to do next

-   Create a reservable module to group similar workplace items into a category. For more information, see [Configure a reservable module](../../wsd-reservation-management/task/config-reservable-module.md).
    -   Enable virtual meeting links for your reservation by configuring a virtual meeting provider. For more information, see [Configure virtual meeting providers](../../wsd-reservation-management/task/configure-virtual-meeting-providers.md).
    -   Provide extra services, such as catering, for the reservations by creating workplace services and adding them to workplace locations. For more information, see [Create a workplace service to provide an extra service for a reservation](../../wsd-reservation-management/task/create-workplace-service-to-provide-extra-service.md).
-   Select the portals and channels that the Virtual Agent is displayed on. For more information, see [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

    **Note:** Selecting the Workplace Service Portal for Now Assist in Virtual Agent replaces the existing NLU experience.

-   Use the Virtual Agent to reserve a workplace item, add services, and invite visitors. For more information, see  Using Now Assist in VA to reserve a workplace item .

