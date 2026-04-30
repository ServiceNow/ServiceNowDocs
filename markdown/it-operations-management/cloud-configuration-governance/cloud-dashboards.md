---
title: Cloud Provisioning and Governance dashboards and reports
description: Dashboards enable cloud admins and cloud users to view reports like cloud billing data and cloud tag usage.The Billing dashboard provides rich summary information on cloud usage, cost trends, and cost aggregates.The Tag dashboard shows all tagged resources. Use the Tag dashboard to see specific tag values for a group of resources such as stacks or virtual machines.Administrators can assign a budget for a group and a user within the group. When the user or group reaches the budget limit threshold, notifications are sent alerting them about it.You can configure budgets for groups and users within that group. You can set up a budget period for the group, allocate a budget limit to a group and to each user within that group.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Provisioning and Governance dashboards and reports

Dashboards enable cloud admins and cloud users to view reports like cloud billing data and cloud tag usage.

Demonstrates billing setup options for Cloud Provisioning and Governance.Follow this short video to learn more about Cloud Provisioning and Governance dashboards.

**Important:** Starting with the Zurich release, the Billing dashboard is no longer available if you have downloaded the ServiceNow Store Cloud Cost Management app. The following changes occur:

-   You are redirected to the Cloud Cost Management home page by default.
-   The View Dashboard widget in the Cloud User portal is replaced by the View Resources widget.
-   The Current Month Spend widget and the Budget widget on the Cloud User portal do not show any data if Cloud Cost Management is activated on the instance.

## View cloud costs on the Billing dashboard

The Billing dashboard provides rich summary information on cloud usage, cost trends, and cost aggregates.

### Before you begin

Role required: sn\_cmp.cloud\_admin

**Important:** You can only access the **Billing Dashboard**, if you have not downloaded and activated the ServiceNow Store Cloud Cost Management app. If you have activated the Cloud Cost Management app, you can only navigate to the Billing Dashboard, if you are using Cloud Provisioning and Governance on a domain separated instance.

### Procedure

1.  In the Cloud Admin Portal, navigate to **Analyze** &gt; **Billing** &gt; **Billing Dashboard**.

    The Billing dashboard shows the **Cloud Cost** tab by default. This tab displays these two graphs:

    -   **Cost Trend**: A line graph showing daily costs over time for the selected **Usage Date**.
    -   **Cost Aggregate**: Total costs for each tag value for the selected **Group by** tag.
    ![The Billing Dashboard](../image/billing-dashboard.png "Cloud Cost tab on the Billing dashboard")

2.  Perform any of the following actions to obtain the tag data you want on the report.

    |Goal|Action|
    |----|------|
    |**Update the billing period**|Select a new option from the Usage Data choice list.|
    |**See data grouped by another tag**|Select a value in the **Group by** choice list under either chart.|
    |**Filter by tag values**|Select a tag value from the list.|
    |**Save an image of a chart**|Point to either donut chart until the options icon \(![options icon](../image/icon-options.png)\) appears, and then select **Save as PNG** or **Save as JPEG**.|

3.  To view the areas with the highest level of spending, click the **Top Spends** tab.

    Bar charts showing the total cost for each tag display by default. You can further filter the data by **Service Category**, **Provider**, and **Datacenter**.

4.  Click any part of the charts to see cost records for the selected criteria.

    The list view of the cost records appear. You can view information such as usage quantity and specific cost per usage date.

    ![Example cost records](../image/cost-records.png "Example cost records")


## View tagged resources on the Tag dashboard

The Tag dashboard shows all tagged resources. Use the Tag dashboard to see specific tag values for a group of resources such as stacks or virtual machines.

### Before you begin

Role required: sn\_cmp.cloud\_admin

### Procedure

1.  In the Cloud Admin Portal, navigate to **Analyze** &gt; **Tag**.

    The **Tag Dashboard** tab displays the Tag dashboard where all tagged resources are broken down by tag.

    ![The Tag dashboard](../image/tag-dashboard.png "The Tag dashboard")

