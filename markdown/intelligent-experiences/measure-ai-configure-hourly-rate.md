---
title: Configure hourly rates in cost framework
description: Learn how to set the average hourly rate used to convert hours saved into financial savings in the Cost Framework.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/measure-ai-configure-hourly-rate.html
release: zurich
topic_type: task
last_updated: "2026-07-27"
reading_time_minutes: 1
breadcrumb: [Configure cost framework, Configure, Measure AI impact and value, Measure AI impact, AI Control Tower, Enable AI experiences]
---

# Configure hourly rates in cost framework

Learn how to set the average hourly rate used to convert hours saved into financial savings in the Cost Framework.

## Before you begin

Role required: AI steward \(sn\_ai\_governance\_ai\_steward\)

## About this task

The hourly rate is the foundation of the Cost Framework. The average hourly rate represents the fully-loaded cost of an average employee \(including salary, benefits, and overhead\) divided by annual working hours. It converts productivity hours \(hours saved through AI automation\) into financial savings.

**Formula:** Money Saved = Hours Saved × Average Hourly Rate

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Settings** &gt; **Rules and Templates** &gt; **Cost**.

2.  Select **Configure** in the **Value and cost configuration** card under the Cost setup section.

3.  In the selected **Configure hourly rates** section, locate the **Average hourly rate** field.

    Determine the correct hourly rate for your organization. To calculate Average hourly rate:

    1.  Gather total annual cost of labor including salaries, benefits, payroll taxes, overhead allocation, and benefits.
    2.  Calculate total annual working hours \(typically 2,000-2,080 hours for full-time employees\)
    3.  Divide total cost by annual hours
    **Example:** If total annual labor cost is $100,000 and annual working hours are 2000, hourly rate = $100000 / 2000 = $50/hour

    **Note:** Enter the rate in your organization's local currency.

4.  With **Set up a global rate** selected, enter the hourly rate.

5.  Select **Set up rates per persona** and enter multiple rates if your organization has significant variations in labor costs by department or cost center.

6.  Select **Next** to continue or **Save and close** to complete the configuration process later.


## Result

Your organization's average hourly rate is now configured, and the cost framework starts using this rate to convert productivity hours into financial savings, enabling net return calculations.

