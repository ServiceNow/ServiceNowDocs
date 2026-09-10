---
title: Exploring Measure
description: Measure helps you determine whether your AI systems deliver more value than they cost. It brings value and cost data together in dashboards so that you can compare productivity gains with AI spend.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
---

# Exploring Measure

Measure helps you determine whether your AI systems deliver more value than they cost. It brings value and cost data together in dashboards so that you can compare productivity gains with AI spend.

Measure is one of the AI Control Tower pillars. It helps you quantify the value your AI systems deliver, track what they cost, and monitor the results over time. Measure includes the following components.

## Value

Value translates AI usage into measurable productivity metrics. It uses value templates and value jobs to assess the impact of AI usage on productivity and to calculate the productivity gains from your AI systems.

A value template is the metric that converts AI usage into productivity gains. Each template includes a usage indicator, the minutes saved per occurrence, and a quality score. Templates are reusable by design, so a single template can be applied to multiple AI systems.

Value jobs are scheduled tasks that run at set intervals—daily \(default\), monthly, or quarterly—to capture usage and user metrics and to power dashboards.

## Cost

Cost records the actual expenses associated with your AI systems, enabling AI Control Tower to compare these costs against productivity gains and calculate the net return on investment. You configure costs by entering your organization's average hourly rate and defining prices for integrated and non-integrated vendors. The cost configuration converts token usage and ServiceNow Assist consumption into monetary costs.

## Dashboards

Dashboards are where value and cost come together. Dashboards display productivity gains, AI costs, and the net return on AI investment. They break down usage and costs by user and department, highlight adoption trends, and identify AI systems that show no usage.

## How Measure turns AI usage into business value

Measure uses value templates, hourly rates, and vendor costs to calculate the value and cost of AI systems. The value measurement follows this sequence.

1.  Define how value is calculated.

    A value template defines the calculation. The template captures a persona, a usage metric, a time value, and a quality \(acceptance\) value.

2.  Convert time saved into financial value.

    Configure hourly rates globally or by persona to convert productivity gains, measured in hours, into monetary value.

3.  Add costs for integrated vendors.

    Add cost details for ServiceNow and integrated vendors so that Measure can calculate costs from monitored usage and observability data.

4.  Add costs for non-integrated vendors.

    Add cost details for vendors that aren't integrated with ServiceNow by using a token-based calculation or by entering the total cost directly.

5.  Calculate savings, cost, and return.

    Total savings and total cost are calculated for the selected time period. Total savings represent the productivity gains, calculated as the total dollar amount saved by using AI systems. Total cost includes the overall token and Assist costs associated with using these AI systems.

6.  Review results on dashboards.

    Dashboards display savings, cost, and net AI return, with breakdowns by AI system, department, and user.


