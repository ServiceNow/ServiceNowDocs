---
title: Configure average hourly rate for your organization
description: Set the average hourly rate that the Cost Framework uses to convert hours saved into financial savings.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
---

# Configure average hourly rate for your organization

Set the average hourly rate that the Cost Framework uses to convert hours saved into financial savings.

## Before you begin

Determine your organization's total annual labor cost and its annual working hours, or a pre-calculated average hourly rate.

Role required: AI steward \(`sn_ai_governance_ai_steward`\).

## About this task

The average hourly rate represents the cost of an average employee, including salary, benefits, and overhead, divided by annual working hours. This rate converts productivity hours into financial savings.

Cost setup is a four-step process: configure hourly rates, add integrated vendor costs, add other vendor costs, and preview cost and savings. You can select **Save and close** at any step and return to the configuration later.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Settings** &gt; **Rules and Templates** &gt; **Cost**.

2.  Select ******Edit configuration**.

    **Note:**

    The currency shown is the currency configured for the instance. You can't change it here.

3.  In the **Configure hourly rates** section, locate the **Avg hourly rate \(in USD\)** field and determine the correct rate for your organization.

    For example, if the total annual labor cost is $100,000 and the annual working hours are 2,000, the hourly rate is $100,000 ÷ 2,000 = $50/hour.

4.  With **Set up a global rate** selected, enter the hourly rate in the **Avg hourly rate \(in USD\)** field.

5.  Select **Set up rates per persona** and enter multiple rates if your organization has significant variations in labor costs.

    Define a rate for each persona, such as agent, developer, fulfiller, or others.

    Enter the rate in the **Avg hourly rate \(in USD\)** field for each persona listed, for example **Agent** and **Other**. The average hourly rate is required for each persona you want included.

    **Note:**

    Total savings reflect only the personas that have a configured hourly rate. A persona field left empty contributes no savings.

6.  Select **Next** to continue.


## Result

Your organization's average hourly rate is configured. The Cost Framework uses this rate to calculate financial savings from productivity hours.

