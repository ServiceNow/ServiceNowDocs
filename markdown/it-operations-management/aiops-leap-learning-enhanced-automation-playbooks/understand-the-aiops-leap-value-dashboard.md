---
title: Monitor automation outcomes using the LEAP value dashboard
description: Use the LEAP value dashboard to monitor automation outcomes across ServiceNow playbooks, Ansible playbooks, KB articles, and problem records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/understand-the-aiops-leap-value-dashboard.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: task
last_updated: "2026-08-25"
reading_time_minutes: 3
keywords: [LEAP dashboard, automation opportunities, cost savings, operational efficiency, LEAP artifacts metrics, Ansible playbooks, KB articles, problem records]
breadcrumb: [Use, Learning Enhanced Automation Platform \(LEAP\), ITOM Visibility, IT Operations Management]
---

# Monitor automation outcomes using the LEAP value dashboard

Use the LEAP value dashboard to monitor automation outcomes across ServiceNow playbooks, Ansible playbooks, KB articles, and problem records.

## Before you begin

Role required: LEAP admin

## About this task

The LEAP value dashboard tracks automation outcomes across all outcome types that LEAP produces. Use the **Overview** tab to monitor cross-outcome metrics and identify high-value automation opportunities.

## Procedure

1.  Navigate to the LEAP dashboard by selecting the dashboard icon \[Omitted image "dashboard-icon.png"\] Alt text:.

    The **Default - LEAP value dashboard** page opens. To view a different automation project dashboard, select **Switch project** in the upper-right corner.

    \[Omitted image "leap-value-dashboard.png"\] Alt text: LEAP value dashboard showing the Overview tab with Grouping value, LEAP artifacts metrics, Outcome by type, and Savings by playbooks sections

    The **Overview** tab opens by default, displaying grouping statistics and a summary of all automation outcomes.

2.  Review the **Grouping value** section to understand the scope and results of the analysis.

    This section displays key grouping metrics and analysis metadata:

    -   **Records analyzed** - total number of records that LEAP processed in the current analysis run.
    -   **Total groups** and **Average group size** - clusters of similar incidents that LEAP identified as candidates for automation.
    -   **Large groups** - groups that exceed the automation threshold and represent high-value automation opportunities.
    -   **Table analyzed** - the ServiceNow table that LEAP used as the data source, for example, Incident.
    -   **Last run** - the date of the most recent GAF analysis run.
    -   **Record date range** - date range of records included in the analysis.
3.  Review the **LEAP artifacts metrics** section.

    Use the **Time Period** list in the upper-right of this section to filter all artifact counts by a time range. The default is **Last 6 months**.

    1.  Review the four artifact summary cards: **ServiceNow playbooks**, **Ansible playbooks**, **KB articles created**, and **Problem records created**.

        Each card shows the total count of that artifact type that LEAP created in the selected time period.

    You can see a cross-outcome summary of all artifacts that LEAP generated.

4.  Review the **Outcome by type** section.

    1.  Review the **Playbooks** donut chart.

        The chart breaks down total playbooks by type: **ServiceNow playbooks** and **Ansible playbooks**. The center value shows the combined total.

    2.  Review the **Automated Opportunities** donut chart.

        The chart shows the proportion of automation opportunities that are automated compared to those that are not automated. The center value shows the total number of groups.

5.  Review the **Savings by playbooks** section.

    1.  Check **Total savings by playbooks** and **Total agent-hours saved by playbooks**.

        These values show realized savings from ServiceNow and Ansible playbook executions.

    2.  Review the **Savings distribution** chart.

        The chart shows how total savings are distributed across playbook types.

    You can see quantified savings from playbook-driven automation for the selected time period.


## Result

The **Overview** tab provides a cross-outcome snapshot of all artifacts that LEAP generated and the total savings from playbook automation. To review detailed metrics for a specific outcome type, see the related tasks: [Review ServiceNow playbook metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/review-servicenow-playbook-metrics.md), [Review Ansible playbook metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/review-ansible-playbook-metrics.md), [Review KB article metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/review-kb-article-metrics.md), and [Review problem record metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/review-problem-record-metrics.md).

