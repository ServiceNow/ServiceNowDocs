---
title: Sailpoint integration for new hire onboarding
description: Provide relevant applications for new hires automatically as part of the onboarding process with the Sailpoint integration.
locale: en-US
release: zurich
product: Employee Journey Management
classification: employee-journey-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate, Lifecyle events for enterprise, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Sailpoint integration for new hire onboarding

Provide relevant applications for new hires automatically as part of the onboarding process with the Sailpoint integration.

This integration requires the Sailpoint IdentityIQ for Service Catalog v2 app from the ServiceNow Store, and is configured to work with the lifecycle event for new hire onboarding that is included as demo data with the Human Resources Scoped App: Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin.

## Setting up the Sailpoint integration

To set up the Sailpoint integration for new hire onboarding, you must install the Sailpoint IdentityIQ for Service Catalog v2 app from the ServiceNow Store. For the installation guide and further information, see [SailPoint IdentityIQ for Service Catalog v2](https://store.servicenow.com/sn_appstore_store.do#!/store/application/c4af6dafdbf73300f931fe1b68961952/2.0.10).

**Note:** Make sure to use version 2.0.10 or later.

## Using the Sailpoint integration with new hire onboarding

Once the integration is set up, you can use it with new hire onboarding. The following components are included in the demo data for your use and example.

**Note:** The lifecycle event for new hire onboarding is included as demo data with the Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin.

|Component|Name|
|---------|----|
|Lifecycle event activity|Account and Application Access in Sailpoint \(in the Day One activity set\)|
|HR task template|Assign Roles in Sailpoint|

## How the application provisioning works

The application provisioning process works as follows. When an onboarding case is created, the hiring manager receives a task to assign roles and entitlements for the new hire. The hiring manager must then manually complete the task. Once assigned, IT then receives a request to supervise the provisioning of those applications. When the provisioning is complete, the new hire should see their applications in the Sailpoint service.

**Important:** New hires must have a user record in the Sailpoint system in order for their applications to be provisioned to them.

![Application provisioning process for the Sailpoint integration for new hire onboarding.](../image/sailpoint-integration-for-new-hire-onboarding.png)

**Parent Topic:**[Lifecyle events for enterprise integrations](onbrd-trans-integrations.md)

