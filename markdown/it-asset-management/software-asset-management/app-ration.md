---
title: Overlapping usage view
description: Use the Overlapping usage view in Software Asset Workspace to get insights into the feature level usage and rationalize your SaaS and Single sign-on \(SSO\) applications.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Overlapping usage view

Use the Overlapping usage view in Software Asset Workspace to get insights into the feature level usage and rationalize your SaaS and Single sign-on \(SSO\) applications.

The Overlapping usage view displays reports showing the spend on your applications based on application category - SaaS or spend detection. You can also view the list of applications grouped by categories based on the main function of the software application, such as video conferencing, project management, and email marketing. This list of applications includes the following details:

-   Spend
-   Usage
-   Total number of subscriptions
-   Reclamation candidates

Access the Overlapping usage view by navigating to **Workspaces** &gt; **Software Asset Workspace** &gt; **Overlapping usage**.

**Note:** Request the Software Asset Management - SaaS License Management Integrations application from the [ServiceNow Store](https://store.servicenow.com/) to view the Overlapping usage view.

**Note:** The Overlapping usage dashboard supports domain separation when Domain Extension Installer \(com.glide.domain.msp\_extensions.installer\) and Domain Support \(com.snc.pa.domain\_support\) plugins are activated. To filter the data, select a domain from the Domain drop-down list.

## End users and roles

<table id="table_xjk_42s_cyb"><thead><tr><th>

End user

</th><th>

Required role

</th><th>

Goal

</th></tr></thead><tbody><tr><td>

SAM Admin/SAM User

</td><td>

sam\_admin/sam\_user

</td><td>

View the Overlapping usage dashboard.**Note:** A SAM Admin or a SAM user must have the it\_demand\_user role to create demand. You can create a demand from the Application feature usage page.

</td></tr></tbody>
</table>## Overlapping applications

By selecting the **Overlapping applications** tab, you can view the following information:

-   **Total count**: Total number of overlapping software applications grouped by application category, such as spend detection or SaaS. Selecting any application category bar navigates you to the list of applications of that type with details on their relevant number of subscriptions, total spend, and overall usage.
-   **Total spend**: Total spend on overlapping software applications grouped by application category, such as spend detection or SaaS. Selecting any application category bar navigates you to the list of applications of that type with details on their relevant number of subscriptions, total spend, and overall usage.
-   **All categories with applications**: The list of overlapping software applications grouped by category based on the main function of the software application. The number next to each category indicates the number of applications in that category, such as development and email marketing.

![Overlapping usage view showing the number of applications and their total spend grouped by category](../image/overlapping-usage-workspace.png)

## Application feature usage

By selecting the **Application feature usage** tab, you can view the following information:

-   A list view of the application categories.
-   Detailed and descriptive feature usage information of an application. By expanding an application category, you can view the following data for each application within that category.

<table id="table_xyf_z3s_cyb"><thead><tr><th>

Attribute/Chart

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Spend

</td><td>

Total spend for the application.

</td></tr><tr><td>

Overall usage

</td><td>

The percentage of users who have performed at least one event in the application.

</td></tr><tr><td>

Subscriptions

</td><td>

Total number of subscriptions for the application.

</td></tr><tr><td>

View reclamation candidates

</td><td>

List of reclamation candidates for the application that aren't closed.

</td></tr><tr><td>

Activities with high usage

</td><td>

Top five activities with the highest usage based on the number of users.**Note:**

-   This chart gets replaced by **Users with last login activity** for SSO applications and the SaaS applications for which only the last login activity is pulled.
-   This chart displays data for all events that have normalized mappings available in the SaaS Event Mapping \(samp\_saas\_event\_mapping\) table.


</td></tr><tr><td>

Departments with least usage

</td><td>

Five departments with least usage for the application in your organization. The usage is based on the number of users. This data helps IT administrators to determine if users within these departments need access and alternatively to help drive adoption for those users.

**Note:** This chart displays data only for users who are assigned to a specific department.

</td></tr><tr><td>

Spend trend chart

</td><td>

Graphical representation of monthly spending trends on the application.

</td></tr></tbody>
</table>
![Application feature usage in the Overlapping usage view showing a list view of the application categories](../image/appl-feature-usage.png)

## SaaS feature usage

The SaaS feature usage page includes the event details for each integration, such as the event ID, event name, last activity, subscription, product, subscription profile, and publisher. Navigate to the SaaS feature usage page in the License operations view by selecting the **SaaS feature usage** link.

**Note:** The SaaS feature usage page displays event details for up to one year from the current date.

![SaaS feature usage page in the Overlapping usage view showing the event details for each integration.](../image/saas-feature-usage.png)

## Creating demand to rationalize software applications

Creating demands enables you to take meaningful action against any redundant software you discover. You can discontinue software, reduce software usage, migrate users to approved software, or take other actions.

**Note:** The PPM Standard plugin \(com.snc.financial\_planning\_pmo\) must be installed to create demands.

Select **Create demand** to rationalize software applications. For more information, see [Create demand to rationalize software applications](../task/soft-asset-demand.md).

