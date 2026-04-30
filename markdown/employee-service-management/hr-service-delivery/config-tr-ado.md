---
title: Configure total rewards in HR Service Delivery Advanced Integration with Oracle HCM
description: Complete the set up to display Oracle total rewards to employees in the configured portal in the ServiceNow instance.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery Advanced Integration with Oracle HCM, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure total rewards in HR Service Delivery Advanced Integration with Oracle HCM

Complete the set up to display Oracle total rewards to employees in the configured portal in the ServiceNow instance.

## Before you begin

Role required: sn\_hr\_oracle\_adv.admin

## Procedure

1.  Create the total rewards BI report in the Oracle HCM system.

    For more details, refer to this [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0999529).

2.  Add the BI report path in the Oracle HCM system.

    This is required for the Get Total Rewards Action to pull Oracle HCM total rewards information into the ServiceNow instance. For more information, see set up [Oracle HCM Cloud spoke](https://www.servicenow.com/docs/access?context=setup-oracle-hcm&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

3.  Click **Submit**.


## What to do next

An employee can add the View Oracle Total Rewards widget to any ServiceNow page. An employee will not be able to view this widget if the Person ID \(Correlation\_ID\) is missing in the HR profile \[sn\_hr\_core\_profile\] table.

