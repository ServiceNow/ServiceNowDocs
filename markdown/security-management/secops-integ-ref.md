---
title: Security Operations Integration Reference
description: Developers and ServiceNow partners can use the information in this section to gain understanding of the under-the-hood functionality of third-party integrations, including development guidelines, integration capabilities, and workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/secops-integ-ref.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security Operations common functionality, Security Operations]
---

# Security Operations Integration Reference

Developers and ServiceNow partners can use the information in this section to gain understanding of the under-the-hood functionality of third-party integrations, including development guidelines, integration capabilities, and workflows.

-   **[ServiceNow Security Operations integration development guidelines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/c_IntegrationWritingGuidelines.md)**  
The ServiceNow platform provides several mechanisms for developing integrations with external systems. The ServiceNow Security Operations product suite adds integration capabilities intended to streamline the process of integrating with security-focused external systems.
-   **[Integrations Capabilities framework 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/cj-sir-capfmw-about.md)**  
The new Integration Capabilities Framework 2.0 has been redesigned to enable implementation of integrations in a simple and consistent manner. This ensures a consistent experience for similar types of integrations \(for example: observable reputation lookup\).
-   **[REST APIs for third-party integration with Security Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/third-party-script-integrations.md)**  
The Security Operations base system includes a series of scripted REST APIs that allow customers and partners to easily integrate with an existing Security Operations deployment. The APIs allow you to gather data from outside of your system \(for example, a Python script is used to receive data from VirusTotal\) and send it back to your instance.
-   **[Integration capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/integration-capabilities.md)**  
The Integration Capabilities framework provides a consistent architecture to support interoperability with third-party integrations. This abstracted interface and data model insulates integrations from changes to the core application and ensures a consistent experience for similar types of integrations.
-   **[Common Security Operations integration flows and orchestration activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/common-wf-activities.md)**  
Many of the flows associated with third-party integrations include the same activities. For example, activities for beginning and completing processing.

**Parent Topic:**[Security Operations common functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sec-ops-common-functionality.md)

