---
title: SaaS overview dashboard in workspace
description: View all SaaS related analytics for pure SaaS, Microsoft Office 365, and Adobe Cloud in the SaaS overview dashboard in the Software asset analytics view.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Software asset analytics view, Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# SaaS overview dashboard in workspace

View all SaaS related analytics for pure SaaS, Microsoft Office 365, and Adobe Cloud in the SaaS overview dashboard in the Software asset analytics view.

Optimize your organization's cost on SaaS by analyzing the subscription usage, cost, and compliance for your SaaS applications on the SaaS overview dashboard. You can also view compliance analysis results related to Microsoft Office 365 and Adobe Cloud.

**Note:** The SaaS overview dashboard is only visible if you activate the Software Asset Management - SaaS License Management plugin from ServiceNow Store.

You can filter the dashboard by instance, publisher, software model, or domain. Select any report to see more information.

**Note:** The Domain filter narrows your results based on the domain that you select. The default value for the domain filter is global. You can select a domain at any given time for widgets to reflect the selected domain. After you clear the selected domain, it defaults back to global. The Domain filter appears on the screen only if the following plugins are installed:

-   Domain Support - Domain Extensions Installer \(com.glide.domain.msp\_extensions.installer\)
-   Performance Analytics - Domain Support \(com.snc.pa.domain\_support\)

You can access the SaaS overview dashboard by navigating to **Workspaces** &gt; **Software Asset Workspace** &gt; **Software asset analytics**.

![SaaS Overview dashboard in workspace](../image/software-analytics-workspace.png "SaaS overview dashboard")

<table id="table_lvv_rrb_dpb"><thead><tr><th>

Report

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total spend

</td><td>

License Metric Results \[samp\_license\_metric\_result\]

</td><td>

Total cost of all active subscription software entitlements.

</td></tr><tr><td>

Potential savings

</td><td>

Removal Candidate \[samp\_sw\_reclamation\_candidate\]

</td><td>

Potential costs saved if you reclaim unused subscriptions.

</td></tr><tr><td>

Actual savings to date

</td><td>

Removal Candidate \[samp\_sw\_reclamation\_candidate\]

</td><td>

Total yearly savings for all subscription software. This value is calculated as the total savings from closed complete reclamation candidates.

</td></tr><tr><td>

True-up cost

</td><td>

License Metric Results \[samp\_license\_metric\_result\]

</td><td>

Cost to have the number of rights you own match the number of rights you’ve assigned to users. This metric helps to verify that your organization is paying for all the rights that your organization is using.

</td></tr><tr><td>

Over-licensed amount

</td><td>

License Metric Results \[samp\_license\_metric\_result\]

</td><td>

Cost of licenses owned but not being used.

</td></tr><tr><td>

Total number of products

</td><td>

Software Subscription \[samp\_sw\_subscription\]

</td><td>

Total number of products, including products automatically detected from imported financial transactions and products manually added to transactions.

</td></tr><tr><td>

User summary Subscriptions Owned

</td><td>

Software Entitlement\[alm\_license\]

</td><td>

All active entitlements with the license type as subscription.

</td></tr><tr><td>

User summary Subscriptions Assigned

</td><td>

Software Subscription\[samp\_sw\_subscription\]

</td><td>

Total number of assigned rights for SaaS software models.

</td></tr><tr><td>

User Summary Stale subscriptions

</td><td>

Software Subscription\[samp\_sw\_subscription\]

</td><td>

Number of subscriptions that don't meet the usage requirements defined by the reclamation rules.

</td></tr><tr><td>

User summary Percent of stale subscriptions

</td><td>

Software Subscription\[samp\_sw\_subscription\]

</td><td>

Percentage of subscriptions that don't meet the usage requirements defined by the reclamation rules. This percentage is calculated as the number of stale rights divided by the total number of assigned rights.

</td></tr><tr><td>

User summary Subscriptions with blocked users

</td><td>

Software Subscription\[samp\_sw\_subscription\]

</td><td>

Number of subscriptions that are consumed by users that have their access blocked by the admin due to security issues.**Note:** Currently, the Blocked users report is supported only for Microsoft 365.

</td></tr><tr><td>

Active vs stale subscriptions over time

</td><td>

Software Subscription\[samp\_sw\_subscription\]

</td><td>

Graphical representation of actively used vs stale subscriptions over a given time period.

</td></tr><tr><td>

Snapshot of last meaningful activity

</td><td>

Software Subscription\[samp\_sw\_subscription\]

</td><td>

Distribution of users based on their subscription software usage behavior. Use this data to identify the users with the highest software usage and determine the most appropriate threshold for your software reclamation rules. This report displays the data if there's no activity, for 30 days, and for 120 or more days.

</td></tr><tr><td>

Subscription spend by cost center

</td><td>

Software Entitlement\[alm\_license\]

</td><td>

Total cost of all active subscription software entitlements by cost center.

</td></tr><tr><td>

Stale subscriptions by instance

</td><td>

Removal Candidate \[samp\_sw\_reclamation\_candidate\]

</td><td>

Total number of stale subscriptions for each subscription profile. If you have multiple profiles for the same subscription software, this report displays each profile separately.

</td></tr><tr><td>

Potential savings by instance

</td><td>

Removal Candidate \[samp\_sw\_reclamation\_candidate\]

</td><td>

Potential costs saved for each subscription profile when you reclaim unused subscriptions.

</td></tr><tr><td>

SaaS detection

</td><td>

DEX Applications \[samp\_dex\_application\]**Note:** This table has been repurposed for use with the ACC-VC product 1.3.0.

</td><td>

Number of SaaS applications or percentage of the total applications that are managed and unmanaged.-   **Managed**: A software model exists for a product.
-   **Unmanaged**: A software model doesn't exist for a product.

**Important:** To view this chart, you must do the following:

-   Request and install the latest version of the Software Asset Management -SaaS License Management application from the [ServiceNow Store](https://store.servicenow.com/). For more information, see [Request SaaS License Management](../task/request-saas-license-management.md).
-   Install the Agent Client Collector for Visibility - Content \(ACC-VC\) product version 1.3.0 or later. For more information, see [Agent Client Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-landing-page.md).

For more information, see the [SaaS detection report](shadow-saas-analytics.md) report.

</td></tr><tr><td>

Consumption summary Total units

</td><td>

Subscription Consumption Summary\[sam\_saas\_consumption\_summary\]

</td><td>

Total number of software units that you’ve purchased across all active entitlements for the software model.

</td></tr><tr><td>

Consumption summary Total cost

</td><td>

License Metric Results\[samp\_license\_metric\_result\]

</td><td>

Total cost of the software units across all active entitlements for the software model.

</td></tr><tr><td>

Consumption summary units consumed

</td><td>

License Metric Results\[samp\_license\_metric\_result\]

</td><td>

Number of software units that you’ve consumed. Unit of measure for the software units that can be consumed.

</td></tr><tr><td>

Consumption summary units remaining

</td><td>

License Metric Results\[samp\_license\_metric\_result\]

</td><td>

Number of software units that haven’t been consumed.

</td></tr><tr><td>

Consumption units over time

</td><td>

License Metric Results\[samp\_license\_metric\_result\]

</td><td>

Graphical representation of the number of software units consumed vs the number of software units that aren't consumed over a period.

</td></tr></tbody>
</table>