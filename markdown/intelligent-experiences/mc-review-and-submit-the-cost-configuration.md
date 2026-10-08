---
title: Review and submit the cost configuration
description: Review all Cost Framework configurations, verify the calculations, and submit to activate the Cost Framework.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/mc-review-and-submit-the-cost-configuration.html
release: australia
topic_type: task
last_updated: "2026-10-08"
reading_time_minutes: 2
breadcrumb: [Cost, Configure, Measure AI system, Measure AI systems, AI Control Tower, Enable AI experiences]
---

# Review and submit the cost configuration

Review all Cost Framework configurations, verify the calculations, and submit to activate the Cost Framework.

## Before you begin

Role required: AI steward \(`sn_ai_governance.ai_steward`\).

## About this task

Before activating the Cost Framework, review all configurations to verify accuracy. The review screen displays how total savings are calculated based on the hourly rate. It also shows how total cost is calculated, which encompasses all vendors combined. Additionally, there is a preview of the Net AI Returns calculation. After verification, these calculations appear in dashboards and reports.

Cost entries that you add or change remain in draft until you submit them in the **Preview cost &amp; savings** step.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Settings** &gt; **Rules and Templates** &gt; **Cost**.

2.  Select **Edit configuration**.

3.  Verify that the average rate, integrated vendor pricing, and other vendor pricing \(if applicable\) are configured.

    For more information, see [Configure average hourly rate for your organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/mc-configure-the-average-hourly-rate-for-your-organization.md), [Add costs for integrated vendors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/mc-add-and-configure-costs-for-integrated-vendors.md), and [Add costs for other vendors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/mc-add-and-configure-costs-for-non-integrated-vendors.md).

4.  In the **Preview cost &amp; savings** section, review the details.

    |Section|Description|
    |-------|-----------|
    |**Preview total savings**|Total savings for the listed personas, calculated as productivity gains in hours multiplied by the average hourly rate. The section also shows **Total productivity gains \(hours\)** and **Personas applicable**.|
    |**Preview total cost**|Total Enterprise AI cost across vendors, based on the information entered in the previous steps.|

    To change a value, select **Back**.

5.  Select **Submit** to activate the Cost Framework.

    The **Cost** tab shows the **Cost setup** summary with the status **Configured** and an updated **Last updated at** date.


## Result

The Cost Framework configuration is active. The Cost Framework calculates total savings, total costs, and Net AI Returns based on your specifications, and dashboards and reports show the financial impact of AI usage.

## What to do next

Verify that the Cost Framework is active in the dashboards:

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Insights** &gt; **Value**.
2.  Confirm that the Productivity Gains widget displays total money saved, not just hours. The Net AI Returns widget shows total calculated returns. The Total AI Cost widget indicates the aggregated vendor costs.
3.  Verify that these values match the values on the Cost setup page.

After submission:

-   Check the Cost Framework dashboards weekly to track costs and savings.
-   If vendor pricing changes or you add new vendors, reconfigure them from **Settings** &gt; **Rules and Templates** &gt; **Cost**.
-   Reassess hourly rates and vendor pricing quarterly to verify accuracy.
-   Watch for unexpected cost spikes or changes in savings patterns.
-   Share Cost Framework insights with stakeholders for budget and investment decisions.

