---
title: Create a child policy from a base policy for Security Posture Control \(example\)
description: An example of how to create a child policy using the conditions of a base policy.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Policy examples, Reference, Security Posture Control, Security Operations]
---

# Create a child policy from a base policy for Security Posture Control \(example\)

An example of how to create a child policy using the conditions of a base policy.

## Before you begin

This child policy inherits the conditions of a base policy, and you will add more conditions to your child policy to help you focus on more specific asset details. You want a new policy to monitor all your devices that have Windows 10 installed that are reported by the CrowdStrike service graph connector, and you want to exclude any devices that match another policy. For this example, you will exclude assets that have been approved for Integrated Risk Management \(IRM\) exceptions from your findings.

**Note:** If you do not have the CrowdStrike service graph connector installed, you can use one that have installed.

Roles required: SPC Admin Group or SPC Analyst Group

## Procedure

1.  Navigate to **All** &gt; **Security Posture Control Workspace** &gt; **Policies and findings**.

2.  From the Active list, locate the Base policy - Windows 10 devices you created in the first example and select it to open the record.

3.  Select the more options menu \(three vertical dots\) and select **Create child policy**.

    A new tab opens and with a new record and the Base policy - Windows 10 devices is displayed in the Base policy field.

4.  Select the pen icon in the upper left and in the Edit metadata modal fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|Type in, `Child policy- Windows devices with CrowdStrike`.|
    |**Criticality**|Select **Medium**.|
    |**Short description**|Type in, `Locate all devices with Windows 10 reported by CrowdStrike.`|

5.  Select **Save metadata**.

6.  In the Condition builder select **Hardware Asset** for Asset type.

7.  Select the Base policy toggle.

8.  Select the policy you created for Example 1, **Base policy - Windows 10 devices** from the list.

    This child policy automatically inherits the conditions of the base policy.

9.  Select the Exclusion policies toggle.

10. Select Assets with IRM exception approved from the list.

    **Note:** If you don't have this policy, you can select another policy from the list that you want to exclude from this policy.

    The assets that match this policy will be excluded from your child policy. Note that you can add more polices.

11. Select **Reported by**.

12. Select **CrowdStrike** from the list.

13. Select **Save changes**.

    Your new policy is displayed on the All list of the Policies and findings module but it is not activated.

14. Select **Activate policy** so your base policy monitors any assets that match the policy's conditions and generates findings.


