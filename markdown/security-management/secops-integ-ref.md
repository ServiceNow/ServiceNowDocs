---
title: Security Operations Integration Reference
description: Developers and ServiceNow partners can use the information in this section to gain understanding of the under-the-hood functionality of third-party integrations, including development guidelines, integration capabilities, and workflows.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Operations common functionality, Security Operations]
---

# Security Operations Integration Reference

Developers and ServiceNow partners can use the information in this section to gain understanding of the under-the-hood functionality of third-party integrations, including development guidelines, integration capabilities, and workflows.

-   **[ServiceNow Security Operations integration development guidelines](../../security-operations-integrations/concept/c_IntegrationWritingGuidelines.md)**  
The ServiceNow platform provides several mechanisms for developing integrations with external systems. The ServiceNow Security Operations product suite adds integration capabilities intended to streamline the process of integrating with security-focused external systems.
-   **[Integrations Capabilities framework 2.0](../../security-incident-response/concept/cj-sir-capfmw-about.md#)**  
The new Integration Capabilities Framework 2.0 has been redesigned to enable implementation of integrations in a simple and consistent manner. This ensures a consistent experience for similar types of integrations \(for example: observable reputation lookup\).
-   **[REST APIs for third-party integration with Security Operations](../../security-operations-common/concept/third-party-script-integrations.md)**  
The Security Operations base system includes a series of scripted REST APIs that allow customers and partners to easily integrate with an existing Security Operations deployment. The APIs allow you to gather data from outside of your system \(for example, a Python script is used to receive data from VirusTotal\) and send it back to your instance.
-   **[Integration capabilities](../../security-operations-common/concept/integration-capabilities.md)**  
The Integration Capabilities framework provides a consistent architecture to support interoperability with third-party integrations. This abstracted interface and data model insulates integrations from changes to the core application and ensures a consistent experience for similar types of integrations.
-   **[Common Security Operations integration flows and orchestration activities](../../security-operations-common/concept/common-wf-activities.md)**  
Many of the flows associated with third-party integrations include the same activities. For example, activities for beginning and completing processing.

**Parent Topic:**[Security Operations common functionality](../../security-operations-common/concept/sec-ops-common-functionality.md)

