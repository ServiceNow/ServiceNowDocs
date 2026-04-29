---
title: Microsoft Entra ID integration for new hire onboarding
description: Automatically provision relevant applications for new hires as part of the onboarding process with the Microsoft Entra ID integration. This integration requires the Microsoft Entra ID spoke in IntegrationHub, and is configured to work with the lifecycle event for new hire onboarding that is included as demo data with the Human Resources Scoped App: Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin.
locale: en-US
release: australia
product: Employee Journey Management
classification: employee-journey-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Lifecyle events for enterprise integrations, Lifecyle events for enterprise, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Microsoft Entra ID integration for new hire onboarding

Automatically provision relevant applications for new hires as part of the onboarding process with the Microsoft Entra ID integration. This integration requires the Microsoft Entra ID spoke in IntegrationHub, and is configured to work with the lifecycle event for new hire onboarding that is included as demo data with the Human Resources Scoped App: Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin.

## Setting up the Microsoft Entra ID integration

To set up the Microsoft Entra ID integration for new hire onboarding, you must first set up the Microsoft Entra ID spoke, next configure the remote directory sync to fetch the groups into your instance, and last configure the relevant business roles. For details on how to set up the integration, see [Set up the Microsoft Entra ID integration for new hire onboarding](../task/set-up-microsoft-azure-ad-integration-for-new-hire-onboarding.md).

## Using the Microsoft Entra ID integration with new hire onboarding

Once the integration is set up, you can use the it with new hire onboarding. The following components are included in the demo data for your use and example.

**Note:** The lifecycle event for new hire onboarding is included as demo data with the Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin.

|Component|Name|
|---------|----|
|Lifecycle event activity|Account and Application Access \(in the Day One activity set\)|
|HR task template|Groups Assignment for New Hires|
|Catalog item|Assign business roles to new hire|

## How the application provisioning works

The application provisioning process works as follows. When an onboarding case is created, the hiring manager receives a task to assign business roles for the new hire. Once assigned, IT then receives a request to supervise the provisioning of those applications. When the provisioning is complete, the new hire should see their applications in the Microsoft Entra ID service.

**Important:** New hires must have a user record in the Microsoft Entra ID system in order for their applications to be provisioned to them.

-   **[Set up the Microsoft Entra ID integration for new hire onboarding](../task/set-up-microsoft-azure-ad-integration-for-new-hire-onboarding.md)**  
To set up the Microsoft Entra ID integration for new hire onboarding, you must first set up the Microsoft Entra ID spoke, next configure the remote directory sync to fetch the groups into your instance, and last configure the required business roles.

**Parent Topic:**[Lifecyle events for enterprise integrations](onbrd-trans-integrations.md)

