---
title: Create a policy for the AWS WAF integration for mitigation controls monitoring
description: Create a policy so you can audit your assets based on data imported from the integration.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Exploit protection \(WAF\), Use mitigation controls, Security Posture Control, Security Operations]
---

# Create a policy for the AWS WAF integration for mitigation controls monitoring

Create a policy so you can audit your assets based on data imported from the integration.

## Before you begin

Roles required: SPC Admin Group or SPC Analyst Group

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Posture Control** &gt; **Policies and findings** &gt; **All**.

2.  Select **Hardware Asset** for Asset type.

    Properties also work for Asset search and Asset Profiles.

3.  For Connection select **Security control configuration**.

4.  For Entity select **AWS Insight**.

    A Criteria field is displayed auto-populated with `Connection`.

5.  For the new Connection field select **With AWS managed rule**.

    The Entity field is auto-populated with `Managed Rule` and a Criteria field is displayed auto-populated with `Property`. Blank Property, Operator, and Value fields are displayed.

    If you created a custom AWS rule, select **With custom match statement**. The Entity field is populated with `Match Statement`.

6.  Select properties from the list.

    You can add more than one.

    For example, for a Web ACL for SQL database in your AWS Service Account, you might see the following rules:

    -   SQLiExtendedPatterns\_QUERYARGUMENTS
    -   SQLiQUERYARGUMNETS
    -   SQLi\_BODY
    -   SQLi\_COOKIE
    -   SQLi\_URIPATH
    From the policy builder, this property displays as: SQLRuleSet-SQLi\_BODY is Allow. You can select **Allow** or **Block** from the list.

7.  Select **or** to add properties.

    See [Create and activate custom policies for Security Posture Control](spc-create-policy.md) for more information about using the policy builder to create policies.

8.  Select **Save changes** when you have completed your policy.

9.  **Activate** the policy if you want to view findings.

10. See [View findings for Security Posture Control](spc-view-findings.md) for more information about viewing the findings from your policy.

11. Open a record on the list and select the Mitigation controls Mitigated vulnerable items tabs.

    The Mitigated vulnerable items tab lists all the mitigated vulnerable items that include information about the CVEs that are mitigated as a result of the mitigation rules that are found on your assets.

    -   Verified source\(s\) - AWS APIs, ITOM Discovery
    -   Protected by Web Application Firewall \(WAF\) - Yes
    -   WAF type - AWS
    -   Vulnerable items fully mitigated - number of associated vulnerable items mitigated.
    -   Vulnerable items partially mitigated - number of associated vulnerable items in process.
    -   Managed Rules categorized by actions - Managed Rules with 'Block' and 'Allow' actions.

        You might see more rules than you entered for your policy. These rules are identified with `CommonRuleSet` \(CRS\) in the rule.

    -   Custom Rules - any of your custom rules categorized by 'Block' and 'Allow' actions.
    -   On the Home page dashboard, the Assets with mitigations tile lists the assets that are protected by WAF in the Exploit Protection \(WAF\) visualization.