2.  Perform any of the following actions to obtain the tag data you want on the report.

    |Goal|Action|
    |----|------|
    |**See tag values for a specific resource group**|Click a section of the **Tagged Resources** donut chart.|
    |**See data grouped by another tag**|Select a value in the **Group by** choice list under the **Assigned Tag Values** donut chart.|
    |**See updated data**|Point to the top of either chart until the refresh icon \(![refresh icon](../image/icon-refresh.png)\) appears, and then click the icon.|
    |**Save an image of a chart**|Point to either chart until the options icon \(![options icon](../image/icon-options.png)\) appears, and then select **Save as PNG** or **Save as JPEG**.|

3.  To view a specific tag history record, click any section in the **Assigned Tag Values** chart.

    A list of tag histories appears that matches the CI class for the selected tag value.

    ![A tag history record](../image/tag-history-record.png "A tag history record")

    |Field|Description|
    |-----|-----------|
    |Created|The date the tag history was created.|
    |Current|If selected, indicates if the current record is the must current.|
    |CMDB CI|The actual CI in the CMDB. Click the record icon to see the CI form.|
    |User group|The group tag associated with this CI.|
    |User|The user tag associated with this CI.|
    |Application|The application tag associated with this CI.|
    |Stack|The stack tag associated with this CI.|
    |Business service|The business service tag associated with this CI.|
    |ServiceNow instance|The instance tag associated with this CI.|
    |Cost center|The cost center tag associated with this CI.|
    |Time provisioned|The date the machine was provisioned.|
    |Project|The project tag associated with this CI.|
    |Custom values|Any custom values tagged to the CI.|


## Budget-based notification and approval

Administrators can assign a budget for a group and a user within the group. When the user or group reaches the budget limit threshold, notifications are sent alerting them about it.

**Important:**

-   The budget-based notification and approval feature is no longer available if you are using the Cloud Cost Management app for cloud billing.
-   You can only continue using the Budget Consumption feature if you are using Cloud Provisioning and Governance on a domain separated instance, or have switched back to the native Cloud Provisioning and Governance billing feature.

Administrators can assign a budget \(in USD\) on a weekly, monthly, quarterly, or yearly basis. The budget set for a user and for a group are independent of each other. For example, a group consisting of five users can have a budget of $100 and each user in that group can be assigned a limit of 25 dollars. An organization decides on the frequency of the budget and all the groups in that organization follow the same frequency. For example, if an organization decides on a monthly budget, then all the groups and users in that organization follow a monthly budget. See [Configure budgets](cloud-dashboards.md#).

A default budget is given to each new group and new user. A new group gets a default budget of $1000 and a new user gets a default budget of 100 dollars.

Administrators can increase or decrease the budget at any given time. Notifications are sent to the user and the group when the budget limit reaches its threshold limits. Notifications trigger as part of the billing process. Billing discovery is scheduled for each user and group. At the end of the billing discovery, a comparison is made between the budget limit and the actual cost and if the threshold has reached or has exceeded, notifications are triggered.

Administrators can set up a policy whereby if the budget limit reaches a particular threshold or exceeds the limit, the administrator gives an approval for the user or the group to continue using the resources. For example, the administrator can create a policy for a group whereby when the group's budget threshold reaches 90%, an approval is required for the group to continue consuming resources. If the administrator does not set up a policy for the budget, the user or the group can continue using the resources.

You can view the budget details on the at **Analyze** &gt; **Budget Consumption**. You can view the budget consumption details for a user as well as for groups.

### Configure budgets

You can configure budgets for groups and users within that group. You can set up a budget period for the group, allocate a budget limit to a group and to each user within that group.

#### Before you begin

Role required: admin

#### Procedure

1.  In the Cloud Admin Portal, navigate to **Govern** &gt; **Budget**.

2.  Click **New** next to **Budget Configuration**.

3.  Fill in the form fields \(as shown in the table\)

    |Field|Description|
    |-----|-----------|
    |Group Name|Select a group from the list.|
    |Budget Period|Select a budget period for the group: weekly, monthly, quarterly, or yearly.|
    |Group Max Limit|Enter a budget limit for the group. By default, the budget limit for each new group is 1000 dollars.|
    |Per User Limit|Enter a budget limit for each user in that group. By default, the budget limit for each new user is 100 dollars.|

4.  Click **Submit**.


