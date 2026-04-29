---
title: Configure the E.164 format for a consumer phone number
description: Ensure that all the necessary information for a phone number is included and properly formatted to successfully route an international call over a territory's public telephone network. Provide the E.164-compliant formatting and validation for phone number.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up ServiceNow Voice, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the E.164 format for a consumer phone number

Ensure that all the necessary information for a phone number is included and properly formatted to successfully route an international call over a territory's public telephone network. Provide the E.164-compliant formatting and validation for phone number.

## Before you begin

Role required: admin

## About this task

An E.164 phone number field displays the following field types:

-   A list for the phone number territory
-   An input box for entering phone numbers

The E.164 format that does not contain any dashes or spaces and must include the + sign. For example, +14152223456.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Consumers**.

2.  Select the required consumer record.

3.  On the Consumer form, right-click any phone field and select **Configure Dictionary**.

4.  On the Dictionary Entry form, for the **Type** field, select **Phone Number \(E164\)**.

5.  Click **Update**.


## Result

After this configuration, when entering the consumer phone number in the phone field, select the territory and enter the corresponding phone number. The same format is reflected in Agent Workspace.

**Parent Topic:**[Setting up ServiceNow Voice](../concept/ccc-setup.md)

