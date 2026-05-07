---
title: Set term multiplier for contract renewal uplift
description: Use the renewal\_uplift\_term system property to select the contract duration basis used to calculate the renewal uplift term, either per year or per term.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Blended pricing for contract consolidation of subscription renewals, Product pricing, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set term multiplier for contract renewal uplift

Use the **renewal\_uplift\_term** system property to select the contract duration basis used to calculate the renewal uplift term, either per year or per term.

## Before you begin

Role required: admin or pricing admin

## Procedure

1.  Navigate to **All** and in the filter enter `sys_properties.list`.

2.  Open the **renewal\_uplift\_term** system property.

    The default value is per term, which means the term is for a specific period of time based on the contract.

3.  Do one of the following in the **Value** field:

    -   To use a yearly basis for the uplift term multiplier, enter `per year` in the **Value** field.
    -   To change the uplift term multiplier to per term, enter `per term` in the **Value** field.
4.  Select **Update**.

    Uplift calculations use the specified multiplier to calculate the contract duration basis.


