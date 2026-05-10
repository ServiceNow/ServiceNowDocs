---
title: Service Exchange for Public Sector Digital Services
description: Connect multiple ServiceNow instances to provide support and service experiences across the Public Sector​ ecosystem, enabling coordination between multiple government service agencies and their constituents using Service Bridge for Public Sector Digital Services \(PSDS\).
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Case management, Explore, Public Sector Digital Services \(PSDS\)]
---

# Service Exchange for Public Sector Digital Services

Connect multiple ServiceNow instances to provide support and service experiences across the Public Sector​ ecosystem, enabling coordination between multiple government service agencies and their constituents using Service Bridge for Public Sector Digital Services \(PSDS\).

Enable agency to agency communication and coordination across multiple ServiceNow instances using Service Bridge for Public Sector Digital Services \(PSDS\). Agencies can coordinate across the ServiceNow® Public Sector Digital Services ecosystem, facilitating cross-agency case management​, real-time coordination with dynamic task management, secure inter-agency data sharing, and streamlined approval workflows for license and permits, social benefits, and grants funding distribution.

Public Sector Digital Services Overview

Whether you are a government agency provider communicating with other agencies, or an agency connecting with their constituents, learn how you can establish an integration between multiple types of instances with Service Exchange. This integration allows agency providers to receive and fulfill service requests in their own instances, share data, route tasks in real-time, and more. Learn how you can use Service Exchange for inter-agency data sharing, constituent support, and service catalog management.

-   Enterprise users can collaborate with service providers and partners through bi-directional workflows.
-   Service Exchange enables streamlined onboarding, and provides a remote service catalog that can be updated in real-time.

A provider instance belongs to the government agency who provides Service Bridge to other agencies and partners. As a government agency provider, you can:

-   Author, publish, and update remote service catalogs from your instance for your constituents, business contacts, channels, or agency partners to generate service requests on their instances that can be fulfilled in your instance.
-   Integrate your instance and tasks with the other instances in your Public Sector ecosystem.
-   Send cases to your constituent's ServiceNow instance via Provider Task
-   Receive and fulfill service requests on your instance pushed remotely from your constituents', business partners', channels', or agency partners' ServiceNow® instance\(s\).
-   Access data synced in real-time between the provider instance and the consumer instance to track updates to government case records

![Exploring Service Bridge for PSDS](../image/psds-servicebridge_graphic.png)

Agencies can connect:

-   Within the agency across multiple departments​
-   With businesses or constituents​
-   With suppliers​
-   With implementation partners
-   With other agencies

A consumer instance

| | | |
|---|---|---|
|Remote Catalog​|Keeps the development of shared catalogs between agencies with the workflows &amp; integrations in the providers instances while providing constituents with native catalog items in their instances.​|Other agencies can avoid creating their own catalogs, and can utilize the original agency's remote catalog, leads to reduced costs and decreasing errors as well as increasing customer experience. Additionally increasing the efficiency and productivity at original agency as well as at consumer.​|
|Remote Choice|Provides direct access to provider data in real time during the submission of a Remote Catalog item.​|Removes the need to replicate foundation data into the consumer instance. Having the right information at the right time reduces the chances of errors and reduces costs.​|
|Remote Task​|A sustainable replacement for custom eBonding. Collaborate effortlessly across the ServiceNow ecosystem. Native alternative to traditional E-Bonding. Enables task to task integration.​|Avoids the need to build error-prone integrations. Enhances collaboration and communication, while enhancing service quality.​|
|Proactive Case​|A case initiates an agency Provider Task through a flow on the agency provider's instance that can be checked proactively on the consumer instance. There is a Proactive Case flow behind to sync.​|Simplifies and increases automation ratio for alerting processes or notification processes. Improves the service delivery quality and streamlines tasks assignments.​|
|Scratchpad​|Scratchpad allows variables to be shared “ad hoc” between instances through Remote Tasks or Provider Tasks.​|Simplifies data sync between agency and consumer instances and reduces adoption efforts. Quick data entry and retrieval, leading to reduced time spend by capturing data and updating directly in scratchpad.​|
|Authorized User​|Enables user level role based access control of Remote Record Producers in the constituent instance.​|Avoids mismatch possibilities due to adoption of user level role based access control. Reduces compliance risks by reducing access errors through data mismatch​.|
|Provider Task \(record producer\)​|Enables agency providers to be transparent and collaborative with their consumers that use ServiceNow by syncing relevant tasks, like cases, to their constituents as Provider tasks.​|Simplifies data sync between the instances and avoids data mismatches between the cases in the different instances​|
|Configuration Revisions​|The configurations of remote record producers, remote task definitions, and foundation data sync offerings can be updated to create new revisions that can be entitled to constituents. New revisions of entitlements with updated functionality can be deployed to compatible consumers without impacting consumers who have not upgraded their Service Bridge applications. ​|New revisions of Service Bridge entitlements that offer updated functionality can be developed and deployed to compatible consumers without negatively impacting consumers who have not yet updated their application. The agency provider delivers an improved customer experience with improved efficiency and scalability.​|
|Mismatch Version Support​|Providers and consumers can run different versions of the Service Bridge applications \(within N-2\) without impacting their ability to exchange data.​|This feature eliminates the need for agency providers to coordinate Service Bridge applications updates with their consumers and allows providers to adopt new features while supporting consumers who have yet to upgrade. Service Bridge supportability and scalability are improved, and the agency provider is able to deliver an improved customer experience.​|
|Consumer Pre-Flows​​|Constituents in the consumer instance can control if Remote Catalog Item request data should be synced to the provider. ​​A flow can be associated with a Service Bridge Remote Record Producer \(RRP\) and run consumer-defined processes, such as approvals, before the request/task is synchronized to their provider.​​|Consumer Pre-Flows will enable Service Bridge providers to improve their service for current consumers and expand to additional customers for whom this feature is a requirement.​​|
|Consumer Variable Sets​​|A Service Bridge consumer administrator can now add additional variables to a Remote Catalog Item/RRP that they can use in managing the request content and flow. ​​|Allowing this additional consumer control of Service Bridge RRP requests will enhance Service Bridge useability, elevate the customer experience, and driver higher adoption rates.​​|
|Remote Catalog Item Client Scripts​​|A provider will be able to include catalog client scripts that will be synchronized to the consumer’s instance with a Remote Catalog item. ​​The consumer administrator will review and approve each script when activating the catalog item in their instance. ​|Allow providers to control the completeness and correctness of catalog requests from the consumer, enabling more efficient service and improved consumer satisfaction; and will lead to increased adoption of Service Bridge.​​|

## Key capabilities

The main capabilities of Service Exchange include:

-   [Onboarding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-onboarding.md): Quickly onboard agency partners or constituents that use ServiceNow with a simplified registration process.
-   [Authorized Users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-auth-users.md): Manage and control access at the Remote Catalog item level to meet security and compliance requirements.
-   [Remote Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-create-apps.md): Update shared agency service catalogs in minutes as new items are introduced.
-   [Remote Choice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-remote-choice-fields.md): Ensure up-to-date field options in downstream agency remote catalogs by retrieving real-time data from the provider's ServiceNow instance.
-   [Remote Task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-remote-task-overview.md): Help increase automation with seamless multi-party and multi-instance workflows across the ServiceNow ecosystem.
-   [Provider Tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-provider-tasks.md): Enable all providers of services using Service Exchange to be transparent and collaborative with their partner agencies who use ServiceNow by syncing relevant tasks like cases, to consumers as Provider Tasks.
-   [Transform Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-provider-tasks.md): Transform inbound and outbound remote task data for easy process transformation between ServiceNow instances.

