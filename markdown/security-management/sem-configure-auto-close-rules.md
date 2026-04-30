---
title: Configuring auto-close rules
description: By configuring auto-close rules, you can automate the process of closing stale detections and findings associated with retired configuration items \(CIs\).Create rules to close stale detections and findings associated with retired CIs automatically.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Configuring auto-close rules

By configuring auto-close rules, you can automate the process of closing stale detections and findings associated with retired configuration items \(CIs\).

The base system provides the following auto-close rules:

-   **Assets last scanned**: Detections associated with assets that haven’t been scanned within the last 90 days are transitioned to Stale state.
-   **Detections last found**: Detections that haven’t been found within the last 90 days. If you activate Detections last found record, then this feature requires a successful integration run of Rapid7 Comprehensive Vulnerable Item Integrations and Microsoft TVM Machine Vulnerabilities Integration \(Full import\) within the last seven days.

Configuration of auto-delete rules includes the following steps.

**Related topics**  


[Closing stale detections and findings automatically using auto-close rules](sem-closing-stale-findings-automatically.md)

## Create or edit auto-close rules

Create rules to close stale detections and findings associated with retired CIs automatically.

### Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](sem-acls-for-admin-rules.md)

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Auto-close rules** tile.

4.  On the Rules page, select **Auto-close** in the navigation pane.

5.  Select **New** and fill in the fields on the form:

<table id="table_vks_thr_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Details

</td></tr><tr><td>

Name

</td><td>

Name of the rule.

</td></tr><tr><td>

Table

</td><td>

Name of the finding type for which the rule is being applied.**Note:** For vulnerable items \(VITs\), rules are applied to detections first, and then applied to the VITs, rather than being directly applied to the VITs.

</td></tr><tr><td>

Description

</td><td>

Description of the rule.

</td></tr><tr><td>

Active

</td><td>

Indicates whether the rule is active.

</td></tr><tr><td colspan="2">

If this condition is met

</td></tr><tr><td>

Condition fields

</td><td>

Filter conditions defining the records in the Findings and Remediation Task tables to which the rules apply.

</td></tr><tr><td>

New condition set

</td><td>

Adds more condition filter fields to choose from.

</td></tr><tr><td colspan="2">

Then do this

</td></tr><tr><td>

Close findings automatically

</td><td>

 

</td></tr><tr><td>

Ignored deferred items

</td><td>

If selected, any findings or detections that are mapped to the **In-review** or **Deferred** states are ignored and not closed. If you clear this option, any findings or detections that match your criteria are closed.

</td></tr></tbody>
</table>6.  Select **Save**.

    The **Auto-Close Stale Detections** scheduled job runs daily. It identifies detections based on the specified conditions and transitions the matching ones to the **Stale** state.

    The job handles the following scenarios:

    -   If all the detections within a VIT are marked as stale, the VIT is closed with the sub-state set as "Stale".
    -   If there is at least one detection that remains open within a VIT, while others are in the Stale status, the VIT remains open.
    -   In cases where there are detections with both "Closed" and "Stale" statuses within a VIT, the VIT is closed with the sub-state set as "Fixed".
    When you upgrade to the latest version of Unified Security Exposure Management, the conditions set in your auto-close rules also get updated accordingly. Additionally, if the rules are associated with different domains, the rules are created specifically within those domains.


