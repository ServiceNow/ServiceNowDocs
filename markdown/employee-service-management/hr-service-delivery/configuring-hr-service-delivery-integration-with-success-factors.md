---
title: Configuring HR Service Delivery Integration with SuccessFactors
description: After you install the HR Service Delivery Integration with SuccessFactors, the services for SuccessFactors are automatically created in Enterprise Service Management Integrations Framework.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/hr-service-delivery/configuring-hr-service-delivery-integration-with-success-factors.html
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery Integration with SuccessFactors, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configuring HR Service Delivery Integration with SuccessFactors

After you install the HR Service Delivery Integration with SuccessFactors, the services for SuccessFactors are automatically created in Enterprise Service Management Integrations Framework.

## Before you begin

-   Role required: sn\_hr\_sf.admin
-   Activate HR Service Delivery Integration with SuccessFactors that automatically activates Enterprise Service Management Integrations Framework and SuccessFactors spoke.

## Procedure

1.  Allow RCAs manually.

    Allow the Restricted Caller Access records with Status = **Requested** and Source Scope = **Enterprise Service Management Integrations Framework** or **HR Service Delivery Integration with Successfactors**.

2.  For better performance, index the employee number field in the HR Profile table and index coalesce fields in [Use transform maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/use-transform-maps-sf.md).

    For more information, see create a table index.

3.  Set up SuccessFactors spoke.

    **Note:** To use HR Service Delivery Integration with SuccessFactors, ensure to set up the SuccessFactors spoke version 3.1.2

    For more information, see set up SuccessFactors Spoke.

4.  Configure integration source properties for [Source for HR Service Delivery Integration with SuccessFactors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/source-for-hrsd-successfactors.md).

5.  Activate and run the scheduled flow that synchronizes Worker profile information between SuccessFactors and ServiceNow HR Service Delivery periodically.

    For more information, see [Activating schedule flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/activating-schedule-flows-sf.md).


