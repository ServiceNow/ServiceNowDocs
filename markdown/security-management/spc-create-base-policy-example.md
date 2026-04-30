---
title: Create a base policy for Security Posture Control \(example\)
description: An example of how to create a base policy that you can use to create other policies.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Policy examples, Reference, Security Posture Control, Security Operations]
---

# Create a base policy for Security Posture Control \(example\)

An example of how to create a base policy that you can use to create other policies.

## Before you begin

Roles required: SPC Admin Group or SPC Analyst Group

## Procedure

1.  Navigate to **All** &gt; **Security Posture Control Workspace** &gt; **Policies and findings**.

2.  Select **New policy**.

3.  Select the pen icon in the upper left and in the Edit metadata modal, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|Type in, Base policy - Windows 10 devices.|
    |**Criticality**|Select **Low**.|
    |**Short description**|Type in, **Locate devices with Windows 10 installed**.|

4.  Select **Save metadata**.

5.  In the Condition builder select **Hardware Asset** for Asset type.

    For this policy, leave the Base policy and Exclusion policies options in their default \(off\) settings.

6.  For Connection select **With aggregated data**.

    For this policy, aggregated data helps you the locate assets in your CMDB that have Windows 10 installed. For example, some records might have slight variations on how different scanners report 'Windows 10'. Aggregated data ensures that all these slight variations on ‘Windows 10’ will match this policy.

    The Entity and Criteria fields are filled in automatically based on your selection in the Connection field.

7.  For Property select **OS**.

8.  For Value type in `Windows 10`.

9.  Select **Save changes**.

    Your base policy is displayed on the All list of the Policies and findings module but it is not activated.

10. Select **Activate policy** so your base policy monitors any assets that match the policy's conditions and generates findings.


