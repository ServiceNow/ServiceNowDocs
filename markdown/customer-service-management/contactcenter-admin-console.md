---
title: CCaaS Admin Console
description: The Admin Console is a tool that administrators use to automate the import of data from CCaaS \(Contact Center as a Service\) providers into ServiceNow. This integration enhances Customer Service Management by enabling Unified Desktop and External Routing, which improves agent efficiency and customer experience.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating with contact centers, Integrate, Customer Service Management]
---

# CCaaS Admin Console

The Admin Console is a tool that administrators use to automate the import of data from CCaaS \(Contact Center as a Service\) providers into ServiceNow. This integration enhances Customer Service Management by enabling Unified Desktop and External Routing, which improves agent efficiency and customer experience.

## Admin Console overview

The Admin Console streamlines the integration of CCaaS providers with the ServiceNow platform, providing a seamless and unified experience for both customers and partners using ServiceNow.

Customer Service Management \(CSM\)

CCaaS providers can use the following features by integrating with the capabilities through their custom plugins. Review prerequisites and plugin requirements to enable the CCaaS Admin Console. See [Plugin requirements for voice and callback integrations with contact centers](../task/plugin-requirements-for-external-call-routing-integration-for-contact-centers.md).

## Accessing Admin Console

Access the CCaaS Admin Console in your ServiceNow instance by navigating to **All** &gt; **Contact Center Integration Center** &gt; **CCaaS Admin Console**.

In the Admin Console, admins must enter the provider ID and label for their contact center to establish a connection with their database. This integration allows the contact center to fetch data and import queues, skills, and wrap-up codes into ServiceNow. The process is streamlined using an extension point, enabling CCaaS providers to consistently return provider IDs and labels. This simplifies the integration, reduces manual configuration, and facilitates easy connections to multiple contact centers.

## Data Import

The key capability of the Admin Console is importing skills, queues, and wrap-up codes from the CCaaS provider platform into ServiceNow. This ensures data synchronization between both platforms for seamless and efficient interaction routing. Queues and skills routing helps direct incoming interactions to the right queue based on agent skills and interaction metadata, ensuring efficient handling of customer queries.

Data import helps customers set up and execute External Routing and Unified Desktop by ensuring data is synchronized across platforms. The Unified Desktop experience allows agents to handle both digital and voice interactions from a single ServiceNow Workspace, eliminating the need to switch between different interfaces and improving efficiency. Customers can choose between different routing engines to manage incoming calls and messages. The routing engine intelligently matches interactions with agents based on skills and experience, ensuring a better customer experience.

For more information, see: [Importing skills, queues, and wrap-up codes](import-skills-queues-and-wrap-up.md).

