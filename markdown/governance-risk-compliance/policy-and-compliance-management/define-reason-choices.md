---
title: Define policy exception reason choices
description: You can define reason choices to be available to any user who requests an exception.
locale: en-US
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Allow policy exception requests, Enhancement steps, Implement, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Define policy exception reason choices

You can define reason choices to be available to any user who requests an exception.

## Before you begin

Role required: sn\_compliance.manager

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Policy Exceptions** &gt; **Exception Reason Choices**.

2.  Click **New**.

    ![Reason Choice List](../image/reason-choice-list.png)

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Label|Enter a unique label for this choice.|
    |Value|Enter a unique value for this choice.|
    |Order|Enter an order for this choice. Reasons are ordered based on this number.|
    |Default|Select this check box to indicate that this reason choice will be available whenever an ad hoc policy exception is requested. If the integration registry does not contain any application-specific choices, all reason choices with **Default** selected will be available.|
    |Active|If this is selected, this choice is displayed in the list of reason choices.|

4.  Click **Submit**.

    The reason choice is added and will be available in the **Reason** field of the policy exception request form for the selected application.

5.  Repeat this process for as many reason choices as required by your users.

    **Note:** For additional details about this process, see [KB0783018](https://support.servicenow.com/nav_to.do?uri=%2Fkb_knowledge.do%3Fsys_id%3Dca72a764db1fc050d82ffb243996194e).


**Parent Topic:**[Allow policy exception requests from other applications](../concept/allow-other-app-policy-except.md)

