---
title: Cross-instance application trust configuration
description: Multi-instance management provides a mechanism to streamline the management of trust configurations across your entire multi-instance environment.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Multi-instance Management, Get started, Administer the ServiceNow AI Platform]
---

# Cross-instance application trust configuration

Multi-instance management provides a mechanism to streamline the management of trust configurations across your entire multi-instance environment.

The multi-instance capability introduces new concepts, describing how communication is supported across instances for enabled applications and their capabilities. In order to do this securely, you need to define how these instances trust each other. This can be defined as a trust profile. The trust profile defines how a set of instances communicate for a given application. In order for this profile to be applied to each instance, that profile needs to be propagated out to the instances that will participate in a given application.

Multi-instance management offers a centralized mechanism for configuring and maintaining trust settings across your multi-instance deployment. This simplifies the process of propagating trust settings to all instances under your control by designating a production instance by designating a production instance to manage the trust configurations on all the instances it should manage remotely.

## Trust concepts

-   **Trust profile**

    The Trust profile defines the ideal trust configuration of all the instances that participate in a specific application. The trust profile is specific to an enabled application. It defines how the instances leverage the application capabilities to communicate with each other. Once the application’s trust profile with the trust configuration for each instance is defined, it can be shared with the managed instances. This will trigger the automatic population of trust tables within those instances. This automation depends on whether there is a Trust profile manager defined. If not, trust configuration needs to be manually created on each instance.

    For example, if you're currently logged into sub-prod 2 and Prod 1 has management privileges over sub-prod 2, you can use the **Sync Trust Profile** button on Prod 1 to distribute trust profiles to all instances under Prod 1's management. The updated trust profile will then be reflected on Prod 2.

-   **Capabilities and operations**

    Capabilities are application features that would be leveraged for cross instance communication. It is a group of granular operations that are available as a part of the application.

    Enabled applications within an instance possesses a trust profile, which is established for every capability it exposes. To ensure seamless communication between instances for these capabilities, a trust configuration must be defined. This trust profile encompasses all the necessary trust configurations between instances for a specific application and its capabilities.

-   **Trustor and Trustee**

    Trustor can be defined as the instance that is trusting the other instances with viewing its data and/or receiving messages from the trusted instance.

    For example, you’re logged into Prod 1. There are 2 other sub prods- sub-prod 1 and sub-prod 2. If Prod 1 trust sub-prod 1 and sub-prod 2, then Prod 1 is the Trustor and sub-prod 1 and sub-prod 2 are Trustees.

    **Note:** The trust concept works on the instance for a given application at the capability level. The table that lists the instances trusted by your instance has 3 columns: application, capability, and Trustee instance.

    When instances are required to communicate, they consider the application trust configuration before communicating with each other.

    For example, if an enabled application on Prod 1 needs to send a message to Sub-prod 1 and Sub-prod 2, these sub-prods must trust Prod 1 to receive the message and act on it. In this scenario, the sub-prods are the trustors, and Prod 1 is the trustee.

    If Prod 1 doesn't trust sub-prod 1 and sub-prod 2, messages from the sub-prods to Prod 1 are not processed.

    You can go to the trust table and create a new trust record. See  for more information.


## Trust configuration management

-   **Managing instances**

    The table shows the instance that is designated as the manager instance for the instance you are logged into. If you are logged into the managing instance, the table will be blank.

    For example, you’re logged into Prod 1. The instances shown in the Managing Instances table are the instances that are being managed by Prod 1 for particular applications.

    See [Configure Manager Instances](../task/mif-conf-manager-instance.md) for more information.

-   **Managed instances**

    The table shows the instances that you are managing.

    For example, you’re logged into Prod 1. The instances shown in the Managed Instances table are the instances that Prod 1 is managing for the specified applications.

    Managed instances must grant permission to managing instances in order to automatically distribute trust profiles.

    **Note:** An instance can’t be both a managing and a managed instance. An instance can manage several instances simultaneously. An application within an instance can be managed by only one instance at a time.


