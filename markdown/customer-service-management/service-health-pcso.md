---
title: Service health status for install base
description: View the real-time health status of a customer's install base. Correlate customer issues with the operational health of their install base to provide more informed responses to your customers.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integration with Event Management, Proactive Customer Service Operations, Configure Proactive Customer Service Operations, Extend capabilities, Configuring Customer Service Management, Customer Service Management]
---

# Service health status for install base

View the real-time health status of a customer's install base. Correlate customer issues with the operational health of their install base to provide more informed responses to your customers.

## Service health tracking overview

The integration between Customer Service Management and the Event Management console in IT Operations Management enables you to track the service health status of a customer's install base.

When an issue affects one or more install base items and an alert is created, the severity of the alert is calculated in Event Management. It is calculated according to alert impact calculation rules. Based on the severity of the alert, the service health status of each install base item is calculated. Customer service agents can view the service health status of install base items in an account or a case in Customer Service Management.

​For more information about how the severity of an alert is calculated, see [Alert impact calculation](https://www.servicenow.com/docs/access?context=c_EMImpactCalculation&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

To provide the service health status for an install base item in Customer Service Management, the following fields are mapped.

|Event Management \(em\_impact\_status table\)|Customer Service Management \(sn\_install\_base\_item table\)|
|---------------------------------------------|-------------------------------------------------------------|
|Business Service|Service Context|
|Element Identifier|Configuration Item|
|Severity|Health Status|

**Note:** The service health status is displayed only if the install base item has both a Configuration Item \(CI\) and a service context associated with it. Service context is the application service associated with the underlying CI for impact calculation in Event Management​. For more information about application services, see Lesson 2 of the [Event Management operator guide](https://www.servicenow.com/docs/access?context=operator-application-services&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

The service health status is displayed in Customer Service Management as follows.

|Severity of alert \(Event Management\)|Service health status on Account and Case forms \(Customer Service Management\)|
|--------------------------------------|-------------------------------------------------------------------------------|
|Critical|Critical: Resource is either not functional or critical problems are imminent.|
|Major|Major: Major functionality is severely impaired or performance has degraded.|
|Minor|Minor: Partial, non-critical loss of functionality or performance degradation occurred.|
|Warning|Warning: Attention is required, even though the resource is still functional.|
|Info|Normal: No severity. An alert is created. The resource is still functional.|
|Clear|Normal|
|Empty/Null|Not Available|

For more information about alert severity, see Lesson 1 of the [Event Management operator guide](https://www.servicenow.com/docs/access?context=operator-application-services&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

## Roles

As a system administrator, configure form views to add the **Service Context**, **Health Status**, and **Health Status Last Updated** fields to the relevant forms.

As a customer service agent, view the service health status of install base items on the Account or Case form.

## Activation information

This feature requires the Proactive Customer Service Operations with Event Management plugin \(com.snc.proactive\_cs\_itom\).

**Related topics**  


[Integration with Event Management](pcso-event-management.md)

[Configure form views for Proactive Customer Service Operations](../task/configure-form-views.md)

[Track the service health of install base items in Agent Workspace](../task/service-health-tracking-csm.md)

