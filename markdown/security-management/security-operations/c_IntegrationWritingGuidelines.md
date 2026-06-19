---
title: ServiceNow Security Operations integration development guidelines
description: The ServiceNow platform provides several mechanisms for developing integrations with external systems. The ServiceNow Security Operations product suite adds integration capabilities intended to streamline the process of integrating with security-focused external systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-operations/c\_IntegrationWritingGuidelines.html
release: zurich
product: Security Operations
classification: security-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# ServiceNow Security Operations integration development guidelines

The ServiceNow platform provides several mechanisms for developing integrations with external systems. The ServiceNow Security Operations product suite adds integration capabilities intended to streamline the process of integrating with security-focused external systems.

Most of the concepts in this guide assume some familiarity with standard ServiceNow functionality. To integrate with the Security Operations suite, at a minimum, knowledge of the following ServiceNow concepts is required:

-   Script includes
-   Inbound/outbound web services
-   Data sources
-   Import sets
-   Transform maps

**Technology Partner Program**

Any requirements for application certification or guidelines given in the Technology Partner Program literature supersede any information in this guide. This guide is not a replacement for the Technology Partner Program literature and serves only as a supplement to existing documentation.

For more information, see [Technology Partner Program training course blog post](https://community.servicenow.com/community/develop/app-publisher/blog/2015/10/19/the-technology-partner-program-training-course).

-   **[Types of ServiceNow integrations provided](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/c_TypesOfIntegrationsProv.md)**  
The Security Operations applications \(Security Incident Response, Threat Intelligence, and Vulnerability Response\) can be seamlessly integrated with other ServiceNow applications to enhance their functionality.
-   **[Security Operations Integration Configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/third-party-integrations.md)**  
Many of the integrations included in the base system require little or no setup, and operate in the same way. Certain integrations, such as the Qualys Cloud Platform, however, require separate steps for setting up the integration. Others support different sets of scan and lookup types and different rate limits.
-   **[Tips for writing integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/c_BestPractisesIntegrations.md)**  
Avoid some of the pitfalls you can encounter when writing your own integrations by following these guidelines.
-   **[Integration troubleshooting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/c_IntegrationTroubleshooting.md)**  
These troubleshooting suggestions can help you resolve common issues you can encounter when setting up or running integrations.

**Parent Topic:**[Security Operations Integration Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/secops-integ-ref.md)

