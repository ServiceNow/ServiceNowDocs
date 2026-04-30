---
title: Customer Service Management and the CSDM guidelines
description: CSM enables you to provide service and support for your external customers through communication channels such as the web, email, chat, telephone, and social media. The goal of this use case is to understand how CSM key entities work with the core CSDM framework.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Getting started with Customer Service Management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Customer Service Management and the CSDM guidelines

CSM enables you to provide service and support for your external customers through communication channels such as the web, email, chat, telephone, and social media. The goal of this use case is to understand how CSM key entities work with the core CSDM framework.

## CSM use case

CSM provides proactive customer service, decreases cost of service, and provides end-to-end visibility to both customer service and service delivery groups. For more information, see [Integrating with Service Portfolio Management](csm-spm-integration.md).

For information on setting up the data, see [Configure foundation data](../task/configure-csm-foundation-data.md).

## Results of the CSM use case

Understand the tables within the CSDM framework that are needed to support the following CSM functionality:

-   Service-aware Install Base
-   Proactive Customer Service Operations
-   Real Time Service Health and Outage Tracking
-   Contextual Service Catalog

The following sections include details of the activities needed for the use case.

See [Applying the CSDM guidelines to your product](https://www.servicenow.com/docs/access?context=use-cases&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information on Common Service Data Model use cases.

## CSM data model

CSM uses the following key entities to resolve complex end-to-end issues.

-   A **case** is the primary entity of CSM. CSM uses cases to track and resolve customer questions or issues.
-   Customer information is linked to a case using associated entities such as Accounts, Contacts, Consumers, Household, Products, and Service Contracts. This information provides the customer service agent the information necessary to resolve customer issues.
-   An **account** can be a customer account, a partner account, or both.
-   The **contact** is an employee of an account. A contact record stores information about a contact, such as the name, phone number, and email address. A contact can also have a user ID and can log in to the customer portal.
-   A **consumer** is a customer in the business-to-consumer \(B2C\) business model.
-   Household defines the consumers who constitute a household, and the relationships between household members.
-   Sold Product tracks the products or services sold to an account or consumer.
-   Install Base Items represent the instance of the product that has been configured for a customer.
-   Service Contract defines the type of support that customers receive. A contract can include an account and contact or a consumer and the specific assets that are covered. A contract can also include multiple service entitlements and SLAs.
-   Entitlement specifies the type of support that a customer receives as well as the supported communication channels.

