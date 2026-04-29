---
title: Domain Separation guidelines for HR Multi Instance Integration
description: Review these domain separation guidelines before using the HR Multi Instance Integration application.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, HR Multi Instance Integration, HR Service Delivery, Employee Service Management]
---

# Domain Separation guidelines for HR Multi Instance Integration

Review these domain separation guidelines before using the HR Multi Instance Integration application.

**Note:**

-   Only Basic Domain separation \(only data separation not process separation\) is supported in HR Multi Instance Integration.
-   Domain Separation is not mandatory for HR Multi Instance Integration. You can omit this section, if your organization doesn’t require domain separation.

## Guidelines for HR Multi Instance Integration for Consumer

Install the Domain Separation plugin \[com.snc.pa.domain\_support\] and Catalog Domain Separation plugin \[com.glideapp.servicecatalog.domain\_separation\].

If you want the remote catalogs and provider tasks to be accessible by all employees across domains, maintain the provider connection and provider company in global.

If you want the remote catalogs and provider tasks to be accessible by specific domain users, maintain the provider connection and provider company in the required domain.

## Guidelines for HR Multi Instance Integration for Provider

To enable domain separation in a provider instance, review the following guidelines:

-   Install the Domain Separation plugin \[com.snc.pa.domain\_support\] and Catalog Domain Separation plugin \[com.glideapp.servicecatalog.domain\_separation\].

    **Note:** Define domains if you want to enable domain separation for each consumer, otherwise, omit the domain separation-specific setup.

-   Associate a consumer company to a domain. Each consumer’s Service Bridge connection record, consumer company, external system integrations connections, external system integration-related flows, and each consumer users must reside in the required domain \(if domain separation is enabled\).
-   Associate the correct consumer company to users who are imported from external systems. The domain of a user is derived from a company record.
-   Maintain the HR services and remote catalogs in global if the same service is used across all consumers. The HR services and HR catalogs can be maintained in a consumer-specific domain by creating the consumer-specific HR service and remote catalogs.

    **Note:** Provider tasks and remote HR cases reside in a consumer-specific domain when domain separation is enabled. The domain of an HR case is derived from the Service Bridge integrator-user's company domain for that consumer.


