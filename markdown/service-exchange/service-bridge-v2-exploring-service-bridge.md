---
title: Exploring Service Exchange
description: Service Exchange helps providers, consumers, and partners connect their ServiceNow instances to build secure business workflows across the ServiceNow ecosystem.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Service Exchange]
---

# Exploring Service Exchange

Service Exchange helps providers, consumers, and partners connect their ServiceNow instances to build secure business workflows across the ServiceNow ecosystem.

## Service Exchange overview

Service Exchange connects multiple ServiceNow instances to provide seamless support and service experiences across the ecosystem, from enterprise customers to suppliers and system integrators. Service Exchange provides a frictionless experience that makes it easy to collaborate and process requests while giving users the convenience of working in their own ServiceNow instance.

Watch this short video for an introduction to the Service Exchange application.An overview of Service Exchange 

Service Exchange has two components or applications:

-   Provider application: An application that enables the service provider to deliver a streamlined and comprehensive solution for managing their service offerings.
-   Consumer application: An application that enables consumers to interact and collaborate with service providers.

## Service Exchange workflow

Service Exchange enables providers to integrate their ServiceNow instances with their customers and partners seamlessly.

![Infographic showing how Service Exchange connects various ServiceNow instances.](../image/service-bridge-v2-explore-sb-lp.svg)

1.  -   **Service Exchange establishes the connection**

    The provider initiates a registration task using Service Exchange to establish a secure, bi-directional connection between multiple instances to enable better collaboration. All necessary instances such as enterprise or partner instances are connected using Service Exchange.

2.  -   **Enterprise initiates a request**

    The workflow begins with the enterprise, also known as the consumer, accessing catalog items that have been published by the provider. These catalog items are integrated into the enterprise’s ServiceNow instance. The enterprise user submits a request for one of these items and a task is created in the consumer instance. This task is then synchronized with the provider’s instance, enabling the provider to fulfill the request while the consumer retains visibility into its progress.

3.  -   **Provider executes and manages services**

    After the connection between the provider and consumer is established, the provider takes charge of delivering and managing the requested services that involves setting up remote tasks, which are mirrored between the provider and consumer instances to support collaborative work. In addition, provider tasks are created to give the consumer visibility into the progress of the request, although the consumer doesn’t participate in fulfilling these tasks. The provider can also initiate proactive cases, which automatically generate provider tasks in the consumer’s instance when specific alerts or conditions are met, enabling timely communication and action.

4.  -   **Partner supports fulfillment**

    The provider can delegate specific tasks to its fulfillment partners. These partners operate within the same Service Exchange infrastructure and receive tasks that are tracked and updated in real-time. This mechanism promotes transparency and continuity across all parties involved in the service delivery process.


Service Exchange promotes real-time collaboration by keeping all connected instances updated with the latest changes, comments, and status updates. These updates are synchronized based on the configured settings, enabling both providers and consumers to stay aligned throughout the service process. This continuous flow of information improves collaboration, enhances transparency, and maintains a secure exchange of data between ServiceNow instances.

## Service Exchange benefits

|Feature|Benefit|
|-------|-------|
|[Mismatched versions](service-bridge-v2-mismatch-version.md)|Run provider and consumer instances on different platform releases and application versions without disrupting the active entitlements or processes.|
|[Configuration revisions](service-bridge-v2-config-revision.md)|Edit or create revisions of entitlements such as remote tasks, remote catalogs, with updated functionality, and deploy them to consumers.|
|[Remote catalog](service-bridge-v2-create-apps.md)|Keep the development of shared catalogs and the workflows/integrations in the provider instance while sharing them with consumers as simple record producers that generate integrated requests in the provider instance.|
|[Proactive cases](service-bridge-v2-proactive-case.md)|Collaborate and foster transparency with your customers by sending Provider Tasks to the consumer instance.|
|[Provider task](service-bridge-v2-provider-tasks.md)|Send case alerts proactively from the provider task table to connected consumers without additional setup or configuration to promote transparency and collaboration.|
|[Remote task](service-bridge-v2-remote-task-overview.md)|Use remote task as a sustainable alternative to custom eBonding to create linked tasks across multiple instances without building an integration. A remote task transmits comments, attachments, and mapped fields between instances, enabling better business workflows.|
|[ScratchPad](service-bridge-v2-scratchpad-consumer.md)|Share name-value pairs as JSON data on provider tasks and remote tasks to enable structured data exchange between instances.|
|[Foundation data sync](service-bridge-v2-explore-foundation-data-sync.md)|Share selected foundational data types with your consumers on a scheduled cadence to reduce manual effort, and eliminate the need to share data externally.|
|[Journal field framework](service-bridge-v2-expolre-journal-field-framework.md)|Map and synchronize journal-type fields between provider and consumer instances to keep critical operational updates current. It also maintains historical continuity by synchronizing previous journal entries, and enhances authenticity and accountability by writing journal entries as a named user rather than using a generic company name.|
|[Flow action](service-bridge-v2-flow-action.md)|Ensure that remote tasks and remote record producers continue to function correctly as you adopt newer revisions by maintaining flow compatibility across configuration updates using four new Flow Actions that preserve mapped variable integrity.|
|[Magic link](service-bridge-v2-explore-magic-link.md)|Convert regular links sent from a provider instance into magic links that enable consumer users to access the linked resource directly in the provider instance without having to log in manually.|

## Applications

<table id="table_jyd_yjw_ffc"><thead><tr><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider

</td><td>

This application enables the provider to deliver services and support to consumers.-   Create and publish remote catalogs from your instance for consumers to generate service requests that can be fulfilled in your instance.
-   Integrate your tasks bidirectionally with your consumer's tasks.
-   Send incidents and cases to your consumer's ServiceNow instance via Provider Task with no setup needed.

</td></tr><tr><td>

Consumer

</td><td>

This application enables the consumer to receive services and support from providers.-   Incorporate remote catalog items assigned to you from your provider into your local catalog and send the requests generated back to your provider for fulfillment.
-   Bidirectionally integrate your tasks with your provider's tasks.
-   Receive proactive tasks from providers to enhance transparency and collaboration.

</td></tr></tbody>
</table>## Service Exchange users

|Application|User|Description|
|-----------|----|-----------|
|Provider|Administrator|The provider administrator is responsible for setting up and maintaining the technical components of Service Exchange. This includes establishing connections, configuring Workflow Studio flows, and publishing service content to consumer instances. They also support registration and troubleshoot integration issues to promote smooth and secure collaboration between provider and consumer instances.|
|Provider|Provider Fulfiller/Agent|The fulfiller/agent is responsible for resolving consumer questions and issues, and may also engage in network operations when needed to support service delivery.|
|Provider|Consumer|The consumer is responsible for consumer registration tasks.|
|Consumer|Administrator|The consumer administrator is responsible for setting up and managing the Service Exchange connection from the consumer side. This includes installing the Service Exchange applications, creating provider and connection records, maintaining transforms, and troubleshooting transport payloads to promote smooth and reliable integration with the provider instance.|
|Consumer|Fulfiller/Agent|The consumer agent is responsible for managing IT services that rely partly or entirely on external providers. They place and track service requests with the provider from within their own instance, promoting that issues are addressed and services are delivered as expected.|
|Consumer|Requester|The requester is responsible for making requests from the remote catalog.|

## What to explore next

-   [Service Exchange for Providers](service-bridge-providers-landing-page.md)
-   [Service Exchange for Consumers](service-bridge-consumers-landing-page.md)
-   [Service Exchange reference](../reference/service-bridge-v2-reference.md)

