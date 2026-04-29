---
title: Domain separation and Predictive Intelligence
description: Domain separation is supported in the Predictive Intelligence application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Predictive Intelligence references, Predictive Intelligence, Enable AI experiences]
---

# Domain separation and Predictive Intelligence

Domain separation is supported in the Predictive Intelligence application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Overview of domain separation and Predictive Intelligence

With Predictive Intelligence, you can create machine learning solutions using historic datasets. A machine learning solution is created and trained in the global domain, and that solution's predictions can be applied in any domain on the instance.

Similarity solutions are domain-aware when applied in your forms and flows, so records from other domains on the instance are not displayed to users. For more information, see KB article [Similarity prediction behavior in domain separated environment](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2035643) on Now Support.

## How domain separation works in Predictive Intelligence

An instance owner can train a machine learning \(ML\) solution for each domain by creating a solution definition for each domain and training those solutions. In this way each solution uses data specific to the corresponding domain.

-   Data can be domain separated
-   Domain column is present for base system application tables
-   Domain-specific configuration is managed by instance owner
-   Tenant domains can manage their own application data
-   Application properties are domain-aware when needed

**Parent Topic:**[Predictive Intelligence references](../reference/reference-predictive-intelligence.md)

**Related topics**  


[Data Encryption in Predictive Intelligence](../reference/predictive-intelligence-encryption.md)

[Predictive Intelligence language support](predictive-intelligence-localization.md)

[Predictive Intelligence properties](../reference/predictive-intelligence-properties.md)

[Predictive Intelligence roles](../reference/predictive-intelligence-roles.md#)

[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US)

