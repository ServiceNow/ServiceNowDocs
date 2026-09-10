---
title: Review and submit the cost configuration
description: Review all Cost Framework configurations, verify the calculations, and submit to activate the Cost Framework.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
---

# Review and submit the cost configuration

Review all Cost Framework configurations, verify the calculations, and submit to activate the Cost Framework.

## Before you begin

Role required: AI steward \(`sn_ai_governance_ai_steward`\).

## About this task

Before activating the Cost Framework, review all configurations to verify accuracy. The review screen displays how money saved is calculated \(based on the hourly rate\), how total cost is calculated \(all vendors combined\), and a preview of the net returns calculation. After your verification is complete, the system uses these calculations in dashboards and reports.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Settings** &gt; **Rules and Templates** &gt; **Cost**.

2.  Select **Edit configuration**.

3.  Make sure you have configured the average rate, added integrated vendor pricing, and added other vendor pricing \(if applicable\).

    For more information, see [Configure average hourly rate for your organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mc-configure-the-average-hourly-rate-for-your-organization.md), [Add costs for integrated vendors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mc-add-and-configure-costs-for-integrated-vendors.md), and [Add costs for other vendors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mc-add-and-configure-costs-for-non-integrated-vendors.md).

4.  Go to **Preview cost &amp; savings** section and review the details.

5.  Select **Submit** to activate the Cost Framework.

    The system uses these configurations for cost calculations.


## Result

Your Cost Framework configuration is complete and active. The system calculates money saved, total costs, and net returns based on your specifications, and dashboards and reports show the financial impact of your AI investments.

## What to do next

Verify that the Cost Framework is active in the dashboards:

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Insights** &gt; **Value**.
2.  Confirm that the Productivity gains widget shows total money saved \(not just hours\), the Net AI Returns widget shows total calculated returns, and the Total AI Cost widget shows aggregated vendor costs.
3.  Verify that these values match the values on the Cost setup page.

After submission:

-   Monitor regularly: Check the Cost Framework dashboards weekly to track costs and savings.
-   Update as needed: If vendor pricing changes or you add new vendors, reconfigure them from **Settings** &gt; **Rules &amp; Templates** &gt; **Cost**.
-   Review quarterly: Reassess hourly rates and vendor pricing quarterly to verify accuracy.
-   Investigate anomalies: Watch for unexpected cost spikes or changes in savings patterns.
-   Use for decisions: Share Cost Framework insights with stakeholders for budget and investment decisions.

