---
title: Set up Total Rewards using Workday
description: Configure the Total Rewards templates by choosing plans, sections, and target audience. Display a customized Total Rewards widget to employees in the configured Service Portal.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring, HR Service Delivery Advanced Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Set up Total Rewards using Workday

Configure the Total Rewards templates by choosing plans, sections, and target audience. Display a customized Total Rewards widget to employees in the configured Service Portal.

## Before you begin

Role required: sn\_hr\_workday\_adv.admin

Configure the required reports for the Total Rewards functionality. See [Configure reports HR Service Delivery Advanced Integration with Workday](../concept/awd-config-re.md#).

## Procedure

1.  Set up plans to include in sections in Total Rewards Template.

    For more information, see [Set up plans for Total Rewards](total-rewards-plans-awd.md).

2.  Set up sections to include in Total Rewards Template.

    For more information, see [Set up sections for Total Rewards templates](total-rewards-config-awd.md).

3.  Set up Total Rewards template by choosing sections, and target audience.

    For more information, see [Set up a template for Total Rewards](total-rewards-tem-setup.md).


## What to do next

1.  Navigate to **Service Portal** &gt; **Service Portal Configuration** &gt; **Designer**. Display the Total Rewards view to employees by adding the **View Workday Total Rewards** widget to the required Service Portal.
2.  Configure the system property, **sn\_hr\_workday\_adv.workday\_total\_rewards.currency\_code**, which stores the currency code to call the Total Rewards RAAS \(Report As A Service\) based API. The default value of the property is **USD**.

