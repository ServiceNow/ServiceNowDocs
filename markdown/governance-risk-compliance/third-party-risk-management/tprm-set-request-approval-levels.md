---
title: Set up the approval levels for due diligence requests
description: Assign one or more approval levels to the users or groups that approve your due diligence requests in the Third-party Risk Management application. Because the approval levels are applied iteratively and each level contains different rules, you can help to ensure that the correct user or group is assigned as an approver.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Approve or reject due diligence requests, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Set up the approval levels for due diligence requests

Assign one or more approval levels to the users or groups that approve your due diligence requests in the Third-party Risk Management application. Because the approval levels are applied iteratively and each level contains different rules, you can help to ensure that the correct user or group is assigned as an approver.

## Before you begin

Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_admin

## Procedure

1.  Navigate to **All** &gt; **Approval Configurator** &gt; **Approval Configurations**.

2.  Select **Third-party due diligence default configuration**.

3.  Create an approval level by selecting **New**.

    A **Third-party due diligence default level** is included as part of the base system.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the approval level.|
    |Level|Stage of approval.|

    **Note:** In an approval configuration, you can’t have multiple approval levels with the same level number. The rules of each level are applied sequentially, one after the other.

5.  Select **Submit**.

    For information on setting up rules to assign to levels, see [Set up the approval rules for due diligence requests](tprm-set-request-approval-rules.md).

    For more information on approval levels and rules, see [Approving or rejecting requests for due diligence](../../grc-vendor-risk/concept/tprm-approving.md).


**Related topics**  


[Set up the approval rules for due diligence requests](tprm-set-request-approval-rules.md)

