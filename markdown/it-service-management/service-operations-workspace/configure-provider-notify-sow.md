---
title: Configure a provider for Notify in Service Operations Workspace
description: Configure a conference provider to be used as a choice for initiating a conference call.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-04-17"
reading_time_minutes: 1
breadcrumb: [Configuring Notify in Service Operations Workspace, Configuring Service Operations Workspace for ITSM to improve your experience, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure a provider for Notify in Service Operations Workspace

Configure a conference provider to be used as a choice for initiating a conference call.

## Before you begin

Role required: notify\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace Admin Center** &gt; **Configurations**.

2.  Select **Notify**, and then select **Configure** corresponding to **Configure your provider preferences**.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the provider.|
    |Order|Order in which the provider appears when multiple providers are configured.|
    |Source table|Table to which this provider must be added.|
    |Condition|Conditions on the source table based on which provider selectors are applied.|
    |Active|Indicates whether the provider is active.|
    |Catch-all|Selects this provider if no other provider selector matches.|
    |Manual selection|Disables the automatic selection of this provider, for example, if in a communication plan you want to use this provider only as a forced communication channel.|

5.  Select **Submit.**

6.  In the **Provider Selector Choices** section, select **New.**

7.  Search for the conference provider or the Notify group that contains the phone numbers for initiating a conference call.

    For sending SMS, search for the Notify group that contains the phone numbers.

8.  Select **Submit.**


**Parent Topic:**[Configuring Notify in Service Operations Workspace](../concept/configure-notify-sow.md)

