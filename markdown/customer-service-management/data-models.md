---
title: Data models
description: Understand how Customer Service Management \(CSM\) structures customer, account, and service data as reusable models. These models define your customers, their assets, and service organizations. They form the common data foundation for CSM case management and connected applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/data-models.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Set up your environment, Configure, Customer Service Management]
---

# Data models

Understand how Customer Service Management \(CSM\) structures customer, account, and service data as reusable models. These models define your customers, their assets, and service organizations. They form the common data foundation for CSM case management and connected applications.

## Overview of CSM data model

CSM doesn't scatter customer data across separate stores. It builds on one shared set of data models. A company, a person, a product, or a service organization is defined once and used across every CSM workflow.

The Customer Data Foundation models describe the customer side of the picture. They cover accounts and contacts for business-to-business \(B2B\) service, consumers and households for business-to-consumer \(B2C\) service, and the combined business-to-business-to-consumer \(B2B2C\) structures. They also cover customer addresses and the relationships and access rules that connect them. Whereas the models describe the service side. They cover service organizations, business locations, and service offerings, used when a case is serviced through or on behalf of another organization.

Together these models give every case a consistent answer to three questions: who the customer is, what they own, and which organization services them. Because the data is shared rather than duplicated, a record created once is available wherever CSM needs it. The same foundation is reused by applications such as Field Service Management and Sales Customer Relationship Management, without a separate copy or sync.

**Related topics**  


[customer-data-foundation]

[Configure Service Model Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configure-industry-data-model.md)

[Configure customer data models for B2B2C](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configure-customer-data-model-b2b2c.md)

[Customer Service Management and the CSDM guidelines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-use-case-product-view.md)

