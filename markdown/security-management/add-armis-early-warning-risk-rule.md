---
title: Add Early Warning criteria to a risk rule
description: Add the Early Warning flag or Admiralty score as a weighted criterion in a risk rule to prioritize vulnerable items based on vulnerability intelligence data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/add-armis-early-warning-risk-rule.html
release: zurich
topic_type: task
last_updated: "2026-07-09"
reading_time_minutes: 2
keywords: [Armis Early Warning, risk rule, risk scoring criteria, Default Risk Calculator]
breadcrumb: [Early Warning for Security Exposure Management, Integrations, Unified Security Exposure Management, Security Operations]
---

# Add Early Warning criteria to a risk rule

Add the Early Warning flag or Admiralty score as a weighted criterion in a risk rule to prioritize vulnerable items based on vulnerability intelligence data.

## Before you begin

The Early Warning for Security Exposure Management plugin must be installed and at least one integration run must have completed so that Early Warning fields are available in the risk rule criteria builder.

Role required: sn\_sec\_calculator.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  In the navigation pane, select **Administration**.

3.  Under the **Configurations** section, locate **Risk calculators** tile.

4.  Select **Review** to open the Risk calculator page.

5.  Open the risk rule to which to add the criterion, such as **Default Risk Rule**.

    The risk rule form opens showing the existing criteria, condition logic, and the **Criteria** section where you add new scoring inputs.

6.  In the **Criteria** section, select **+ New criteria**.

    A new criteria row expands with fields for Reference table, Table, Field, and Weightage %.

7.  In the **Reference table** field, select **Vulnerable Item --&gt; Vulnerability**.

8.  In the **Table** field, select **National Vulnerability Database Entry**.

9.  In the **Field** dropdown, type `armis` to filter the field list, then select the desired Armis Early Warning field.

    Available Armis Early Warning fields include the early warning flag and the admiralty score. To apply a weight based solely on whether early warning is enabled, select the early warning flag field. To incorporate confidence level, select the admiralty score field and configure it as an additional condition.

10. In the **Weightage %** field, enter the percentage weight to assign to this criterion.

11. Select **Update** to save the new criterion.


## What to do next

To preview how the updated risk rule scores existing vulnerable items, select **Preview** in the Criteria section before saving the rule.

**Parent Topic:**[Early Warning for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/armis-early-warning-integration.md)

**Related topics**  


[Define fields and weights for the risk rule for Unified Security Exposure Management risk calculators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-vuln-calc-define-risk-rule-fields.md)

