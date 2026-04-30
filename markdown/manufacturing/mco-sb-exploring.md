---
title: Manufacturing Commercial Operations with Service Bridge
description: Securely build business workflows across the ServiceNow ecosystem using Service Bridge for Manufacturing Commercial Operations.Use the Service Exchange application with Manufacturing Commercial Operations for providers to create and publish catalogs of services, receive, and fulfill requests generated from consumers, and establish integrations with consumer instances.Use the Service Exchange application with Manufacturing Commercial Operations so your consumers can make any requests they need.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-10-10"
reading_time_minutes: 6
keywords: [​]
breadcrumb: [Exploring Manufacturing Commercial Operations, Manufacturing]
---

# Manufacturing Commercial Operations with Service Bridge

Securely build business workflows across the ServiceNow ecosystem using Service Bridge for Manufacturing Commercial Operations.

## Manufacturing Commercial Operations for Providers with Service Exchange

Use the Service Exchange application with Manufacturing Commercial Operations for providers to create and publish catalogs of services, receive, and fulfill requests generated from consumers, and establish integrations with consumer instances.

A provider instance belongs to the OEM/manufacturer who provides Service Bridge to the end users such as customers, dealers, and partners.

As a manufacturing provider, you can:

-   Author and publish remote service catalogs for your customers, suppliers, channels, or manufacturing partners on their instances.
-   Integrate your instance with the instances within your manufacturing ecosystem.
-   Receive and fulfill service requests on your instance from your customers', suppliers', channels', or manufacturing partners' ServiceNow® instance\(s\).

A provider in the manufacturing industry can use Service Exchange for Manufacturing Commercial Operations to provide various types of support to consumers, such as:​

-   Technical support​
-   Order and Parts fulfillment
-   Claims Management​
-   Routing to AR team​
-   Dispute resolution
-   Field Technician Dispatch \(requires an [integration with FSM](integrating-manufacturing.md)\)

| | | |
|---|---|---|
|Remote Catalog​|Keeps the development of shared catalogs with the workflows &amp; integrations in the providers instances while providing consumers with native catalog items in their instances.​|Customers, Channels, Partners are avoiding creating their own catalogs, and can utilize the OEM’s remote catalog, leads to reduced costs and decreasing errors as well as increasing customer experience. Additionally increasing the efficiency and productivity at OEM as well as at consumer.​|
|Remote Task​|A sustainable replacement for custom eBonding. Collaborate effortlessly across the ServiceNow ecosystem. Native alternative to traditional E-Bonding. Enables task to task integration.​|Avoids the need to build costly and error-prone integrations. Enhances collaboration and communication, while improving service quality.​|
|Proactive Case​|A case initiates a Provider Task through a flow on the Provider instance that can be checked proactively on the consumer instance. There is a Proactive Case flow behind to sync.​|Simplifies and increases automation ratio for alerting process or notification process, like recall management. Improves the service delivery quality and streamlines tasks assignments.​|
|Scratchpad​|Scratchpad allows variables to be shared “ad hoc” between instances through Remote Tasks or Provider Tasks.​|Simplifies data sync between the instances and reduces adoption efforts. Quick data entry and retrieval, leading to reduced time spend by capturing data and updating directly in scratchpad.​|
|Authorized User​|Enables user level role based access control of Remote Record Producers in the customer instance.​|Avoids mismatch possibilities due to adoption of user level role based access control. Reduces compliance risks by reducing access errors through data mismatch​|
|Provider Task \(record producer\)​|Enables providers to be transparent and collaborative with their consumers that use ServiceNow by syncing relevant tasks, like cases, to their consumers as Provider tasks.​|Simplifies data sync between the instances and avoids data mismatches between the cases in the different instances​|
|Configuration Revisions​|The configurations of remote record producers, remote task definitions, and foundation data sync offerings can be updated to create new revisions that can be entitled to consumers. New revisions of entitlements with updated functionality can be deployed to compatible consumers without impacting consumers who have not upgraded their Service Bridge applications. ​|New revisions of Service Bridge entitlements that offer updated functionality can be developed and deployed to compatible consumers without negatively impacting consumers who have not yet updated their application. The provider delivers an improved customer experience with improved efficiency and scalability.​|
|Mismatch Version Support​|Providers and consumers can run different versions of the Service Bridge applications \(within N-2\) without impacting their ability to exchange data.​|This feature eliminates the need for providers to coordinate Service Bridge applications updates with their consumers and allows providers to adopt new features while supporting consumers who have yet to upgrade. Service Bridge supportability and scalability are improved, and the Provider is able to deliver an improved customer experience.​|
|Order Management Support​|When a Product Offering is defined in Sales and Order Management \(SOM\), the administrator can specify a Remote Catalog Item, and the offering will be published as a Remote Record Producer in entitled Service Bridge connected customers’ service catalogs.​|A customer can order a Sales and Order Management \(SOM\) product offering from a connected Service Bridge provider using a Service Bridge Remote Record Producer, enabling faster order fulfillment, improved accuracy, and improved customer satisfaction.​|

