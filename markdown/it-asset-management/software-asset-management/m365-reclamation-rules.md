---
title: Reclamation rules for Microsoft 365 integration
description: Reclamation rules for Microsoft 365 integration sets the minimum usage threshold for a subscription. If a subscription remains inactive for a specified period, Software Asset Management marks the subscription as a potential reclamation candidate.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Reclamation rules for Microsoft 365 integration

Reclamation rules for Microsoft 365 integration sets the minimum usage threshold for a subscription. If a subscription remains inactive for a specified period, Software Asset Management marks the subscription as a potential reclamation candidate.

<table id="table_el3_1wh_ddc"><thead><tr><th>

Reclamation rule

</th><th>

Justification

</th><th>

Description

</th></tr></thead><tbody><tr><td>

-   Power BI
-   Exchange Online
-   SharePoint Online
-   OneDrive for Business
-   Teams
-   Project Online
-   Visio Online
-   Microsoft 365 Copilot

</td><td>

Low Usage

</td><td>

If these individual subscriptions show low usage, Software Asset Management recommends reclaiming the low usage subscriptions.

</td></tr><tr><td>

Microsoft 365

</td><td>

-   Low Usage

**Note:** Only downgrade use cases related to Microsoft 365 and Office 365 are supported for low usage justification.

-   Dual license
-   Consolidate Subscriptions

**Note:** The Dual license and Consolidate Subscriptions use cases are applicable to all Microsoft 365 and its applications \(Office 365, Enterprise Mobility+Security \(EMS\), Windows\).


</td><td>

-   **Low usage**

For example, if a Microsoft 365 E5 subscription including advanced features and capabilities with Power BI isn't being used, Software Asset Management recommends switching to a downgraded Microsoft 365 E3 subscription.

-   **Dual license**

For example, both Microsoft 365 E3 and Office 365 E3 subscriptions exist, leading to unnecessary duplicate access to Office applications and additional services already included in Microsoft 365 E3. Software Asset Management recommends reclaiming the Office 365 E3 subscriptions and using the Microsoft 365 E3 subscriptions instead.

-   **Consolidate Subscriptions**

For example, if Office 365 Enterprise E5, Windows, and EMS subscriptions exist, Software Asset Management recommends using a single license such as Microsoft 365 Enterprise E5 to cover these multiple products at a lower cost.


</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

**Related topics**  


[Review a software reclamation rule](../task/add-reclamation-rule-sub.md)

[Evaluating software usage activity for Microsoft 365 subscriptions](../concept/integrate-with-microsoft.md#)

[Publisher optimizations for Microsoft](pub-opt-microsoft.md)

[Integrating with Microsoft 365](../concept/integrate-with-microsoft.md#)

