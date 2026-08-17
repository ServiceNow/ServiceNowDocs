---
title: External Organization as a fulfiller
description: External Organization \(formerly External business location \(EBL\)\) as a fulfiller enables partners, external agencies, and franchises to fulfill customer cases. You can use this capability to maintain consistent customer experiences across both internal and external organizations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/ebl-as-a-fulfiller.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Cases, Overview, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# External Organization as a fulfiller

External Organization \(formerly External business location \(EBL\)\) as a fulfiller enables partners, external agencies, and franchises to fulfill customer cases. You can use this capability to maintain consistent customer experiences across both internal and external organizations.

**Important:** Some table and field labels have been changed across recent releases. For a mapping of former labels to current labels, see [Service Model Foundation renamed Entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/renamed-entities.md).

## Overview of external organization

In the past, only location staff at internal organizations could resolve customer-related cases through both platform and workspace. External staff could only create cases from the business organization support portal \(formerly business location service portal \(BLSP\)\) but couldn't resolve them for the business organizations \(formerly business locations\). By using external organization as a fulfiller,

-   external location agents having svc\_location\_agent and snc\_external roles can access the platform to create and resolve cases, similar to internal location agents.
-   external location consumer agents \(having sn\_customerservice.svc\_location\_consumer\_agent and snc\_external roles\) can access the platform to create and resolve consumer cases, similar to internal location consumer agents.

You can activate this functionality by enabling the business location \(com.snc.business\_location\) plugin.

## Use case for external location agent

For example, the financial institution agencies perform various activities, from policy issuance to claims processing. These activities include underwriting, reviewing claims, and helping customers in claims submission. As most of these tasks are fulfillment activities currently performed by external members or third parties. Now, by using External Organization as a fulfiller capability, external location agents in these agencies can efficiently manage and resolve cases.

## Use case for external location consumer agent

For example, hotels perform various activities, from guest check-in to billing and refund resolution. These activities include reviewing billed charges, processing refund requests, and helping guests resolve billing discrepancies. As most of these tasks are fulfillment activities currently performed by staff local to that specific hotel property. Now, by using External Location Consumer Agent as a fulfiller, hotel staff can efficiently manage and resolve refund cases raised by guests associated with that location — without escalating to a central organization.

**Related topics**  


[Access limitations for external location agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/access-limitations-for-ext-loc-agent.md)

