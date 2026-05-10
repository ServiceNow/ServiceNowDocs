---
title: Domain separation and Generative AI Controller
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conkeyref at the end that describes domain separation.Domain separation is supported for Generative AI Controller. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Generative AI Controller
classification: generative-ai-controller
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Exploring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Domain separation and Generative AI Controller

Domain separation is supported for Generative AI Controller. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

Domain separation enables you to create partitions in the application data and administrative processes. Because the generative AI tables are domain separated, Generative AI Controller supports domain separation for OneExtend capabilities. The capabilities are the basic building blocks for Virtual Agent Designer topics, components, flows, and scripts that use generative AI. With domain separation, you can isolate the data and control access so that users in one domain don’t have access to the capabilities of another domain.

For more details on domain separation and Virtual Agent, [check out the documentation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/domain-separation-virtual-agent.md).

## How domain separation works in Generative AI Controller

Domain separation is possible at the generative AI OneExtend capability level. Records that are related to the execution and configuration of OneExtend capabilities, such as log tables that are accessible to ServiceNow personnel, are also separated according to the capability's domain.

If you want to create a copy of an existing generative AI capability in a different domain, you must create a record in the OneExtend Capabilities \(sys\_one\_extend\_capability\) table. See the [reference for Generative AI Controller](../reference/reference-for-generative-ai-controller.md) for more information about the OneExtend Capabilities table.

You set the domain when the record is created. The domain is based on the domain that you're in at the time that you create the record. When you're creating a capability record, you can use an existing OneExtend Capability record as a blueprint to help confirm that the capability works as intended.

After you create the OneExtend Capability record, you must create records for the following attribute and config records in the new domain:

-   OneExtend Capability Attribute records with the same values as the capability in the global domain.
-   A OneExtend Capability Definition that corresponds to the new capability.
-   A OneExtend Definition Config definition record that includes the OneExtend Capability Definition for the new domain.

For more information on setting up OneExtend Definition Configs to use in Virtual Agent Designer, see enabling Generative AI Controller for Virtual Agent.

You can also create these records by using the related lists in the OneExtend Capability record default view.

**Note:** The OneExtend Capability Definition record that you add must be the same as the capability that you want in the new domain. For example, if you’re creating a capability in a new domain for sentiment analysis, you could add the Sentiment Analysis \(OpenAI Completion\) record. Adding the Summarize \(OpenAI Completion\) Config could result in unexpected behavior. The OneExtend Definition Config record that you select should include the OneExtend Capability Definition record that you added.

## Use cases

With domain-separated capabilities, you can build different Virtual Agent topics, flows with Workflow Studio, or different background and business rule scripts that are also domain separated.

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

