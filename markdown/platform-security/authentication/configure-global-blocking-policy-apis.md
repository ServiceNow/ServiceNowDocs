---
title: Configure global blocking policy for APIs
description: Global blocking policy denies the authentication requests of users and APIs based on the specified policy conditions. This policy can be used as an alternative to the IP Address Access Control.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [API Authentication Policies, API access policy, Authentication, Access Management]
---

# Configure global blocking policy for APIs

Global blocking policy denies the authentication requests of users and APIs based on the specified policy conditions. This policy can be used as an alternative to the IP Address Access Control.

## Before you begin

Role required: api\_service\_admin, adaptive\_auth\_policy\_admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **API Access Policies** &gt; **Global Blocking Policy**.

2.  From the **Policy Inputs** tab, click **Edit**.

3.  Select one or more filter criteria from the **Collection** list and move them to **Global Blocking Policy** list.

    You can also add additional filters.

4.  From the **Policy Conditions** tab, click **New**.

5.  On the form, fill these fields:

    |Field|Description|
    |-----|-----------|
    |Label|Name to identify the condition.|
    |Description|Description of the condition.|
    |Condition|Logical combination of multiple policy inputs \(filter criteria\) that is used to evaluate authentication requests. For example, you can create conditions that allow only contractors from a list of trusted IP addresses.|


