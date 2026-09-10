---
title: Configuring Measure
description: Set up default template rules, the value job user, AI cost, and usage tracking so that the AI Control Tower can calculate value and cost.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
---

# Configuring Measure

Set up default template rules, the value job user, AI cost, and usage tracking so that the AI Control Tower can calculate value and cost.

## Recommended order

Configuration falls into two independent tracks that meet on the dashboard. Complete the Value track first, because cost figures are only meaningful once value is being calculated.

1.  Value: Configure default template rules, then assign the value job user. Publish at least one value template and map your AI systems to it.
2.  Cost: Configure the average hourly rate, add integrated vendor costs, add other vendor costs if you use any, and then review and submit. These four tasks are steps in one flow, so complete them in order.
3.  Dashboard: Set up usage tracking by user and department so that usage and cost can be attributed correctly.

**Important:**

Cost configuration can't be altered for past dates. Make sure you have the correct hourly and vendor rates before submitting, as any corrections will only apply to future dates.

## Configure value management

The following topics describe how to configure value management:

1.  Set up value template rules. Do one of the following:
    -   To use the out-of-the-box templates, review default value template rules.

        For more information, see [Review or create default template rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mv-review-default-templates.md).

    -   To build your own, create new value template rules.

        For more information, see [Create and publish a value template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mv-create-and-publish-a-value-template.md).

    -   To manage AI systems that don't have discovery integration, create and run manual value jobs.

        For more information, see [Create and run manual value jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mv-create-and-run-manual-value-jobs.md).

2.  Assign the value job user.

    For more information, see [Assign the value job user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mv-assign-the-value-job-user.md).

3.  Map an AI system to a value template.
4.  \(Conditional\) Set up the Multi-Instance Framework for value calculations

    For more information, see [Set up the Multi-Instance Framework for value calculations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mv-set-up-the-multi-instance-framework-for-value-calculations.md).

5.  Configure the average hourly rate for your organization.

    For more information, see [Configure average hourly rate for your organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mc-configure-the-average-hourly-rate-for-your-organization.md).

6.  Add and configure costs for integrated vendors.

    For more information, see [Add costs for integrated vendors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mc-add-and-configure-costs-for-integrated-vendors.md).

7.  Add and configure costs for non-integrated vendors.

    For more information, see [Add costs for other vendors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mc-add-and-configure-costs-for-non-integrated-vendors.md).

8.  Review and submit the cost configuration.

    For more information, see [Review and submit the cost configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mc-review-and-submit-the-cost-configuration.md).

9.  Set up usage tracking by user and department.

    For more information, see [Set up usage tracking by user and department](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/md-set-up-usage-tracking-by-user-and-department.md).


