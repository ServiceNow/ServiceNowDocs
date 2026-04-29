---
title: Define a third-party risk domain
description: A risk domain defines the type of risk to assess for a third party. For example, you might want to assess a data-management third party in terms of security risk and a bank in terms of financial risk. Security risk and financial risk are risk domains. Some platform applications refer to risk domains as "risk areas."
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Classic assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Define a third-party risk domain

A risk domain defines the type of risk to assess for a third party. For example, you might want to assess a data-management third party in terms of security risk and a bank in terms of financial risk. Security risk and financial risk are risk domains. Some platform applications refer to risk domains as "risk areas."

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

## About this task

**Note:** Risk domains are called "risk areas" in some platform applications.

You can better understand and mitigate the risks that a third party poses to your organization by identifying the domains of their business to assess for risk and quantifying the importance \(weight\) of each domain.

-   Security risk domain: A third party that handles sensitive personal data in their infrastructure might need to be assessed against their security posture.
-   Reputational risk domain: If that personal data were breached, it could cause damage to your reputation due to negative media attention.
-   Financial risk domain: If a third party fails to deliver on time, you might have to pay fines, settlements, or both resulting in financial loss.

In this procedure, you create a Risk domain definition. In each definition, you specify the criteria that determine which organizations should be assessed for a particular type of risk.

**Note:** Risk domain definitions are called Risk area definitions on the forms.

## Procedure

1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **Scoring Setup** &gt; **Risk Domains**.

    ![Third-party risk area definitions.](../image/vendor-risk-area-def.png)

2.  Select **New**, fill in the form, and then select **Submit**.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the risk domain.

</td></tr><tr><td>

Description

</td><td>

A description of the risk domain that helps colleagues to understand the intent of the definition. See the example.

</td></tr><tr><td>

Default scoring method

</td><td>

The default scoring method for third parties in this risk domain. The scoring methods are based on how well a third-party contact answers 100 questions:-   Average Risk: A rounded average of the ratings earns an Average Risk \(Moderate\) for the third party.
-   Max Risk: A score of 0 indicates that all questions were answered incorrectly and the risk for that third party would be Max Risk \(Critical\).
-   Min Risk: A score of 100 indicates that all questions were answered correctly and the risk for that third party would be Min Risk \(Minor\).
**Note:** Each organization in a particular risk domain inherits the scoring method and weight of the risk area definition. Third-party risk managers can override the values when needed.

</td></tr><tr><td>

Default weight

</td><td>

The default weight for third parties in this risk domain.

</td></tr></tbody>
</table>    ![Third-party risk area definition — new record.](../image/vendor-risk-area-def-new.png)


