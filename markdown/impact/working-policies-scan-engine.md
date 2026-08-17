---
title: Create policies for Scan Engine
description: Policies let you determine how specific definition findings appear on analytics dashboards; you can ignore them completely or place them in a prioritized view.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/working-policies-scan-engine.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customize Scan Engine definitions, Activate Scan Engine and review settings, Run Impact Guided Setup, Configuring Impact, Impact]
---

# Create policies for Scan Engine

Policies let you determine how specific definition findings appear on analytics dashboards; you can ignore them completely or place them in a prioritized view.

## Before you begin

Role required: admin

You can choose to create policies that label these definition findings as:

-   **Acceptable as is**: Findings remain in the **Open Findings** table but are excluded from dashboard metrics, health score calculations, and prioritization views. They aren't automatically closed.
-   **Prioritize**: Findings will appear in the **Prioritized findings** module on analytics dashboards.

**Note:** Policies match findings based on the **Definition** field. When creating a policy from a finding, the policy automatically references that definition and will apply to all future findings from the same definition.

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Open Findings**.

2.  Select the short description for a finding to open the record to assign a policy.

3.  In the **Related Links** section, select **Create a policy for this finding**.

4.  Set the following fields to configure the policy.

<table id="table_ot3_tqp_zjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated ID for the policy.

</td></tr><tr><td>

Active

</td><td>

Enable the policy to display in the **Finding Policies** page \(**ALL &gt; Impact &gt; Platform Health &gt; Finding Policies**\).

</td></tr><tr><td>

Status

</td><td>

Select one of the following: -   None: The policy is defined but not currently affecting findings
-   Acceptable as is: Exclude findings from metrics
-   Prioritize: Highlight the finding in dashboards


</td></tr><tr><td>

Order

</td><td>

Policies are evaluated in order lowest to highest. The first policy that matches a finding is applied; subsequent policies aren't evaluated for that finding. Lower order values have higher priority.

</td></tr><tr><td>

Reason for policy

</td><td>

Description of why the policy was created.

</td></tr></tbody>
</table>5.  Select **Submit**.

    When a policy is active, findings matching its criteria display its name in their **Policy** field. View all findings affected by a policy through the policy record's **Findings** related list, or navigate to **ALL &gt; Impact &gt; Platform Health &gt; Finding Policies** to manage all policies.


**Parent Topic:**[Customize Scan Engine definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/view-modify-scan-engine-properties.md)

