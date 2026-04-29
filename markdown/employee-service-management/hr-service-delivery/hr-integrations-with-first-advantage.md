---
title: Integrating with the First Advantage service
description: The preconfigured First Advantage integration uses SOAP services to request background checks through the First Advantage service. You can use the preconfigured integration as-is or customize it to meet your needs.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [HR Integrations, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Integrating with the First Advantage service

The preconfigured First Advantage integration uses SOAP services to request background checks through the First Advantage service. You can use the preconfigured integration as-is or customize it to meet your needs.

**Important:** Integrating with the First Advantage service is being prepared for deprecation. It will be hidden and unavailable for activation from Zurich, but will continue to be supported till Brazil. If you have an active subscription, you can still activate the plugin by submitting a [plugin activation request](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/plugins/task/t_RequestAPlugin.html). For more details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

## First Advantage integration overview

The First Advantage integration is configured to request background checks as follows.

-   The HR agent creates a case to request a background check through the First Advantage service.
-   The First Advantage service evaluates the request to:
    -   Update the case with the background check applicant ID and status.
    -   Create a task, as well as send an email, for the employee to sign up and complete a background check application through the First Advantage website.
-   Once the employee completes the task, the First Advantage service performs the background check.
-   When the background check is complete, the First Advantage service updates the case with the background check status and details.

## First Advantage integration setup

To set up the First Advantage integration, you must provide the source credentials, verify the integration settings, and add the appropriate background check packages. Once the integration is complete, you can request background checks through the First Advantage service.

1.  [Provide source credentials for the First Advantage service](../task/hr-integrations-sources-first-advantage.md)  
Provide the source and SOAP credentials for the First Advantage service so that it can be accessed for integration.
2.  [Verify integration for the First Advantage service](../task/verify-base-inbound-integration-for-first-advantage.md)  
The integration is configured to push background check data between the HR service in HR Service Delivery and the First Advantage service. You can verify the preconfigured settings and determine whether they meet your needs or if further customization is required.
3.  [Add background check packages for the First Advantage](../task/background-check-package-for-first-advantage.md)  
Add one or more background check packages to your instance so they can be accessed when a request for a background check by First Advantage is made. For example, you can add a package for a background check only and a package for both a background check and drug screening.

**Parent Topic:**[HR Integrations](scoped-hr-third-party-integrations.md)

