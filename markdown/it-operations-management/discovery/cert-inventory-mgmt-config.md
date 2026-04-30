---
title: Configuring Certificate Inventory and Management
description: Establish a streamlined process for gaining insights into Certificate Inventory Management, covering key aspects like certificate discovery, bulk upload functionality, maintenance of certificate chain relationships, configuration of Credential Identifiers, customization of the system, creation of new/renewal requests, archiving tasks, automation of TLS certificate management, integration with Event Management, Slack notifications for alerts, and leveraging cert-Manager for efficient certificate generation.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Certificate Inventory and Management, Discovery, ITOM Visibility, IT Operations Management]
---

# Configuring Certificate Inventory and Management

Establish a streamlined process for gaining insights into Certificate Inventory Management, covering key aspects like certificate discovery, bulk upload functionality, maintenance of certificate chain relationships, configuration of Credential Identifiers, customization of the system, creation of new/renewal requests, archiving tasks, automation of TLS certificate management, integration with Event Management, Slack notifications for alerts, and leveraging cert-Manager for efficient certificate generation.

## Configuration overview

Before using Certificate Inventory and Management, it is crucial to set up the necessary plugins, ensure activation, upgrade your instance to the latest version, and download the Certificate Inventory and Management application from ServiceNow Store. For additional details, see [Get started with Certificate Inventory and Management](../task/get-started-cert-inventory-mgmt.md).

After the prerequisites are met, you can proceed with the following tasks.

|Task|Description|
|----|-----------|
|[Visibility to TLS certificates](run-cert-discovery.md)|Establish an efficient Certificate Inventory Management system by configuring certificate discovery, enabling bulk certificate uploads, managing chain relationships, configuring secure access, and customizing the system to meet specific organizational needs.|
|[Manual flow for certificate requests](manual-cert-requests.md)|Enable the creation of new certificate requests or certificate renewals within the system, adhering to defined policies. Implement a process to archive completed certificate tasks, maintaining a historical record for auditing and compliance purposes.|
|[Automated certificate management for TLS certificates](automated-cert-requests.md)|Set up automation processes to manage TLS certificates, including renewal, updates, and revocation as needed.|
|[Certificate integrations and notifications](cert-inventory-mgmt-workflow.md)|Establish integration between Event Management systems and Certificate Inventory Management for real-time monitoring and response to certificate-related events. Configure notifications to be sent to Slack channels, keeping stakeholders informed about critical certificate events and changes.|
|[Certificate generation through Cert-Manager Integration](cert-mngr-integration.md)|Utilize Cert-Manager or a similar tool to automate the certificate generation process, ensuring efficient and secure issuance based on predefined policies.|

