---
title: Add a value configuration in the Business Value dashboard \(Lux UI\)
description: Add a value configuration to define the business value metrics calculated for an AI asset, including average time saved per execution and average hourly rate.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-admin-center-lux-add-value-configuration.html
release: australia
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 2
keywords: [AI Admin Center, Now Assist Center, AI, AI setup, business value]
breadcrumb: [Business Value dashboard \(Lux UI\), View AI assets usage and performance \(Lux UI\), Monitor, AI Admin Center, Enable AI experiences]
---

# Add a value configuration in the Business Value dashboard \(Lux UI\)

Add a value configuration to define the business value metrics calculated for an AI asset, including average time saved per execution and average hourly rate.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

Role required: sn\_na\_center.nac\_admin

## About this task

Value configurations define the data used to calculate business value metrics for each AI asset on the Business Value dashboard. Each configuration specifies the asset, average time saved per execution, and average hourly rate, which are used to calculate the total time saved and total cost saved displayed on the dashboard.

**Note:** This topic describes the AI Admin Center feature based on the Lux user interface \(UI\). If you're using the Next Experience UI for AI Admin Center, see the Next Experience UI version of this topic.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **Home** or **Admin** &gt; **AI Admin Center**.

    The home page opens.

2.  Select **Analytics** \(\[Omitted image "icon-aiac-lux-nav-monitor.png"\] Alt text: Analytics icon.\) in the side navigation panel.

3.  Select the **Business Value** tab.

4.  Select **Add configuration**.

    The **Add value configuration** modal opens.

5.  Select an **Asset type**.

6.  Select an **Asset name**.

    The **Execution count \(Last 7 days\)** field is automatically populated based on the selected asset's execution history and is read-only.

    The **Currency** field displays the currency configured for your instance. To change the currency, update your instance configuration.

7.  Enter a value in **Average time saved per execution \(min\)**.

8.  Enter a value in **Average hourly rate**.

    The **Total time saved \(hrs\)** and **Total cost saved** fields are calculated automatically based on the execution count, average time saved per execution, and average hourly rate values.

9.  Select **Add**.


## Result

A confirmation banner appears. The value configuration is added to the **Business value configuration** table and the Business Value dashboard metrics are updated to reflect the new configuration.

**Parent Topic:**[Business Value dashboard in AI Admin Center \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-lux-business-value-dashboard.md)

