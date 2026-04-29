---
title: Create policies for Scan Engine
description: Policies let you determine how specific definition findings appear on analytics dashboards; you can ignore them completely or place them in a prioritized view.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Scan Engine, Platform Health, Using Impact, Impact]
---

# Create policies for Scan Engine

Policies let you determine how specific definition findings appear on analytics dashboards; you can ignore them completely or place them in a prioritized view.

## Before you begin

Role required: admin

You can choose to create policies that label these definition findings as:

-   **Acceptable as is**: Findings remain in the **Open Findings** table but are excluded from dashboard metrics, health score calculations, and prioritization views. They are not automatically closed.
-   **Prioritize**: Findings will appear in the **Prioritized findings** module on analytics dashboards.

**Note:** Policies match findings based on the **Definition** field. When creating a policy from a finding, the policy automatically references that definition and will apply to all future findings from the same definition.

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Open Findings**.

2.  To open the record of a finding that you want to assign a policy to, select its short description.

3.  In the **Related Links** section, select **Create a policy for this finding**.

4.  Set the following fields to configure the policy.

<table id="choicetable_npc_csk_hhc"><tbody><tr><td id="d43172e123">

**Number**

</td><td>

Auto-generated ID for the policy.

</td></tr><tr><td id="d43172e132">

**Active**

</td><td>

Enable the policy to display in the **Finding Policies** page \(**ALL &gt; Impact &gt; Platform Health &gt; Finding Policies**\).

</td></tr><tr><td id="d43172e150">

**Status**

</td><td>

Select one of the following: -   None
-   Acceptable as is
-   Prioritize
**Note:** **None** means the policy is defined but not currently affecting findings. Use **Acceptable as is** to exclude findings from metrics, or **Prioritize** to highlight them in dashboards. Inactive policies do not process at all.

</td></tr><tr><td id="d43172e180">

**Order**

</td><td>

Policies are evaluated in order \(lowest to highest\). The first policy that matches a finding is applied; subsequent policies are not evaluated for that finding. Lower order values have higher priority.

</td></tr><tr><td id="d43172e189">

**Reason for policy**

</td><td>

Description of why the policy was created.

</td></tr></tbody>
</table>5.  Select **Submit**.

    When a policy is active, findings matching its criteria display its name in their **Policy** field. View all findings affected by a policy through the policy record's **Findings** related list, or navigate to **ALL &gt; Impact &gt; Platform Health &gt; Finding Policies** to manage all policies.


