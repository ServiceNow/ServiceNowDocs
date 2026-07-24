---
title: Service definitions in Retail
description: A service definition describes a service that a retail organization offers to support its stores or customers. Service definitions build on case types to encapsulate different types of request and fulfillment processes within a single case type, without creating a new table for every variation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-retail-service-definitions.html
release: australia
topic_type: concept
last_updated: "2026-06-28"
reading_time_minutes: 1
keywords: [service definitions, retail service definitions, case type service definition]
breadcrumb: [Retail case types, Explore, Retail]
---

# Service definitions in Retail

A service definition describes a service that a retail organization offers to support its stores or customers. Service definitions build on case types to encapsulate different types of request and fulfillment processes within a single case type, without creating a new table for every variation.

Defining the services a retail service organization delivers is a foundational component of every Retail implementation. Without service definitions, the processes service definitions are meant to reflect are often incorrectly modeled in the category and subcategory field structures of cases.

## Why service definitions matter

Categories and subcategories track the long-term root cause of cases—the why behind an issue. Without service definitions, category and subcategory values are commonly used to capture both the service being requested \(the what\) and the reason for the case \(the why\). This leads to category sprawl and reduced data quality because the category structure must serve two purposes.

By using service definitions to identify the requested service, category and subcategory values can focus solely on capturing the root cause of the case. This separation produces cleaner reporting data and makes it easier to identify trends over time.

## Service definitions versus case types

Use a service definition when different work types share the same required attributes and automations within a single case type. Create a new case case type when the process requires fundamentally different fields, state models, or automation logic. For a full decision framework, see [Extending the Retail base case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-extending-retail-base-case.md).

**Related topics**  


[Service definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-service-definitions.md)

[Create a service definition for multi-store cases in Retail Task Management Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/legacy-retail-task-management/rahi-retail-create-service-definition.md)

