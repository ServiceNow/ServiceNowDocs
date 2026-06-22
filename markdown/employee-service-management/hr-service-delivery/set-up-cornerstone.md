---
title: Setting up HR Service Delivery Integration with Cornerstone OnDemand
description: Understand how to set up the HR Service Delivery Integration with Cornerstone OnDemand application for pulling learning courses from the Cornerstone OnDemand system into the ServiceNow system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/hr-service-delivery/set-up-cornerstone.html
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery Integration with Cornerstone OnDemand, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Setting up HR Service Delivery Integration with Cornerstone OnDemand

Understand how to set up the HR Service Delivery Integration with Cornerstone OnDemand application for pulling learning courses from the Cornerstone OnDemand system into the ServiceNow system.

## Before you begin

-   Role required: sn\_hr\_cornerstone.admin
-   Activate the Human Resources Scoped App: Core plugin \[com.sn\_hr\_core\].
-   Activate the HR Service Delivery Integration with Cornerstone OnDemand plugin \[sn\_hr\_cornerstone\] from ServiceNow Store. This plugin activates Cornerstone spoke in IntegrationHub and HR Service Delivery Integrations Framework plugin \[sn\_hr\_integr\_fw\].

## Procedure

1.  Set up the Cornerstone spoke in IntegrationHub.

    For more information, refer to the [Cornerstone spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/integration-hub/cornerstone-spoke.md) documentation.

2.  Configure the URL prefix in the Cornerstone source record in HR Service Delivery Integration with Cornerstone OnDemand.

    For more information, refer to [Use deep link for HR Service Delivery Integration with Cornerstone OnDemand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/generate-deep-link-cor.md).

    **Important:** Once you have activated the necessary plugins and set up the Cornerstone spoke, HR Integration Services \(for Cornerstone OnDemand application\) are automatically created. For more information, refer to [HR Integration Services for HR Service Delivery Integration with Cornerstone OnDemand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/cornerstone-hr-service.md).

3.  Configure the flow for HR Service Delivery Integration with Cornerstone OnDemand.

    For more information, refer to [Configure the flow for HR Service Delivery Integration with Cornerstone OnDemand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/schedule-job-hrint.md).


