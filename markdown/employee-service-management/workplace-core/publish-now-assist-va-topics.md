---
title: Publish Now Assist in Virtual Agent topics for Workplace Service Delivery
description: Publish Virtual Agent topics to enable your employees to submit a reservation request by using Now Assist in Virtual Agent.
locale: en-US
release: xanadu
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2024-08-05"
reading_time_minutes: 3
keywords: [=]
breadcrumb: [Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Publish Now Assist in Virtual Agent topics for Workplace Service Delivery

Publish Virtual Agent topics to enable your employees to submit a reservation request by using Now Assist in Virtual Agent.

## About this task

A Virtual Agent topic is created to meet a specific objective or goal, such as fulfilling a user's request. To enable a feature in the Virtual Agent, you must publish the topic. For more information about Virtual Agent topics, see [Create a Virtual Agent topic](https://www.servicenow.com/docs/access?context=create-virtual-agent-topic&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

Topic blocks are reusable components to run common tasks and conversational elements in Virtual Agent conversations. For more information about topic blocks, see [Maximizing code reuse with topic blocks](https://www.servicenow.com/docs/access?context=topic-blocks-overview&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

## Before you begin

Make sure that you are on the Xanadu release and the following applications are installed on your instance. If they aren't installed, add the applications from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

-   Now Assist for HR Service Delivery \(HRSD\)

    For more information about the application, see [Now Assist for HR Service Delivery \(HRSD\)](../../human-resources/concept/now-assist-hrsd.md).

-   Workplace Reservation Management

    For more information about the application, see [Workplace Reservation Management](../../wsd-reservation-management/concept/workplace-rsv-mgmt-feat.md).

-   Workplace Visitor Management

    For more information about the application, see [Workplace Visitor Management](../../workplace-visitor-mgmt/concept/workplace-visitor-mgmt-feat.md)

-   Workplace Case Management

    For more information about the application, see [Workplace Case Management](../../workplace-case-mgmt/concept/workplace-case-mgmt-feat.md).


**Note:** to

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  In the LLM Assistant list, select **Now Assist in Virtual Agent**.

3.  Publish the **Reserve Space** topic.

    For more information about publishing a topic, see [Publish a Virtual Agent topic](https://www.servicenow.com/docs/access?context=publish-virtual-agent-topic&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

    The Reserve Space topic is published and can be used from Virtual Agent.


## What to do next

-   [Configure a reservable module](../../wsd-reservation-management/task/config-reservable-module.md).
    -   [Configure virtual meeting providers](../../wsd-reservation-management/task/configure-virtual-meeting-providers.md).
    -   [Create a workplace service to provide an extra service for a reservation](../../wsd-reservation-management/task/create-workplace-service-to-provide-extra-service.md).
-   Select the portals and channels that Virtual Agent is displayed on. For more information, see [Configuring Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

    **Note:** Enabling Now Assist in Virtual Agent for Workplace Service Portal replaces the existing NLU experience.

-   Use Virtual Agent to reserve a workplace item, add services, add coworkers, or invite visitors. For more information, see  [Using Now Assist in Virtual Agent topics for Workplace Service Delivery](../concept/use-now-assist-in-virtual-agent-wsd.md).

