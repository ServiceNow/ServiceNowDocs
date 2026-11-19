---
title: Review and submit the cost configuration
description: Review all Cost Framework configurations, verify the calculations, and submit to activate the Cost Framework.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/mc-review-and-submit-the-cost-configuration.html
release: zurich
topic_type: task
last_updated: "2026-11-19"
reading_time_minutes: 2
breadcrumb: [Cost, Configure, Measure AI systems, Measure AI systems, Super Intelligence Control Tower, Enable AI experiences]
---

# Review and submit the cost configuration

Review all Cost Framework configurations, verify the calculations, and submit to activate the Cost Framework.

## Before you begin

Role required: AI steward \(`sn_ai_governance.ai_steward`\).

## About this task

Before activating the Cost Framework, review all configurations to verify their accuracy. The review screen shows how money saved is calculated based on the hourly rate. It also displays how the total cost is determined by combining all vendors. Additionally, there's a preview of the net returns calculation. After your verification is complete, the system uses these calculations in dashboards and reports.

## Procedure

1.  Make sure you have configured the average rate, added integrated vendor pricing, and added other vendor pricing \(if applicable\).

    For more information, see [Configure average hourly rate for your organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mc-configure-the-average-hourly-rate-for-your-organization.md), [Add costs for integrated vendors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mc-add-and-configure-costs-for-integrated-vendors.md), and [Add costs for other vendors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mc-add-and-configure-costs-for-non-integrated-vendors.md).\[Omitted image "mc-review-and-submit.png"\] Alt text: Preview cost &amp; savings step showing total productivity gains, total savings, and total Enterprise AI cost for the last 31 days, with the Submit button.

2.  Go to **Preview cost &amp; savings** section and review the details.

3.  Select **Submit** to activate the Cost Framework.

    The system uses these configurations for cost calculations.


## Result

Your Cost Framework configuration is complete and active. The system calculates money saved, total costs, and net returns based on your specifications, and dashboards and reports show the financial impact of your AI investments.

## What to do next

Verify that the Cost Framework is active in the dashboards:

1.  Navigate to **All** &gt; **Control Tower** &gt; **Insights** &gt; **Value**.
2.  The Productivity Gains widget shows total money saved, not just hours. The Net AI Returns widget displays total calculated returns. The Total AI Cost widget presents aggregated vendor costs.
3.  Verify that these values match the values on the Cost setup page.

After submission:

-   Monitor regularly: Check the Cost Framework dashboards weekly to track costs and savings.
-   Update as needed: If vendor pricing changes or you add new vendors, reconfigure them from **Settings** &gt; **Rules &amp; Templates** &gt; **Cost**.
-   Review quarterly: Reassess hourly rates and vendor pricing quarterly to verify accuracy.
-   Investigate anomalies: Watch for unexpected cost spikes or changes in savings patterns.
-   Use for decisions: Share Cost Framework insights with stakeholders for budget and investment decisions.

