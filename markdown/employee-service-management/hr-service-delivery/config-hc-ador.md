---
title: Configure holiday calendars in HR Service Delivery Advanced Integration with Oracle HCM
description: Pull holiday calendars from the Oracle HCM system into a ServiceNow application. Display applicable holiday calendars to employees in the configured Service Portal.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery Advanced Integration with Oracle HCM, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure holiday calendars in HR Service Delivery Advanced Integration with Oracle HCM

Pull holiday calendars from the Oracle HCM system into a ServiceNow application. Display applicable holiday calendars to employees in the configured Service Portal.

## Before you begin

Role required: sn\_hr\_oracle\_adv.admin

## Procedure

1.  Create the Holiday Calendar BI report in the Oracle HCM system.

    For more details, refer to this [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0999535).

2.  To run the View Holiday Calendar widget successfully, configure BI report and Connection &amp; Credential Aliases in Oracle Cloud HCM Spoke.

    For more information, see set up [Oracle HCM Cloud spoke](https://www.servicenow.com/docs/access?context=setup-oracle-hcm&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

3.  Navigate to **Oracle Advanced Use Cases** &gt; **Holiday Calendar**.

4.  Click **Get Holiday Calendars**.

    All the records starting from current year until the next available calendar years are pulled from Oracle HCM system and stored in the Holiday Calendar \[sn\_hr\_oracle\_adv\_holiday\_calendar\] table.


## What to do next

An employee can add the View Holiday Calendar widget to any ServiceNow page. An employee will not be able to view this widget if the Person ID \(Correlation\_ID\) is missing in the HR profile \[sn\_hr\_core\_profile\] table.

