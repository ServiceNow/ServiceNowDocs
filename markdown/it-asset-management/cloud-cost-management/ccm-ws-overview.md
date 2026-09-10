---
title: Cloud cost overview
description: Enhance your experience by using the modernized and user-friendly Cloud Cost Management overview. This overview page helps you use the Cloud Cost Management application more effectively by reducing complexity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/cloud-cost-management/ccm-ws-overview.html
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Cloud Cost Management Workspace, Explore, Cloud Cost Management, IT Asset Management, Asset Management]
---

# Cloud cost overview

Enhance your experience by using the modernized and user-friendly Cloud Cost Management overview. This overview page helps you use the Cloud Cost Management application more effectively by reducing complexity.

**Important:** If you have the insights\_owner role, only the accounts that are assigned to you appear in the filters and data.

Use the Cloud Cost Management overview to,

-   Understand how you currently spend on cloud resources or service accounts for the last 30 days.
-   Gain insights into key metrics such as the total budget and potential savings for your cloud resources.
-   Analyze your spend breakdown and group your results by provider, service category, service account, cloud service, or purchase option. Refine your results by selecting a time range of 3, 6, 9, or 12 months, choosing actual or amortized cost, and toggling forecast cost on or off.

    **Note:** You can view the forecast grouped only by provider or service account.

-   Make smarter cloud cost decisions with AI-powered summarization of cloud spend reports.
-   View cloud spending analytics based on provider, service category, and cloud service.
-   Get information about the top spend trends that are grouped by service category, cloud service, cost center, business service, and provider.
-   Understand your savings breakdown by viewing your potential and actual saving.
-   Get actionable insights into your cloud resources through alerts and recommendations.

\[Omitted image "ccm-overview-ws.png"\] Alt text: Cloud Cost Management overview in the Workspace.

<table id="table_m3g_fz5_ywb"><thead><tr><th>

Report

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total spend this month

</td><td>

Actual spend on your service accounts or cloud resources for the month. Selecting this card navigates you to the Spend dashboard. For more information, see [Spend view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/spend-view-ccm-ws.md).The **Forecasted spend this month** amount displays the total future spends for all your cloud assets.

The **Compared to last month** percentage amount shows the spend difference of the current month and last month.

</td></tr><tr><td>

Total budget

</td><td>

Total budget of your service accounts or cloud assets where the current date falls between the start date and end date of the budget. Selecting this card navigates you to the Budget view. For more information, see [Budget view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/budget-view-ws.md).For a budget owner, the budget for only the created policies is displayed.

The **Forecasted variance** amount shows the budget amount based on the spend on your cloud resources, which is

```
Forecasted spend this month - Total budget.
```

</td></tr><tr><td>

Total potential saving

</td><td>

Total saving for your cloud assets based on all the recommendations that you haven't acted on. Selecting this card navigates you to the Optimization view. For more information, see [Optimization view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/optimization-view-ccm-ws.md).

</td></tr><tr><td>

Monthly spend breakdown

</td><td>

Monthly spend breakdown grouped by provider, service category, service account, cloud service, or purchase option. The results can be sorted by time range and cost type. Use the **Show forecast** toggle switch for hiding or showing the future cost.Selecting the **Summarize** button generates an AI-assisted summary of your cloud spend trends, top cost drivers, and budget alignment with your selected filters and groupings.

Selecting a monthly spend breakdown bar navigates you to the Spend analytics page. The filters that you apply to the Monthly spend breakdown get applied to the Spend analytics page. For more information, see [Spend analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/spend-anaytics.md).

</td></tr></tbody>
</table><table id="table_llc_g3c_2yb"><thead><tr><th>

Report

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Top spend trend

</td><td>

Spend trend or actual cost grouped by service category, cloud service, provider, cost center, business service, and Kubernetes cluster.Selecting a Top spend trend card navigates you to the Spend analytics page. For more information, see [Spend analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/spend-anaytics.md).

</td></tr></tbody>
</table><table id="table_nwp_kz5_ywb"><thead><tr><th>

Report

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Potential vs actual savings grouped by Provider, Service category, and Environment

</td><td>

Potential vs actual savings grouped by provider, service category, and environment.**Note:** To view the Potential vs actual savings grouped by environment chart, you must create tag categories as Production and Non Production. For more information about creating a tag category, see [Create and update a tag category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/tag-category-crud-cloudin.md).

-   **Potential savings**: Indicates the total spend on your cloud resources that could be optimized by the recommendations.
-   **Actual savings**: Indicates the total savings achieved by following the recommendations to optimize your cloud resources.

Selecting a potential or actual savings bar navigates you to the Optimization view. For more information, see [Optimization view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/optimization-view-ccm-ws.md).

</td></tr></tbody>
</table>**Note:** The alerts that you view on the Cloud Cost Management Overview page are for the last one week.

|Alert|Description|
|-----|-----------|
|Last &lt;provider&gt; billing download job failed|The billing download job that downloads, organizes, and stores billing data for your payer account has failed.|
|Last &lt;provider&gt; price sheet download job failed|The price sheet download job that downloads and stores price sheet data for your cloud provider has failed.|
|Scheduled jobs failed|One or more scheduled jobs, which automate processes for cloud providers have failed.|
|&lt;Number&gt; declined recommendations|Number of recommendations that you have declined, which indicates potential savings.|
|&lt;Number&gt; failed recommendations|Number of recommendations that have failed, which indicates potential savings for your cloud resources.|

<table id="table_sb3_f12_cxb"><thead><tr><th>

Recommendation

</th><th>

Description

</th></tr></thead><tbody><tr><td>

All

</td><td>

Displays all the recommendations that Cloud Cost Management provides for your cloud assets.

</td></tr><tr><td>

Business hour

</td><td>

The Business hour recommendation helps you identify resources that are running when they should be powered off.

</td></tr><tr><td>

Commitments

</td><td>

The Commitments recommendation helps you identify resources that would save you money with reservation plans or saving plans.You can accept or decline the recommendation.

</td></tr><tr><td>

Rightsizing

</td><td>

The Rightsizing recommendation helps you identify the users, user groups, or locations that are wasting money by running over-provisioned or underused resources. You can schedule the rightsizing processes and specify the amount of potential rightsizing savings that triggers notifications.

</td></tr><tr><td>

Unused

</td><td>

The Unused recommendation helps you identify the unused resources. You can schedule unused machines to be powered off or terminated.

</td></tr></tbody>
</table>