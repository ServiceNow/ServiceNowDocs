---
title: Configuring HR Service Delivery Integration with SuccessFactors
description: After you install the HR Service Delivery Integration with SuccessFactors, the services for SuccessFactors are automatically created in Enterprise Service Management Integrations Framework.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery Integration with SuccessFactors, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configuring HR Service Delivery Integration with SuccessFactors

After you install the HR Service Delivery Integration with SuccessFactors, the services for SuccessFactors are automatically created in Enterprise Service Management Integrations Framework.

## Before you begin

-   Role required: sn\_hr\_sf.admin
-   Activate HR Service Delivery Integration with SuccessFactors that automatically activates Enterprise Service Management Integrations Framework and SuccessFactors spoke.

## Procedure

1.  Allow RCAs manually.

    Allow the Restricted Caller Access records with Status = **Requested** and Source Scope = **Enterprise Service Management Integrations Framework** or **HR Service Delivery Integration with Successfactors**.

2.  For better performance, index the employee number field in the HR Profile table and index coalesce fields in [Use transform maps](../reference/use-transform-maps-sf.md).

    For more information, see [create a table index](https://www.servicenow.com/docs/access?context=t_CreateCustomIndex&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

3.  Set up SuccessFactors spoke.

    **Note:** To use HR Service Delivery Integration with SuccessFactors, ensure to set up the SuccessFactors spoke version 3.1.2

    For more information, see set up [SuccessFactors Spoke](https://www.servicenow.com/docs/access?context=successfactors-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

4.  Configure integration source properties for [Source for HR Service Delivery Integration with SuccessFactors](../reference/source-for-hrsd-successfactors.md).

5.  Activate and run the scheduled flow that synchronizes Worker profile information between SuccessFactors and ServiceNow HR Service Delivery periodically.

    For more information, see [Activating schedule flows](activating-schedule-flows-sf.md).


