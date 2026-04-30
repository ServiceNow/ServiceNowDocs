---
title: Publisher optimizations for Microsoft
description: View licensing optimizations for Microsoft by selecting Microsoft from the Publisher drop-down list.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Publisher optimizations for Microsoft

View licensing optimizations for Microsoft by selecting **Microsoft** from the **Publisher** drop-down list.

<table id="table_vcq_xwt_2xb"><thead><tr><th>

Report

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Microsoft 365 subscription details**Note:** This report appears only if you request and install the Software Asset Management - SaaS License Management application.

</td><td>

-   Active and inactive subscriptions: Software Subscriptions \[samp\_sw\_subscription\]
-   Unassigned subscriptions: Purchased Subscription Details \[samp\_purchased\_subscription\_details\]

</td><td>

Number of active, inactive, and unassigned user subscription details for Microsoft 365, Office 365, and Power BI products, which are grouped by software models.

 Select a data point to view more details about the user subscriptions for a software model.

-   Select the **Active subscriptions** bar to view the active user subscriptions, where the last activity date is equal to or less than 90 days.
-   Select the **Inactive subscriptions** bar to view the inactive subscriptions, where the last activity date is empty or was before 90 days.
-   Select the **Unassigned subscriptions** bar to view the number of available rights or user subscriptions that are unassigned.

</td></tr><tr><td>

Microsoft 365 potential savings by type**Note:** This report appears only if you request and install the Software Asset Management - SaaS License Management application.

</td><td>

Removal Candidate\[samp\_sw\_reclamation\_candidate\]

</td><td>

Potential monthly savings for your Microsoft 365 and Office 365 licenses that are based on recommended downgrade, double license, and consolidate candidates. This report displays potential savings for the last 12 months.

Select any bar to view more details about the recommended downgrade or dual license candidates for a given month.-   Select the **Downgrades** bar to view the list of candidates that can be downgraded to a previous version of Microsoft 365 and Office 365.
-   Select the **Double Licensed Users** bar to view the list of candidates with both Microsoft 365 and its applications \(Office 365, Enterprise Mobility+Security \(EMS\), Windows\) subscriptions.
-   Select the **Consolidate** bar to view the list of Microsoft 365 consolidate subscriptions reclamation candidates.

</td></tr><tr><td>

Microsoft 365 optimization recommendations**Note:** This report appears only if you request and install the Software Asset Management - SaaS License Management application.

</td><td>

Removal Candidate\[samp\_sw\_reclamation\_candidate\]

</td><td>

Number of licenses per month that can be downgraded or reclaimed based on recommended downgrade, dual license candidates. This report displays data for the last 12 months.

Select any bar to view more details and act on the recommended downgrade, double licensed, or consolidate candidates for a given month.-   Select the **Downgrades from Office 365 E5 to E3** bar to view the list of candidates that can be downgraded from Office 365 E5 to Office 365 E3. Select a candidate from the list to downgrade the associated license.
-   Select the **Downgrades from Office 365 E3 to E1** bar to view the list of candidates that can be downgraded from Office 365 E3 to Office 365 E1. Select a candidate from the list to downgrade the associated license.
-   Select the **Downgrades from Microsoft 365 E5 to E3** bar to view the list of candidates that can be downgraded from Microsoft 365 E5 to Microsoft 365 E3.
-   Select the**Downgrades from Microsoft 365 E3 to F3** bar to view the list of candidates that can be downgraded from Microsoft 365 E3 to Microsoft 365 F3.
-   Select the **Consolidate** bar to view the list of consolidated Microsoft 365 optimization candidates.

</td></tr><tr><td>

On-Premises potential savings by optimizing licenses

</td><td>

Potential Savings by Optimizing Licenses\[samp\_license\_optimization\_summary\]

</td><td>

Potential cost savings for licenses on your physical hosts and clusters based on recommended licensing optimizations.**Note:** This report is available only for the following Microsoft license types:

-   Per core licenses for Microsoft SQL Server and Microsoft BizTalk Server
-   Per core \(with CAL\) licenses for Microsoft Windows Server, Microsoft Core Infrastructure Server, and Microsoft System Center

Select the report to view details about the recommended licensing optimizations and associated cost savings for each host or cluster. Licensing optimizations include the recommended license, recommended rights, and recommended spending.

</td></tr><tr><td>

On-Premise optimization realized savings

</td><td>

Microsoft Core License Optimization Reports\[samp\_ms\_optimization\_report\]

</td><td>

Cost savings that you have achieved for licenses on your physical hosts and clusters based on recommended licensing optimizations.**Note:** This report is available only for the following Microsoft license types:

-   Per core licenses for Microsoft SQL Server and Microsoft BizTalk Server
-   Per core \(with CAL\) licenses for Microsoft Windows Server, Microsoft Core Infrastructure Server, and Microsoft System Center

Select the report to view details about the cost savings that you have achieved for each host or cluster.

</td></tr><tr><td>

Microsoft 365 portal available subscription details**Note:** This report appears only if you request and install the Software Asset Management - SaaS License Management application.

</td><td>

Purchased Subscription Details\[samp\_purchased\_subscription\_details\]

</td><td>

Number of licenses that are available on the Microsoft portal per subscription.Select a bar to view details about the purchased subscription details such as software model, product, purchased rights, assigned rights, available rights, and subscription profile.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

**Related topics**  


[Reclamation rules for Microsoft 365 integration](m365-reclamation-rules.md)

