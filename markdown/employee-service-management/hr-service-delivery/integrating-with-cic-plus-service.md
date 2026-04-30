---
title: Integrating with the CIC Plus service
description: Integrate with the CIC Plus service so that you can enable US-based new hires to provide relevant tax information as part of the onboarding process.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [HR Integrations, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Integrating with the CIC Plus service

Integrate with the CIC Plus service so that you can enable US-based new hires to provide relevant tax information as part of the onboarding process.

This integration assumes you are already integrated with a third-party identity provider \(IDP\) service, and is configured to work with the lifecycle event for new hire onboarding that is included as demo data with the Human Resources Scoped App: Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin.

## Setting up the CIC Plus integration

To set up the CIC Plus integration, you must configure a SAML connection between your third-party identity provider \(IDP\) and CIC Plus accounts. Your CIC Plus partner must then set up your account to get employee profiles for US-based employees through the get\_usa\_employee\_profile REST endpoint, as well as verify that the callback is properly configured. Finally, you must configure the source credentials to include the login URL of the identity provider service you are using with the CIC Plus integration. For details on how to set up the CIC Plus integration, see [Set up the CIC Plus integration](../task/set-up-cic-plus-integration.md).

## Using the CIC Plus integration with new hire onboarding

Once the integration is set up, you can use the CIC Plus service with new hire onboarding. The following components are included in the demo data for your use and example.

**Note:** The lifecycle event for new hire onboarding is included as demo data with the Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin.

|Component|Name|
|---------|----|
|Lifecycle event activity|Complete Tax Forms \(in the Day One activity set\)|
|HR service|Complete Tax Forms through CIC Plus|
|HR case template|Complete Tax Forms through CIC Plus|

## How the CIC Plus integration works

The CIC Plus integration works as follows. Your HR management system \(HRMS\) pushes employee information to your IDP and ServiceNow AI Platform systems. The CIC Plus integration then invokes the get\_usa\_employee\_profile REST endpoint to fetch employee information. When a user opens an assigned task and clicks on the link to connect to the CIC Plus service, the CIC Plus integration authenticates the user through a SAML identification via your IDP service. After the user completes the required tax forms, the status is pushed back to the ServiceNow AI Platform system and the employee task is automatically closed.

![CIC Plus integration setup.](../image/cic-plus-integration.png)

