---
title: Optimization and savings dashboard in workspace
description: Use the Optimization and savings dashboard to view actual and potential cost savings for your software assets. In addition, view the recommended licensing optimizations for third-party software publishers, including Microsoft, Red Hat, and SAP. Use this information to downgrade or reclaim licenses so that you can optimize your licensing costs.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Software asset analytics view, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Optimization and savings dashboard in workspace

Use the Optimization and savings dashboard to view actual and potential cost savings for your software assets. In addition, view the recommended licensing optimizations for third-party software publishers, including Microsoft, Red Hat, and SAP. Use this information to downgrade or reclaim licenses so that you can optimize your licensing costs.

**Note:** You can use the Domain filter to narrow your results based on the domain that you select. The default value for the Domain filter is **global**. You can select a domain at any given time for widgets to reflect the selected domain. If you clear the selected domain, it defaults back to **global**.

The Domain filter appears on the screen only if the following plugins are installed:

-   Domain Support - Domain Extensions Installer \(com.glide.domain.msp\_extensions.installer\)
-   Performance Analytics - Domain Support \(com.snc.pa.domain\_support\)

You can access the Optimization and savings dashboard by navigating to **Software asset** &gt; **Software Asset Workspace** &gt; **Software asset analytics** &gt; **Optimization and savings**.

View the licensing optimizations for a publisher by selecting the publisher from the **Publisher** drop-down list.

-   [Publisher optimizations for SAP](pub-opt-sap.md)
-   [Publisher optimizations for Red Hat](pub-opt-redhat.md)
-   [Publisher optimizations for Microsoft](pub-opt-microsoft.md)
-   [Publisher optimizations for Adobe](pub-opt-adobe.md)

![Optimization and savings dashboard in Software Asset Workspace.](../image/optimizations-savings-dboard.png "Optimization and savings dashboard")

<table id="table_xvt_zjm_qpb"><thead><tr><th>

Report

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total actual savings YTD

</td><td>

Removal Candidate \[samp\_sw\_reclamation\_candidate\]

</td><td>

State is Closed Complete and closed on this year.

</td></tr><tr><td>

Cumulative actual savings

</td><td>

Removal Candidate \[samp\_sw\_reclamation\_candidate\]

</td><td>

State is Closed Complete and the sum of potential savings.

</td></tr><tr><td>

Potential savings

</td><td>

Removal Candidate \[samp\_sw\_reclamation\_candidate\]

</td><td>

State is NOT closed complete OR closed canceled OR closed skipped and the sum of potential savings.

</td></tr><tr><td>

Reclamation

</td><td>

Removal Candidate \[samp\_sw\_reclamation\_candidate\]

</td><td>

Active is true.

</td></tr><tr><td>

Actual Savings

</td><td>

Removal Candidate \[samp\_sw\_reclamation\_candidate\]

</td><td>

Five months of history of closed complete reclamation candidates and their corresponding savings.

</td></tr><tr><td>

Total spend vs. potential savings top 10 publishers

</td><td>

Product Result \[samp\_product\_result\] and Removal Candidate \[samp\_sw\_reclamation\_candidate\]

</td><td>

History of top 10 publishers sorted by highest spend and their corresponding potential savings.

</td></tr></tbody>
</table>