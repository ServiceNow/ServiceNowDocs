---
title: Customer Contracts and Entitlements release notes
description: The ServiceNow Customer Contracts and Entitlements application enables users to manage contracts from the initial offer to contract finalization, directly within the CSM Configurable Workspace. See the following sections for release notes by version.You can now create contracts and entitlements for a buyer organization, as well as an account or consumer.The September 2026 release includes user experience improvements in quote related workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/customer-contracts-entitlements-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Sales Customer Relationship Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Customer Contracts and Entitlements release notes

The ServiceNow® Customer Contracts and Entitlements application enables users to manage contracts from the initial offer to contract finalization, directly within the CSM Configurable Workspace. See the following sections for release notes by version.

## About Customer Contracts and Entitlements

-   View and manage contracts and entitlements directly within the CSM Configurable Workspace, tracking entitlements and improving contract compliance.
-   Establish relationships with existing customer data, such as sold products and install base items, by adding contract and entitlement data to the common data model.
-   Support customer needs ranging from account-based support entitlements to contracts with service plans that include complex entitlement coverage.
-   Manage the complete life cycle of customer contracts and entitlements, including generating, renewing, modifying, suspending, resuming, and canceling, through Contracts and Entitlement workflows.

See [Customer Contracts and Entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/exploring-post-sales-support.md) for more information.

## Activation and other requirements

-   **Activation information**

    Customer Contracts and Entitlements is a ServiceNow AI Platform feature that is available with activation of the \(com.sn\_pss\_core\) plugin, which requires a separate subscription. For details, see [Configure Customer Contracts and Entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/configuring-post-sales-support.md).


**Parent Topic:**[Sales Customer Relationship Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/sales-order-management-rn-landing.md)

## Version

You can now create contracts and entitlements for a buyer organization, as well as an account or consumer.

### What's new

-   **[Contracts and entitlements for buyer organizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/service-contract-form.md)**

    Enable users to create contracts and entitlements for service organizations, in addition to accounts and consumers. When an order fulfilled for a buyer organization is processed to a contract or entitlement, the buyer organization information is populated in contracts and entitlements automatically.

-   **[Enhancements in Modify workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/cce-modify-service-contract-line.md)**

    Enhanced Modify workflows by enabling users to modify an entire line, quantity, or end date through a single Modify action. The Modify workflow shows only the changes allowed for the selected lines, based on whether the line is configurable or a simple product.

-   **[Enhancements in Renewal workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/cce-renew-service-contract-line.md)**

    Following enhancements have been made in the renewal workflow:

    -   If a customer contract or customer contract line that is terminated before its end date, it is excluded from the renewal workflow.
    -   If a contract line is terminated before its end date, then the renewal quote for that contract line is deleted.
    -   If a contract line is terminated before its end date, then the status of that contract line is updated to **Canceled** when the contract reaches its end date.

## Version 20.0.0

The September 2026 release includes user experience improvements in quote related workflows.

### What's new

-   **Support ServiceNow® Quote Experience for Contracts and Entitlements**

    Open quotes created from Customer Contracts and Entitlements lifecycle workflows in the ServiceNow® Quote Experience. Activating the Quote Experience plugin provides you a unified experience for creating, pricing, approving, and quote completion in a single interface. Quotes generated from contract renewal and amendment workflows in ServiceNow® Quote Experience maintains consistent workflows, pricing logic, and governance.


### Plugin information

-   **New plugins**

    Quote Experience \(`sn_quote_mgmt_adv`\): Enables the ServiceNow® Quote Experience for contract renewal and amendment workflows.


