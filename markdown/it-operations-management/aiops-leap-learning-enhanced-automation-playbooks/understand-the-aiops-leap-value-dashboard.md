---
title: Monitor automation opportunities using the LEAP value dashboard
description: Use the dashboard to track automation opportunities, cost savings, and operational efficiency metrics.
locale: en-US
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [LEAP dashboard, automation opportunities, cost savings, operational efficiency]
breadcrumb: [Using LEAP, Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# Monitor automation opportunities using the LEAP value dashboard

Use the dashboard to track automation opportunities, cost savings, and operational efficiency metrics.

## Before you begin

Role required: admin

## About this task

The LEAP value dashboard provides real-time insights into automation opportunities within your IT operations. Use this dashboard to justify automation investments and track the return on automation initiatives.

## Procedure

1.  Navigate to the LEAP dashboard by selecting the dashboard icon ![](../images/dashboard-icon.png).

    The dashboard displays records analyzed and grouped into automation opportunities.

    ![LEAP value dashboard showing automation metrics and opportunities](../images/leap-value-dashboard.png)

    The dashboard opens, displaying automation metrics and grouping statistics.

2.  Review the Grouping statistics section.

    1.  Review the total number of records analyzed.

        This metric shows the volume of data processed by LEAP.

    2.  Check the number of groups created and average group size.

        Groups represent similar incidents that can be automated together.

    3.  Identify large groups that exceed the automation threshold.

        Large groups indicate high-value automation opportunities.

    4.  Note the record duration and last GAF run timestamp.

        This information shows the data freshness and analysis scope.

3.  Review the Automation Value section.

    1.  Review the predicted cost and time savings from automation.

        These projections help justify automation investments.

    2.  Check the number of playbooks created and tickets resolved.

        These metrics demonstrate actual automation implementation and success.

    You can see the quantified benefits of your automation initiatives.

4.  Contact your LEAP administrator to customize settings when dashboard metrics do not align with organizational requirements.

    LEAP administrators can adjust calculation parameters, thresholds, and time ranges to match your business context.


## Result

The dashboard displays current automation metrics including potential cost savings, time savings, and automation opportunities. Use these metrics to prioritize automation initiatives and demonstrate ROI to stakeholders.

If the dashboard shows no data, verify that LEAP has processed incident records within the specified time range and that the GAF analysis has completed successfully.

