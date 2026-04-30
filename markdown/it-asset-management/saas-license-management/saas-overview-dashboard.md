---
title: SaaS Overview dashboard
description: Optimize how much your organization spends on SaaS and SSO licensing by analyzing the subscription usage, cost, and compliance of your SaaS applications and SSO providers using the SaaS Overview dashboard.
locale: en-US
release: zurich
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# SaaS Overview dashboard

Optimize how much your organization spends on SaaS and SSO licensing by analyzing the subscription usage, cost, and compliance of your SaaS applications and SSO providers using the SaaS Overview dashboard.

**Important:** The SaaS Overview dashboard is available in both the Software Asset Management classic application and the Software Asset Workspace. This topic provides information on the SaaS Overview dashboard in the Software Asset Management classic application. For information on the SaaS Overview dashboard in the Software Asset Workspace, see [SaaS overview dashboard in workspace](../reference/saas-dashboard-workspace.md).

The Engineering License Overview dashboard is no longer available for new Zurich users who have activated the Software Asset Management Professional \(com.snc.samp\) plugin or upgraded to Zurich without activating the Software Asset Management Professional \(com.snc.samp\) plugin prior to Zurich.

-   If you activated the Software Asset Management Professional \(com.snc.samp\) plugin prior to Zurich but didn't activate the Workspace plugin \(com.sn\_sam\_workspace\), you have access to this dashboard.
-   If you activated the Software Asset Workspace \(sn\_sam\_workspace\) store application after upgrading to Zurich, you won’t be able to access this dashboard from the **Software Asset** navigation menu in your instance. You can however access this dashboard from the **Dashboards** navigation menu.

The SaaS Overview dashboard displays information about the usage, costs, and potential savings that are associated with your SaaS and SSO applications. Access this dashboard by navigating to **SaaS License** &gt; **Overview**. You can filter the dashboard by software model or publisher. Click any report to see more information.

**Note:** To view your organization's software usage and compliance for Microsoft Office 365 and Adobe Cloud, navigate to **SaaS License** &gt; **Office 365 &amp; Adobe Cloud**.

![SaaS Overview dashboard shows SaaS cost and usage.](../image/saas-license-dashboard.png "SaaS Overview dashboard")

<table id="table_r1f_s3d_4fb"><thead><tr><th>

Report

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Current Subscription Spend

</td><td>

Total cost of all active subscription software entitlements.

</td></tr><tr><td>

Percentage of Unused Subscriptions

</td><td>

Percentage of subscriptions that don't meet the usage requirements that are defined by reclamation rules. This percentage is calculated as the number of stale rights \(subscriptions that have limited to no activity within the activity threshold that is defined in the reclamation rule\) divided by the total number of assigned rights.

</td></tr><tr><td>

SaaS Potential Savings

</td><td>

Potential cost saved if you reclaim unused subscriptions.

</td></tr><tr><td>

Assigned Subscriptions

</td><td>

Total number of assigned subscriptions.

</td></tr><tr><td>

True-up Cost

</td><td>

Cost to have the number of rights you own match the number of rights you've assigned to users. This metric helps to verify that your organization is paying for all the rights that your organization is using.

</td></tr><tr><td>

Actual Savings Year-to-Date

</td><td>

Total yearly savings for all subscription software. This value is calculated as the total savings from closed complete reclamation candidates.

</td></tr><tr><td>

Snapshot of Last Meaningful Activity

</td><td>

Distribution of users based on their subscription software usage behavior. Use this data to identify the users with the highest software usage and determine the most appropriate threshold for your software reclamation rules. This report displays the data for the last 30 days, 30–60 days, 60–90 days, and 90–120 days.

</td></tr><tr><td>

Stale Subscriptions by Instance

</td><td>

Total number of stale subscriptions for each subscription profile. If you have multiple profiles for the same subscription software, this report displays each profile separately.

 You can filter the data that is displayed on this report by selecting an option from the Breakdown list. To view the stale subscriptions for both SaaS and SSO subscription profiles, select **All Subscriptions**. To view the stale subscriptions for only SaaS subscription profiles, select **Subscriptions Excluding SSO**.

</td></tr><tr><td>

Subscription Spend by Cost Center

</td><td>

Total cost of all active subscription software entitlements by cost center.

</td></tr><tr><td>

Potential SaaS Savings by Instance

</td><td>

Potential cost saved for each subscription profile if you reclaim unused subscriptions.

 You can filter the data that is displayed on this report by selecting an option from the Breakdown list. To view the potential savings for both SaaS and SSO subscription profiles, select **All Subscriptions**. To view the potential savings for only SaaS subscription profiles, select **Subscriptions Excluding SSO**.

</td></tr></tbody>
</table>**Parent Topic:**[SaaS License Management](sam-subscription-management.md)

**Related topics**  


[Request SaaS License Management](../task/request-saas-license-management.md)

[SaaS License Management setup for large companies](saas-setup-large-companies.md)

[Integrate with SaaS applications](create-integration-profile.md)

[Integrate with SSO providers](saas-sso-integration.md)

[Playbook for SaaS integrations](playbook-saas-integrations.md)

[Viewing your SaaS and SSO subscriptions](usage-summary-saas.md)

[Review a software reclamation rule](../task/add-reclamation-rule-sub.md)

[Reclaiming user subscriptions](reclaiming-user-subscriptions-saas.md)

[Create a child alias to set up multiple integration profiles](../reuse/create-child-alias-saas.md)

[Create a child alias to set up multiple Cisco Webex integration profiles](../task/create-child-alias-webex.md)

[Create a child alias to set up multiple Confluence Cloud integration profiles](../task/create-child-alias-confluence.md)

[Create a child alias to set up multiple Jira integration profiles](../task/create-child-alias-jira.md)

[Create a child alias to set up multiple Slack workspace integration profiles](../task/create-child-alias-slack-ws.md)

[Associate a user with subscription records](../task/map-user-data.md)

[Disconnect SSO apps](../task/disconnect-azure-ad-apps.md)

[Delete an integration profile](delete-saas-integration.md)

[Subscription identifiers for SaaS and SSO applications](subscription-identifiers.md#)

[Subscription exclusions for SaaS and SSO applications](subscription-exclusions.md#)

