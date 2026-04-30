---
title: Integrating with the Sterling Talent Solutions service
description: The preconfigured Sterling Talent Solutions integration uses REST services to request background checks through the Sterling service. You can use the preconfigured integration as-is or customize it to meet your needs.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [HR Integrations, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Integrating with the Sterling Talent Solutions service

The preconfigured Sterling Talent Solutions integration uses REST services to request background checks through the Sterling service. You can use the preconfigured integration as-is or customize it to meet your needs.

**Important:** Integrating with the Sterling Talent Solutions service is being prepared for deprecation. It will be hidden and unavailable for activation from Zurich, but will continue to be supported till Brazil. If you have an active subscription, you can still activate the plugin by submitting a [plugin activation request](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/plugins/task/t_RequestAPlugin.html). For more details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

## Sterling integration overview

The Sterling integration is configured to request background checks as follows.

-   The HR agent creates a case to request a background check through the Sterling service.
-   The Sterling service evaluates the request to:
    -   Update the case with the background check order ID.
    -   Send an email to the employee with a link to sign up and complete a background check application through the Sterling website.
-   Once the employee completes the background check application, the Sterling service performs the background check.
-   When the background check is complete, the Sterling service will update the case with the background check status and details.

## Sterling integration setup

To set up the Sterling integration, you must provide the source credentials, verify the integration settings, and add the appropriate background check packages. Once the integration is complete, you can request background checks through the Sterling service.

1.  [Provide source credentials for the Sterling service](../task/hr-integrations-sources-sterling.md)  
Provide the source and REST credentials for the Sterling service so that it can be accessed for integration.
2.  [Verify integration for the Sterling service](../task/verify-base-integration-for-sterling.md)  
The integration is configured to push background check data between the HR service in HR Service Delivery and the Sterling service. You can verify the preconfigured settings and determine whether they meet your needs or if further customization is required.
3.  [Add background check packages for the Sterling service](../task/background-check-package-for-sterling.md)  
Add one or more background check packages to your instance so they can be accessed when a request for a background check by Sterling is made. For example, you can add a package for a background check only and a package for both a background check and drug screening.

**Parent Topic:**[HR Integrations](scoped-hr-third-party-integrations.md)

