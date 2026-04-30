---
title: Configure a provider in Notify
description: Configure a conference provider or a phone number to be used as choices for initiating a conference call. For sending SMS, configure preferences for phone numbers.
locale: en-US
release: yokohama
product: Notify
classification: notify
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure a provider in Notify

Configure a conference provider or a phone number to be used as choices for initiating a conference call. For sending SMS, configure preferences for phone numbers.

## Before you begin

Role required: notify\_admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Provider Selector**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the provider you are adding.|
    |Order|Order in which the provider appears when multiple providers are configured.|
    |Source table|The table to which this provider needs to be added.|
    |Condition|Conditions on the source table based on which provider selectors is applied.|
    |Active|Indicates whether the provider is active.|
    |Catch-all|Selects this provider if no other Provider Selector matches.|
    |Manual selection|Disables the automatic selection of this provider, for example, if in a communication plan you want to use this provider only as a forced communication channel.|

4.  Click **Submit.**

5.  In the Provider Selector Choices section, click **New.**

6.  Search for the conference provider or the Notify group that contains the phone numbers for initiating a conference.

    For sending SMS, search for the Notify group that contains the phone numbers.

7.  Click **Submit.**


**Parent Topic:**[Configuring Notify](../concept/configuring-notify.md)

