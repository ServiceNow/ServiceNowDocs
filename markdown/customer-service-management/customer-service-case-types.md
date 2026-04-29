---
title: Customer service case types
description: A case type represents the processes and the data that are needed to resolve a specific type of customer issue. Use the case types feature to create and configure the different types of customer service cases that your organization needs.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Customer service case types

A case type represents the processes and the data that are needed to resolve a specific type of customer issue. Use the case types feature to create and configure the different types of customer service cases that your organization needs.

Customers can use case types to support a wide variety of end user needs, including:

-   Diverse industries and products
-   Complex processes, events, and systems
-   Collaboration with multiple users

A good example of an industry that benefits from multiple case types is the banking industry. Within a bank, customer service agents can use this feature to create case types for different customer needs such as loan processing, credit card processing, or managing complaints.

## Case types overview

-   **Configuring case types**

    System administrators configure the case types feature by creating a table for the new case type that extends the Case table and then setting up a number of different processes and components for the case type.

    -   The [Case Types Guided Setup](customer-service-case-types.md#section_ls3_dcp_bjb) section below provides an overview of these setup steps.
    -   For details about the case type guided setup tasks, see [Configure customer service case types](../task/configure-csm-case-types.md).
-   **Managing case types**

    After a case type has been created, system administrators can view the case types, manage settings, and update the configuration. For more information, see [Manage customer service case types](manage-csm-case-types.md).

-   **Using case types**

    Agents can use the case types feature when creating cases for customers by selecting from a list of configured case types. For more information, see the [Using case types to create cases](customer-service-case-types.md#section_s41_wtg_f4b) section below.


## Customer service case types plugin

Users with the system administrator role can activate the Customer Service Case Types plugin \(com.snc.csm\_case\_types\) and Service Request Criteria plugin .

Activating these plugin adds the **Customer Service** &gt; **Case Types** module to the application navigator. The system administrator can use this module to create and manage case types.

**Note:** Starting with the Zurich release, the Customer Service Case Types application \(sn\_csm\_case\_types\) has moved to the ServiceNow Store. Any new enhancements to this application are delivered through the Customer Service Case Types store app.

## Product Model and Catalog Items Relationship plugin deprecation

The Customer Service Case Types plugin replaces the Product Model and Catalog Items Relationship plugin \(com.snc.product\_catalog\_relationship\), which is being prepared for future deprecation. Use the [Service definitions](csm-service-definitions.md) feature, available with the Customer Service Case Types plugin, to create definitions for the services that are offered to support your products. Then [configure the service definitions](csm-service-definitions-configure.md) to associate them with the appropriate products and catalog items.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

## Customer service case types applications

The following applications for specific case types are available from the ServiceNow® Store.

<table id="table_urx_csq_zkb"><thead><tr><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Case Playbook for Onboarding \(sn\_csm\_onboarding\)

</td><td>

Provides an onboarding case type to capture the details when onboarding customers for a product or service and a playbook that provides step-by-step guidance through the lifecycle of the onboarding process.

</td></tr><tr><td>

Case Playbook for Complaints\(sn\_csm\_complaint\)

</td><td>

Provides a complaint case type to capture the details for a customer complaint and a playbook that provides step-by-step guidance through the lifecycle of the complaint.

</td></tr></tbody>
</table>For more information, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Note:** These applications have dependencies on the following plugins:

-   Customer Service Case Types \(com.snc.csm\_case\_types\)
-   Customer Service Case Action Status \(com.snc.csm\_action\_status\)

## Case Types Guided Setup

Activating the Customer Service Case Types plugin adds the Case Types section to the Customer Service Management Guided Setup. Navigate to **Customer Service** &gt; **Administration** &gt; **Guided Setup** &gt; **Case Types** and use the tasks in this section to create and configure a case type.

You can configure a number of different processes and components for a customer service case type, including client scripts and business rules; views, roles, and ACLs; and notifications and record producers.

To create and configure a new case type:

-   Create a table for the new case type that extends the Case table \(sn\_customerservice\_case\).
-   Configure UI actions, UI policies, and client scripts for the new case type.
-   Configure views and view rules, roles and ACLs, and business rules for the new case type.
-   Set up processes for the case type, including record producers, state flows, and special handling notes.
-   Create a case type definition record for the new case type and add it to the Case Type table \(sn\_case\_type\).
-   Configure the **Get Case Types** flow and modify the conditions that determine visibility for a case type.

For more information, see [Configure customer service case types](../task/configure-csm-case-types.md).

## Using case types to create cases

Customers can extend the Case table to handle different types of cases. Each extended case type can support multiple types of requests. For example, if a customer creates a case type for Credit Card Services, this case type can support requests such as applying for a new card and reporting a lost or stolen card.

When creating cases, customer service agents select the case type that corresponds to the customer issue.

-   In CSM Configurable Workspace and CSM Agent Workspace, agents select a case type from the [case type selector](csm-case-type-select-modals.md).
-   In the platform interface, agents select a case type from an interceptor.

In CSM Configurable Workspace, there are several versions of the [case type selector](csm-case-type-select-modals.md) that can be configured for agents to use when creating cases of a specific type. These versions include multi-select, single-select, and Product Service Select. The multi-select version is the default functionality. In CSM Agent Workspace, agents can use the multi-select version of the [case type selector](csm-case-type-select-modals.md).

-   [Create a customer service case of a specific type](../task/create-case-of-specific-case-type.md)
-   [Create a case task of a specific type for a customer service case](../task/create-case-task-specific-case-type.md)

