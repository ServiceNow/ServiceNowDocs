---
title: Modify the attributes and relationships required for application services
description: Modify the lists of attributes and relationships that are required when creating application services.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Application services, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Modify the attributes and relationships required for application services

Modify the lists of attributes and relationships that are required when creating application services.

## Before you begin

Role required: itil\_admin

## About this task

In application service settings, the lists of required attributes and required relationships determine which of those items are required when creating application services. By default, the list of required attributes contains the required **Name** and **Number** attributes. Also by default, no relationships are required.

You can choose from predefined lists of allowed required attributes and relationships. To change the requirement status of an attribute, remove it from or add it to the list of required attributes. You can also add **Business Application**, **Technical Service Offering**, or **Business Service Offering** to the list of required relationships.

## Procedure

1.  Navigate to **All** &gt; **CSDM** &gt; **Service Instance Settings**.

2.  Review the list of **Available** items in the Required attributes and Required relationships lists and then add items to the **Selected** list.

3.  Click **Save**.


## Result

Next time that you create an application service, the required attributes and relationships are visibly noted in the Basic Details section on the Create an Application Service page.