For information on setting up Service Exchange for Providers with Manufacturing Commercial Operations, see [Install Service Bridge for Providers in Manufacturing Commercial Operations](../task/mco-install-sb-providers.md).

## Manufacturing Commercial Operations for Consumers with Service Exchange

Use the Service Exchange application with Manufacturing Commercial Operations so your consumers can make any requests they need.

As a consumer, you can do the following using the Manufacturing Commercial Operations Service Exchange consumer portal:

-   View the service catalog and create requests \(i.e., report product issues\)​
-   See remote choices and case updates in real time
-   Receive resolution comments.
-   See all employee related items in one place \(HR issues, product issues\)​

A consumer instance is one that contains a B2B customer, channel, supplier or 3PL, who is receiving the Service Bridge connection​. A consumer with a consumer instance can use Manufacturing Commercial Operations with Service Exchange for Consumers to:

-   Submit product issues \(hardware &amp; software\)​
-   Order parts​
-   Replace equipment​
-   Submit issues with an invoice​
-   Change orders​
-   File a warranty claim​

| | | |
|---|---|---|
|Remote Choice​|Provides direct access to provider data in real time during the submission of a Remote Catalog item.​|Removes the need to replicate foundation data into the consumer instance. Having the right information at the right time reduces the chances of errors and reduces costs.​|
|Transformation Framework​|Enables a provider or consumer to transform inbound and outbound data for Remote Tasks. Easily transform fields with static choices like State, and Priority. Advanced scripted transforms allow for complex logic.​|Simplifies the communication with each other \(OEM, consumer\), that agents can focus more on resolving the incidents, cases, and consumer requests.​|
|Mismatch Version Support​|Providers and consumers can run different versions of the Service Bridge applications \(within N-2\) without impacting their ability to exchange data.​|This feature eliminates the need for providers to coordinate Service Bridge applications updates with their consumers and allows providers to adopt new features while supporting consumers who have yet to upgrade. Service Bridge supportability and scalability are improved, and the Provider is able to deliver an improved customer experience.​|
|Consumer Pre-Flows​|Consumers can control if and when data should be synced between the provider tasks on the consumer and provider. A flow can be associated with a Service Bridge Remote Record Producer \(RRP\) and run consumer-defined processes, such as approvals, before the request/task is synchronized to their provider.​|Consumer Pre-Flows will enable Service Bridge providers to improve their service for current consumers and expand to additional customers for whom this feature is a requirement.​|
|Order Management Support​|When a Product Offering is defined in Sales and Order Management \(SOM\), the administrator can specify a Remote Catalog Item, and the offering will be published as a Remote Record Producer in entitled Service Bridge connected customers’ service catalogs.​|A customer can order a Sales and Order Management \(SOM\) product offering from a connected Service Bridge provider using a Service Bridge Remote Record Producer, enabling faster order fulfillment, improved accuracy, and improved customer satisfaction.​|

For information on setting up Service Exchange for Providers with Manufacturing Commercial Operations, see [Install Service Exchange for Consumers in Manufacturing Commercial Operations](../task/mco-install-sb-consumers.md).

