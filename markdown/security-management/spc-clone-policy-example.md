---
title: Clone a policy for Security Posture Control \(example\)
description: An example of how to create a policy that copies the conditions from another policy.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Policy examples, Reference, Security Posture Control, Security Operations]
---

# Clone a policy for Security Posture Control \(example\)

An example of how to create a policy that copies the conditions from another policy.

## Before you begin

Create a policy that copies the conditions from the policy you created in Example 2 so you do not have to re-enter them. You will clone these conditions and add more conditions to the copy of the child policy you created. For this example, you want this policy to locate devices with Windows 10 with CrowdStrike, exclude assets with IRM exceptions that have not been seen in the last 7 days.

Roles required: SPC Admin Group or SPC Analyst Group

## Procedure

1.  Navigate to **All** &gt; **Security Posture Control Workspace** &gt; **Policies and findings**.

2.  From the Active list, locate the child policy- Windows devices with CrowdStrike you created for the second example and select it to open the record.

3.  Select the more options menu \(three vertical dots\) and select **Clone policy**.

    A new tab opens and the policy name is displayed in a new record with ‘copy’ in the title: Windows devices with CrowdStrike-copy.

4.  Select the pen icon in the upper left and in the Edit metadata modal fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|Type in, `Cloned policy - Windows 10 CrowdStrike IRM exceptions not seen 7 days.`|
    |**Criticality**|Select **Critical**.|
    |**Short description**|Type in, `Locate devices with Windows 10 with CrowdStrike IRM exceptions not seen last 7 days.`.|

5.  Select **Save Metadata**.

6.  To the right of the first Connection and Entity fields, select the **AND** operator for new fields.

    This adds a logical AND between the current Connection-Entity criteria, and new criteria from another Connection-Entity. In this case, you want to specifcy connector data for assets not seen by CrowdStrike in the last 7 days.

7.  For Connection select **With connector data**.

8.  For Entity, select **CrowdStrike: CrowdStrike Device Details**.

    The criteria filed is automatically filled based on your selection.

9.  For Property select **Last Seen Time**.

10. For Value select **This week**.

11. Select **Save changes**.

12. Select **Activate policy**.

    You can remove these policies at any time from the Policies and Findings module.


