---
title: Configuring HR Service Delivery with Ultimate Kronos Group
description: Set up the HR Service Delivery with Ultimate Kronos Group application to start pulling information, such as accrual balances and shifts from the Ultimate Kronos Group application into a ServiceNow application.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery with Ultimate Kronos Group, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configuring HR Service Delivery with Ultimate Kronos Group

Set up the HR Service Delivery with Ultimate Kronos Group application to start pulling information, such as accrual balances and shifts from the Ultimate Kronos Group application into a ServiceNow application.

## Before you begin

Role required: sn\_hr\_core.admin

Activate the HR Service Delivery Integration with Ultimate Kronos Group \[sn\_hr\_ukg\] application, which automatically activates the following plugins and spoke:

-   Glide Virtual Agent \[com.glide.cs.chatbot\]
-   Human Resources Scoped App: Core \[com.sn\_hr\_core\]
-   Employee Service Center \[com.sn\_hr\_service\_portal\]
-   Virtual Agent Service Portal Widgets \[com.glide.va.sp\_widgets\]
-   NLU Workbench \[com.snc.nlu\_studio\]
-   Predictive Intelligence \[com.glide.platform\_ml\]
-   UKG spoke

## Procedure

1.  Integrate your Ultimate Kronos Group application with your ServiceNow instance.

    Register an OAuth application in the Ultimate Kronos Group application and authenticate requests from ServiceNow. For more information, see [Set up the UKG spoke](https://www.servicenow.com/docs/access?context=setup-kronos&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

2.  Complete the one time set up of loading accrual codes from the Ultimate Kronos Group application into ServiceNow.

    For more information, see [Set up accrual codes](accrual-type-ukg.md).

3.  The **Person number** field in Ultimate Kronos Group application should match the **Employee number** field in the ServiceNow User table.

    If the **Person number** field in Ultimate Kronos Group application matches with some other field in the ServiceNow User table, you must override the getPersonNumberBySysID method in HRKronosUtils script.


