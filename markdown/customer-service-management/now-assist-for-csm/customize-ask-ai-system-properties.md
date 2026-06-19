---
title: Customize Case Insights Ask AI button system properties
description: Update the Case Insights Ask AI button system properties to control the drop-down and quick questions displayed on the CSM Case Insights section in your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/now-assist-for-csm/customize-ask-ai-system-properties.html
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-05-21"
reading_time_minutes: 2
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Configure, Now Assist for CSM, Customer Service Management]
---

# Customize Case Insights Ask AI button system properties

Update the Case Insights Ask AI button system properties to control the drop-down and quick questions displayed on the CSM Case Insights section in your instance.

## Before you begin

Role required: admin

-   Now Assist for Customer Service Management \(CSM\) must be installed in your instance.
-   Case summarization, Customer summarization or Special handling notes summarization skills must be activated.

## About this task

System properties control the behavior of the Ask AI feature on the CSM Case Insights section. Two Ask AI properties are available:

-   **sn\_csm\_gen\_ai.ask\_ai\_dropdown\_questions** — controls the drop-down questions displayed for the Ask AI feature on the CSM Case Insights section.
-   **sn\_csm\_gen\_ai.ask\_ai\_quick\_questions** — controls the quick questions displayed for the Ask AI feature on the CSM Case Insights section.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  In the **Name** search field at the top of the list, type `ask_ai`.

    The list filters to show the following two properties:

    -   **sn\_csm\_gen\_ai.ask\_ai\_dropdown\_questions**
    -   **sn\_csm\_gen\_ai.ask\_ai\_quick\_questions**
3.  Select the name of the property you want to configure.

    The **System Property** record opens and displays the following fields:

    -   **Suffix** — the unique suffix of the property name.
    -   **Name** — the full system property name \(read-only\).
    -   **Description** — a description of what the property controls.
    -   **Choices** — available list options, if applicable.
    -   **Type** — the data type of the property \(for example, choice list\).
    -   **Value** — the current value of the property.
    -   **Ignore cache** — when selected, changes take effect without a cache flush.
    -   **Private** — when selected, the property value is hidden from display.
    -   **Read roles** — roles permitted to read this property.
    -   **Write roles** — roles permitted to update this property.
    **Tip:** For the **sn\_csm\_gen\_ai.ask\_ai\_dropdown\_questions** property, the default **Type** is **choice list** and the default **Value** includes: Identify potential root cause, Recommend resolution steps, Show similar resolved issues, Show similar open issues.

4.  In the **Value** field, enter or modify the value as required for your instance.

    For choice list properties, enter each option as a comma-separated list.

5.  In the **Description** field, edit the text to reflect any instance-specific notes or changes to the property.

6.  Select **Update** to save the changes to the property record.


## Result

The Ask AI system property is updated. The new value takes effect for the Ask AI feature on the CSM Case Insights section. If **Ignore cache** is selected, changes are applied immediately without requiring a cache flush.

## What to do next

-   To configure the second Ask AI property, select its name from the list and repeat this procedure.
-   Test the Ask AI feature in the **CSM Configurable Workspace** to verify that the updated questions appear as expected.

