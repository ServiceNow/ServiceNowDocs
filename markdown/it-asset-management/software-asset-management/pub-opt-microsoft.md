---
title: Publisher optimizations for Microsoft
description: View licensing optimizations for Microsoft by selecting Microsoft from the Publisher drop-down list.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [References, Software Asset Management, IT Asset Management]
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

Number of active, inactive, and unassigned user subscription details for Microsoft 365 products, which are grouped by software models.

 Select a data point to view more details about the user subscriptions for a software model.

-   Select the **Active subscriptions** bar to view the active user subscriptions, where the last activity date is equal to or less than 90 days.
-   Select the **Inactive subscriptions** bar to view the inactive subscriptions, where the last activity date is empty or was before 90 days.
-   Select the **Unassigned subscriptions** bar to view the number of available rights or user subscriptions that are unassigned.

</td></tr><tr><td>

Microsoft 365 subscription assignment details

</td><td>

Software Subscriptions \[samp\_sw\_subscription\]

</td><td>

Number of assigned Microsoft 365 subscriptions. This report displays assigned subscriptions for the last six months.Select a data point to view the details of the assigned subscription such as Publisher, Product, User, User principal name, Software model, and Subscription profile.

</td></tr><tr><td>

Microsoft 365 potential savings by type**Note:** This report appears only if you request and install the Software Asset Management - SaaS License Management application.

</td><td>

Removal Candidate\[samp\_sw\_reclamation\_candidate\]

</td><td>

Potential monthly savings for your Microsoft 365 licenses that are based on recommended downgrade, overlapping, consolidate, and low usage candidates. This report displays potential savings for the last six months.

Select any bar to view more details about the recommended downgrade or dual license candidates for a given month.-   Select the **Low Usage** bar to view the list of Microsoft 365 low usage reclamation candidates. Select a candidate to view the details, software installations, subscriptions to reclaim, and subscriptions to assign.
-   Select the **Downgrade** bar to view the list of candidates that can be downgraded to a previous version of Microsoft 365 and Office 365. Select a candidate to view the details, software installations, subscriptions to reclaim, and subscriptions to assign.
-   Select the **Overlapping** bar to view the list of Microsoft 365 overlapping reclamation candidates. Select a candidate to view the details, subscriptions to reclaim, and subscriptions to assign.
-   Select the **Consolidate** bar to view the list of Microsoft 365 consolidate subscriptions reclamation candidates. Select a candidate to view the details, subscriptions to reclaim, and subscriptions to assign.

</td></tr><tr><td>

Microsoft 365 optimization recommendations**Note:** This report appears only if you request and install the Software Asset Management - SaaS License Management application.

</td><td>

Removal Candidate\[samp\_sw\_reclamation\_candidate\]

</td><td>

Number of licenses per month that can be downgraded or reclaimed based on recommended downgrade, overlapping, consolidate, and low usage candidates. This report displays data for the last six months.

 -   Select the **Low Usage** bar to view the list of Microsoft 365 candidates that can be reclaimed based on low usage.
-   **Downgrade**: Select the Downgrade bar to view the list of Microsoft 365 and Office 365 candidates that can be downgraded. Select a candidate from the list to downgrade the associated license.
-   **Overlapping**: Select the Overlapping bar to view the list of Microsoft 365 overlapping reclamation candidates. Select a candidate from the list to reclaim the associated license.
-   **Consolidate**: Select the Consolidate bar to view the list of consolidated Microsoft 365 optimization candidates. Select a candidate from the list to reclaim the associated license.

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

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

**Related topics**  


[Evaluating software usage activity for Microsoft 365 subscriptions](../concept/o365-usage-activity.md)

[Reclamation rules for Microsoft 365 integration](m365-reclamation-rules.md)

[Microsoft 365 integration](../concept/microsoft-o365.md)

