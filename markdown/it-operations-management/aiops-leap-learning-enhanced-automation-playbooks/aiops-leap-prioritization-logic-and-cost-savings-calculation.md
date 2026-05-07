---
title: LEAP prioritization logic and cost savings calculation
description: LEAP uses built-in prioritization logic to identify the highest-impact automation opportunities. This logic helps you focus on the most valuable automation tasks. The calculations provide an estimate of potential cost and time savings. It's best to validate these values in a non-production environment before implementing them in production.
locale: en-US
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Exploring LEAP, Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# LEAP prioritization logic and cost savings calculation

LEAP uses built-in prioritization logic to identify the highest-impact automation opportunities. This logic helps you focus on the most valuable automation tasks. The calculations provide an estimate of potential cost and time savings. It's best to validate these values in a non-production environment before implementing them in production.

The automation priority is calculated by combining the following key factors:

-   Business impact
-   Projected cost/time savings

The priority for an automation opportunity is determined using the following chart.

![automation opportunity priorities](../images/projected-cost-time-savings.png "Automation opportunity priority")

The key factors are evaluated for each group of related incidents, called  automation opportunities, and the results help teams focus on high-value areas.

## Business impact

Each automation opportunity is a cluster of tickets. Every ticket is scored based on the following factors:

-   Business criticality
-   Major incident status
-   Impact level

These factors are given values. Example values for  criticality:

-   Most Critical = 100%
-   Somewhat Critical = 75%
-   Less Critical = 50%
-   Not Critical = 25%

|Key|Default value|Description|
|---|-------------|-----------|
|ohf\_p4|0.8|Overhead factor for P4 records.|
|ohf\_p5|0.4|Overhead factor for P5 records.|
|ohf\_p1|1.8|Overhead factor for P1 records.|
|ohf\_p2|1.4|Overhead factor for P2 records.|
|cost\_per\_entry|20|Cost in dollars associated with adding a work note entry to a record.|
|ohf\_p3|1.1|Overhead factor for P3 records.|
|time\_per\_entry|0.5|Time in hours associated with adding a work note entry to a record.|
|first\_run\_group\_limit|0|Total number of groups for which resolution steps are generated in the initial run.|
|gaf\_mapping\_min\_threshold|0.2|Minimum ratio of incidents pointing to an active group that is considered for remapping after clustering.|

**Note:**

-   You can modify the values in the LEAP settings page. However, the calculations will differ when you change the values.
-   The values in the LEAP settings page should be modified before activating LEAP.
-   If you modify the values in the LEAP settings page, you need to rerun the calculation. For this, you must deactivate and reactivate the LEAP installer skill.

Each factor is weighted. For example, say that Criticality = 0.8, Major Incident = 0.2, and Impact = 0.4.

```
Ticket Score = (Criticality × 0.8 + Major Incident × 0.2 + Impact × 0.4) ÷ 3
```

The  average of all ticket scores  in the group becomes the  Business Impact Score. Based on this score, automation opportunities are labeled as high impact \(the top 33%\) , medium impact  \(next 33%\), and low impact  \(remaining 33%\).

## Projected cost or time savings impact

LEAP estimates how much time and cost can be saved by automating a group of incidents with historical ticket data.

The key inputs for cost and time savings are the following:

-   Frequency of Incidents \(FOI\) : Average number of similar incidents per month
-   Average Manual Work Notes Count \(AWNC\)
-   Overhead Factor \(OHF\) : varies by incident priority based on the priorities table

LEAP uses the following formulas to calculate the projected cost or time savings:

-   `Projected Cost Savings = ∑ (FOI × OHF) × AWNC × Cost per Work Note`
-   `Projected Time Savings = ∑ (FOI × OHF) × AWNC × Agent Time per Entry`

Each ticket’s projected savings is calculated. The  average for the group  becomes the  Projected Cost/Time Savings Score, which is also categorized as  High,  Medium, or  Low. The automation opportunities are sorted in descending order based on the projected cost or time savings.

## Determining overall priority

After calculating the values for the business impact and the projected cost/time savings, LEAP assigns a priority level to each automation opportunity using this matrix:

|Business impact|Projected cost/time savings|Automation priority|
|---------------|---------------------------|-------------------|
|High|High|Very High|
|Medium|High|High|
|High|Medium|High|
|Medium|Medium|Medium|
|Medium|Low|Low|
|Low|Medium|Low|
|Low|Low|Very Low|

These prioritized automation opportunities are displayed on the LEAP home page.

## Tracking the actual cost and time savings

After automation is implemented, LEAP tracks  actual cost and time savings and displays them on the  LEAP Value Dashboard, helping you measure impact and make decisions.

Key metrics:

-   Additional Work Notes \(AWN\) : Manual entries after playbook execution
-   Overhead Factor \(OHF\) by Priority : For example, P1 = 1.8x

Formulas:

-   `Saved Work Notes (SWNs)  = AWNC – AWN`
-   `AWN = SWN × OHF`
-   `Actual Cost Savings = AWN × Cost per Work Note`
-   `Actual Time Savings = AWN × Agent Time per Entry`

## Example projected cost and time savings calculations

A cluster has 20 AWNC and is mapped to a P2 incident with 6 AWN. The cost per work note is $20, and the agent time per entry is 0.5 hours.

According to the formulas, the SWN count is `(20 - 6) = 14`. According to the properties tables, the OHF = 1.4.

`SWN x OHF = AWN` so `14 x 1.4 = 19.6`

This value can be rounded off to 20 AWN. Each AWN entry represents $20 of savings.

The actual cost savings post automation = `AWN x Cost per Work Note` = `20 x 20 = $400`.

So, if you use automation, then the projected cost savings can be up to $400. Thus, the calculation provides actionable insights for ongoing process improvement and resource allocation.

