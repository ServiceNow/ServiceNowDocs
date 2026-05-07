---
title: LEAP savings metrics
description: LEAP displays two distinct types of savings metrics: projected savings and actual savings. The difference between these metrics helps you correctly interpret the values shown across the platform and make informed decisions about automation opportunities.
locale: en-US
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: concept
last_updated: "2026-04-11"
reading_time_minutes: 5
keywords: [savings metrics, LEAP, automation]
breadcrumb: [Exploring LEAP, Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# LEAP savings metrics

LEAP displays two distinct types of savings metrics: projected savings and actual savings. The difference between these metrics helps you correctly interpret the values shown across the platform and make informed decisions about automation opportunities.

## LEAP Savings metrics overview

When you use LEAP to identify and act on automation opportunities, the platform tracks savings at two stages of the workflow:

-   **Projected savings** — displayed on the LEAP home page *before* you automate, based on historical incident data.
-   **Actual savings** — recorded in resolution reports *after* playbooks execute during completed incident resolutions.

Both metrics are important. Projected savings help you prioritize which opportunities to pursue. Actual savings help you measure the real return on your automation investment.

## Projected savings

Projected savings represent the estimated value that could be realized if an automation opportunity is adopted. These figures appear on the LEAP home page and on individual automation opportunity cards.

LEAP calculates projected savings using the following inputs from your historical incident data:

-   Historical incident volume \(number of incidents per month\)
-   Average manual resolution time \(mean time to resolve, or MTTR\)
-   Estimated automation rate
-   Cost per hour of IT labor

The formula is:

```
Projected savings = Incident volume × Avg. manual resolution time × Estimated automation rate × Cost per hour
```

Projected savings update dynamically as new incidents are ingested and clustered. Because they are based on estimates and historical patterns, they represent a *potential* value, not a guaranteed outcome.

**Important:** The savings number displayed on the LEAP home page is always a projected value. It indicates the potential savings if all identified automation opportunities were fully adopted.

## Actual savings

Actual savings represent the realized value recorded when playbooks are executed during completed incident resolutions. These figures reflect real, measured outcomes and accumulate over time.

LEAP calculates actual savings using the following inputs from playbook execution data:

-   Number of incidents resolved by the playbook
-   Time saved per automated resolution \(manual time minus automated time\)
-   Cost per hour of IT labor

The formula is:

```
Actual savings = Sum of (Time saved per automated resolution × Cost per hour) across all completed playbook executions
```

Actual savings are visible in your resolution reports and savings dashboards. They are recorded per resolution and accumulate as more incidents are handled by playbooks.

## Projected vs. actual savings comparison

The following table summarizes the key differences between the two savings metrics.

| |Projected savings|Actual savings|
|---|-----------------|--------------|
|**Definition**|Estimated value based on historical incident data, displayed on the LEAP home page before playbooks are executed.|Realized value recorded when playbooks are executed during completed incident resolutions.|
|**Data source**|Historical incident volume, MTTR, and manual effort estimates.|Playbook execution logs, time saved per automated resolution, and resolution outcomes.|
|**Where displayed**|LEAP home page and automation opportunity cards.|Resolution reports and savings dashboards.|
|**When calculated**|Continuously, as new incidents are ingested and clustered.|Per resolution, upon successful playbook execution.|
|**Formula**|Incident volume × Avg. manual resolution time × Estimated automation rate × Cost per hour.|Sum of \(Time saved per automated resolution × Cost per hour\) across completed executions.|

## Use case: Password reset automation

This walkthrough follows a realistic scenario to show how projected and actual savings are calculated at each stage of the LEAP workflow.

**The scenario:** Your IT service desk receives approximately 1,200 password reset requests every month. Each request currently takes an agent about 15 minutes to resolve manually. Your organization values IT labor at $50 per hour.

**Step 1: LEAP analyzes your incident history**

LEAP ingests your historical incident data and identifies a cluster of 1,200 recurring password reset incidents per month. It recognizes this as an automation opportunity and displays it on the home page with a priority level based on the automation priority matrix.

**Step 2: LEAP calculates projected savings**

Using historical data, LEAP estimates how much time and money your team could save if this incident type were automated.

The calculation: 1,200 incidents × 15 minutes each = 18,000 minutes = 300 hours per month. At $50 per hour, that equals **$15,000 per month** or **$180,000 per year** in projected savings.

The LEAP home page displays *"Projected savings: $15,000/month"* on the automation opportunity card. This is an estimate based on historical patterns.

**Step 3: You create and activate a playbook**

Based on the automation opportunity, LEAP generates resolution steps for password resets. You review them, create a playbook, and activate it. From this point forward, incoming password reset incidents that match the cluster are handled by the playbook automatically.

**Step 4: Playbook runs and LEAP records actual savings**

Over the next month, the playbook executes against real incidents. LEAP measures the actual time saved for each automated resolution.

-   **Coverage:** The playbook successfully automates 1,040 of the 1,200 incidents \(87%\). The remaining 160 incidents require manual handling due to edge cases such as locked accounts, expired tokens, or multi-factor authentication issues.
-   **Time per automated incident:** Each automated resolution takes about 2 minutes \(versus 15 minutes manually\), saving 13 minutes per incident.
-   **Actual calculation:** 1,040 automated incidents × 13 minutes saved = 13,520 minutes = 225 hours. At $50 per hour = **$11,267 actual savings** for the month.

**Step 5: Compare projected vs. actual savings**

After one month of operation, you can compare the two numbers side by side to understand the real impact of automation.

|Metric|Projected \(before automation\)|Actual \(after automation\)|
|------|-------------------------------|---------------------------|
|Time saved per incident|15 minutes \(estimated\)|13 minutes \(measured\)|
|Monthly time savings|300 hours|225 hours|
|Monthly cost savings|$15,000|$11,267|
|Annual cost savings|$180,000|$135,204|

## Why projected and actual savings differ

A gap between projected and actual savings is normal and expected. The most common reasons include:

-   **Automation coverage:** Not every incident matches the playbook. Edge cases, exceptions, and unusual incident variations still require manual handling.
-   **Processing overhead:** Automated resolutions are fast but not instant. The playbook takes some time per incident rather than zero.
-   **Ramp-up period:** Early in deployment, coverage is typically lower. As playbooks are refined and edge cases are addressed, actual savings trend closer to projected values over time.

**Tip:** Over time, as playbooks are refined and coverage expands, actual savings typically trend closer to projected values. Regularly review your resolution reports to track this improvement.

Projected savings tell you the potential value of an automation opportunity and help you prioritize which opportunities to pursue. Actual savings tell you the real value being delivered and help you measure ROI. Both metrics are important — projected savings guide your decisions, and actual savings validate them.

