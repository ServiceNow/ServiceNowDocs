---
title: Automatically create universal request from an inbound email
description: Universal requests can be automatically created from the information received by emails. The auto-creation of universal requests enables faster response time and quicker resolution for employees compared to the agents manually creating requests from emails.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Unified ticket experience setting, Configure service to use Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Automatically create universal request from an inbound email

Universal requests can be automatically created from the information received by emails. The auto-creation of universal requests enables faster response time and quicker resolution for employees compared to the agents manually creating requests from emails.

Configure the email IDs in the **General email address for Universal Requests** \(sn\_uni\_req.ur\_email\) property. For more information, see [Universal Request properties](../reference/ur-properties.md). By default, an email sent to these configured mail IDs will automatically create a universal request. Incoming emails marked with high importance will create universal requests with high priority \(Priority 1\).

By default, the solution definition is configured and the predictive model is auto-trained when the following conditions are met.

-   The Universal Request \(com.snc.universal\_request\) plugin is installed.
-   The Predictive Intelligence \(com.glide.platform\_ml\) plugin is installed.
-   The Predictive Intelligence for Universal Request plugin \(com.snc.universal\_request.ml\) plugin is installed. This plugin requires a separate subscription and must be activated by a ServiceNow personnel.

On instances where Predictive Intelligence for Universal Request is active, the following solution definition and business rule are available:

|Definition|Description|
|----------|-----------|
|Universal Request Categorization|Predicts the assignment group from the short description and description of a Universal Request and also creates service level tickets that will be associated with the universal request.|

|Business rule|Table|Description|
|-------------|-----|-----------|
|Predict assignment group of UR|Universal Request \[universal\_request\]|Predicts the assignment group from the short description and description of a Universal Request.|

**Parent Topic:**[Unified ticket experience setting](unified-ticket-experience.md)

**Related topics**  


[Create universal request automatically for department tickets via other channels](../task/autocreate-ur-from-interactionrecord-WS.md)

[Email notification preferences for your service](ur-customize-email-notifcations.md)

[Configure a catalog item or record producer to create a universal request](../../service-catalog-management/task/create-ur-recordproducer.md)

