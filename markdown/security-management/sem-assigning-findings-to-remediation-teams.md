---
title: Assigning findings to remediation teams using assignment rules
description: Assignment rules automatically assign findings, such as vulnerable items, application vulnerabilities, container vulnerabilities, and configuration test results, to the appropriate groups for remediation. This streamlined triage ensures that tasks are directed to the appropriate teams, and enhances consistency and visibility across security and compliance programs.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-31"
reading_time_minutes: 5
keywords: [assign findings to remediation teams automatically, assign vulnerable items to remediation teams automatically, assign application vulnerable items to remediation teams automatically, assign container vulnerable items to remediation teams automatically, assignment rules overview]
breadcrumb: [Automating prioritization and triaging, Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Assigning findings to remediation teams using assignment rules

Assignment rules automatically assign findings, such as vulnerable items, application vulnerabilities, container vulnerabilities, and configuration test results, to the appropriate groups for remediation. This streamlined triage ensures that tasks are directed to the appropriate teams, and enhances consistency and visibility across security and compliance programs.

In the Security Exposure Management Workspace, you can set up a single assignment rule that applies to all types of findings, including vulnerable items \(VITs\), application vulnerabilities \(AVITs\), container vulnerabilities \(CVITs\), and configuration test results \(CTRs\). This rule can then be applied to all the findings or a specific combination of findings.

Assignment rules apply when findings are:

-   Created \(imported or manually\)
-   Reopened
-   Modified \(if rules are manually reapplied\)

## Assigning vulnerable items automatically

There are three different ways to assign findings using:

-   User Group: Assign findings directly to a selected user group.
-   User Group Field: Assign any assignment group field available using the cmdb\_ci table. Assign based on the assignment group field available using the cmdb\_ci table.
-   Script: Use a script to define assignment conditions. This option requires coding or advanced ServiceNow® expertise. For more information on how to use the script editor to define complex conditions, see the [KB0965240](https://support.servicenow.com/kb?id=kb_article_view_popup&sysparm_article=KB0965240) KB article.

    **Note:** The options for assigning rules using the User group and User group field gets updated based on the tables selected in the **Applies to** field.


## Assignment rule evaluation process

When a new or reopened finding is processed, the system evaluates assignment rules in the following order:

1.  Ascending order: Rules are processed starting with the lowest execution order.
2.  First match: The system applies the first rule that matches the finding.
3.  Default group: If no rule matches, the finding is assigned to a default group \(if a default rule is configured\).
4.  Unassigned: If no default rule exists, the finding remains unassigned.

Assigned groups are then used by remediation task rules to determine task ownership and grouping.

**Note:**

-   The default rule should have the highest execution order value to act as a fallback or catch-all.
-   Manually assigned findings aren’t reevaluated by assignment rules.

## Execution order recommendation

You may use the following order to run the rules:

1.  High priority rules: Run these rules first for items that require special handling, where the risk is critical, or where findings must be addressed for regulatory compliance.
2.  General rules: Run these rules next for items that do not require special handling and where you have a clear understanding of the responsible parties.
3.  Default rules: Finally, create a default rule to assign findings to a group that determines the appropriate assignment group. This group can then add additional rules based on their decisions. The default rule should run last.

In the Security Exposure Management Workspace, you can set the execution order of the assignment rules by simply dragging and dropping them to reorder on the Rules list page.

## Applying assignment rules

Assignment rules are applied to the findings using:

-   A scheduled job: The **Run assignment rules** job runs daily to apply the assignment rules on the findings. It’s inactive by default. You can configure it to run on a set schedule \(daily, weekly, monthly, on demand, and so on\) based on the scale of your environment. Depending on how many active findings you have in your environment, remember to set the **Run** field appropriately following the initial run to avoid performance impacts. This job applies to all open findings, excluding those that have been manually assigned.
-   The Reapply button: Use the **Reapply** button to reapply updated rules to all open findings. Manually assigned findings are excluded from this process.
-   A business rule: The business rule **Link to Remediation Tasks** on the Findings table evaluates all the assignment rules and applies them to the newly created or modified findings. To enable the business rule:
    1.  Navigate to **System Definition** &gt; **Business Rules**.
    2.  Enable **Link to Remediation Tasks** business rule.
    3.  Select the **Active** check box to activate the business rule.

**Note:** When enabled:

-   Findings are automatically regrouped under a relevant remediation task or group. If they can't be grouped under an existing group, a new group is created.
-   Manual changes don’t trigger regrouping—only rule-driven updates do.
-   Remediation tasks themselves aren’t deleted. Only findings are removed or regrouped.

When rules are updated, reapplying them ensures that current findings reflect the new logic.

## Automating regrouping after assignment group changes

You can automate the regrouping of findings when assignment groups change due to assignment rule reapplication by activating the **sn\_sec\_rem.rerun\_task\_rules** system property.

**Note:** This system property is not activated by default.

Steps to enable:

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.
2.  Open the **sn\_sec\_rem.rerun\_task\_rules** system property.
3.  In the **Value** field, set the value to true.

When enabled, findings are unlinked from prior remediation tasks if the rule conditions no longer match.

## Assignment impact on remediation tasks

Assignment rules also influence how findings are grouped and managed in remediation tasks. Remediation task rules inherit assignment groups from findings. For example, if findings across multiple CIs are assigned to different groups, remediation tasks may be split accordingly.

If the assignment group of a remediation task is updated:

-   All findings within that task, sharing original assignment group, are also updated.
-   These findings are marked as manually assigned and excluded from further automatic rule evaluation.

## Special considerations by finding type

|Finding type|Notes|
|------------|-----|
|Vulnerable items \(VITs\)|Base system includes an **Assign to CI Support Group** rule. Use order to prioritize critical, general, and fallback rules.|
|Container vulnerable Items \(CVITs\)|Only one matching rule applies. Rules ignore non-Open or manually assigned CVITs.|
|Configuration Test Results \(CTRs\)|Uses similar logic. Default assignment rule is inactive. Terminology changes as of v14.9 \(for example, "Group Rules" → "Remediation Task Rules"\).|

-   **[Removing assignments from findings and remediation tasks](sem-unassigning-findings.md)**  
You can remove yourself or your group from the **Assigned to** and **Assignment group** fields on findings and remediation tasks if you believe they were incorrectly assigned.

**Parent Topic:**[Automating prioritization and triaging](sem-automating-prioritization-triaging.md)

**Related topics**  


[Configuring assignment rules](sem-configure-assignment-rules.md#)

