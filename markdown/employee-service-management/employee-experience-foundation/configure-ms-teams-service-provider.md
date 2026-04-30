---
title: Make Microsoft Teams the default communication channel
description: Make Microsoft Teams the default communication channel to initiate a conference call to resolve a ticket.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Notify connector, Microsoft Teams integration for Agent Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Make Microsoft Teams the default communication channel

Make Microsoft Teams the default communication channel to initiate a conference call to resolve a ticket.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Provider Selector**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the provider you are adding, for example, Microsoft Teams.|
    |Order|Order in which this provider appears when multiple providers are configured.|
    |Source table|The table to which Microsoft Teams must be added.|
    |Condition|Field to add the filter conditions.|
    |Active|Option for indicating whether Microsoft Teams as a provider is active.|
    |Catch-all|Option for making Microsoft Teams the default provider if other notify providers like Zoom or Twilio are configured.|
    |Manual Selection|Option for disabling the automatic selection of this provider.|

4.  Select **Submit**.

    The list of service providers displays.

5.  Select the created service provider.

6.  Select **New** in the **Provider Selector Choices** section.

    1.  Select either **Notify number group** to choose the required notify group or select **Conference provider** to choose Microsoft Teams.

        You can set up configurations for numerous conference providers within the Notify framework.

        For example, you can configure Microsoft Teams as a provider for all the conferences initiated from incidents, and Zoom as the provider for all the conferences related to change or problem.

        **Note:** Selecting both values results in error.

    2.  Select **Submit**.


**Parent Topic:**[Configure Notify connector for Microsoft Teams](../concept/config-notify-ms-teams.md)

