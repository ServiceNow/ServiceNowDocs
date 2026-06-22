---
title: Activate HR Service Delivery for mobile
description: Activate the HR Service Delivery for mobile plugin \(sn\_hr\_mobile\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/hr-service-delivery-for-mobile/activate-mobile-employee-experience-for-hr-service-delivery.html
release: zurich
product: HR Service Delivery for mobile
classification: hr-service-delivery-for-mobile
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery for mobile, HR Service Delivery, Employee Service Management]
---

# Activate HR Service Delivery for mobile

Activate the HR Service Delivery for mobile plugin \(sn\_hr\_mobile\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

HR Service Delivery for mobile activates these related plugins if they are not already active:

-   [Now Mobile app \[sn\_me\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-mobile-employee-experience/mobile-employee-experience.md)
-   Surveys for mobile \[com.sn\_msc\]

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/find-components.md).


-   **[Components installed with Now Mobile for HR Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery-for-mobile/components-installed-with-now-mobile-hr.md)**  
Several types of components install with the activation of the Now Mobile for HR Service Delivery plugin, including tables and user roles.
-   **[Configurations for the Now Mobile app for HR Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery-for-mobile/hr-mobile-configuration.md)**  
Configure options for the Now Mobile app for HR Service Delivery.

**Parent Topic:**[HR Service Delivery for mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery-for-mobile/mobile-employee-experience-for-hr-service-delivery.md)

