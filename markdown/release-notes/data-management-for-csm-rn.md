---
title: Data Management for CSM release notes
description: The ServiceNow Data Management for Customer Service Management \(CSM\) application enables you to organize and manage the data for both your internal users and external customers. Data Management for CSM was enhanced and updated in the Brazil release. See the following sections for release notes by version.CSM Data Management unifies billing schedules and payment profiles for clearer visibility into billing accounts. It adds related-party and return merchandise authorization \(RMA\) tracking on sold products directly from the portal. It also auto-proposes major and child cases for business organization outages in the Brazil release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/data-management-for-csm-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Customer Service Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Data Management for CSM release notes

The ServiceNow® Data Management for Customer Service Management \(CSM\) application enables you to organize and manage the data for both your internal users and external customers. Data Management for CSM was enhanced and updated in the Brazil release. See the following sections for release notes by version.

## About Data Management

-   Unify billing schedules and payment profiles across all billing accounts, with visibility into when each account is billed, who is responsible for payment, and how payments are collected.
-   Manage related parties and deal context on sold products, and enable customers to create and track Return Merchandise Authorization \(RMA\) cases directly from the portal.
-   Track business organization outages efficiently. As a major case manager, get auto-proposed major cases and child cases for every affected organization, ensuring consistent updates across all impacted accounts.

See [Data management for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-data-management.md) feature for more information.

## Activation and other requirements

-   **Activation information**

    CSM is a ServiceNow AI Platform application that is available with activation of the Customer Service Management \(CSM\) plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/t_ActivateCustomerService.md).

    Additional CSM features are available with the activation of other plugins. For details, see .

    Sales Customer Relationship Management is a ServiceNow AI Platform feature that is available with the activation of the Lead to Cash Core plugin \(com.snd.l2c.core\). For details, see [Exploring Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-exploring.md).

-   **Browser requirements**

    Starting with the Brazil release, data management for Customer Service Management doesn't support mobile devices and Internet Explorer. For more information, see [Browser support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/browser-support.md).


**Parent Topic:**[Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/customer-service-mgmt-rn-landing.md)

## Version 1.0

CSM Data Management unifies billing schedules and payment profiles for clearer visibility into billing accounts. It adds related-party and return merchandise authorization \(RMA\) tracking on sold products directly from the portal. It also auto-proposes major and child cases for business organization outages in the Brazil release.

### What's new

-   **[Restricted Customer Access now controls visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/associate-customers-or-bus-loc-to-so.md)**

    Extended the organization customer criteria for a business organization with a new **Restricted Customer Access** check box that controls visibility of customer records. When enabled, business organization staff can view only the customer and consumer records that satisfy the configured criteria at their business organization. This applies to both service and sales personas. Upgrade customers must run the one-time scheduled job, **Remove Legacy roles from Loc Mgr Contrib** to enable restricted customer access configuration.

-   **[New business organization-scoped contributor personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-contributor-user-roles.md)**

    Added two new roles, Business Org Account Contributor \[sn\_bus\_loc.business\_org\_account\_contributor\] and Business Org Consumer Contributor \[sn\_bus\_loc.business\_org\_account\_contributor\] that grant location-scoped equivalents of the existing Account Contributor and Consumer Contributor roles. With Business Org Account Contributor role, you can create cases for accounts supported by your business organization. You can also track and manage cases created by you for the accounts associated with your organization. With Business Org Consumer Contributor role, you can create cases for consumers or households supported by your business organization. You can also track and manage cases created by you for the consumers or households associated with your organization.

-   **Proactive Customer Service extended to business organizations**

    Extended proactive customer service and major case management to business organizations, alongside the existing support for accounts and consumers. When a network alert affects install base items belonging to a business organization, the system can propose a major case and build a recipient list of the affected business organizations. If the major case manager accepts the proposal, they can create a child case for each affected business organization, so all affected business organizations are tracked and updated under a single major case. Business Organization staff can track cases from Business Organization Support Portal.

-   **[Billing account address](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/associate-location-with-billing-account.md)**

    Associate one or more locations with a billing account using the new Billing Account Address \[sn\_billing\_account\_address\] table. Each address record captures the address type, identifies the primary address, and tracks whether the address is active or inactive.

-   **[Billing account payment profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/add-payment-profile-to-billing-account.md)**

    Define payment information for a billing account using the new Billing Account Payment Profile \[sn\_billing\_account\_payment\_profile\] table, which captures the payment method and related payment details for the account.

-   **[Payment responsibility on billing accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/add-payment-profile-to-billing-account.md)**

    Specify who pays for a billing account with the new Paying party and Paying billing account fields, supporting self, parent, and designated-account payment relationships.

-   **[Billing schedules on billing accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/set-up-billing-schedule-for-billing-account.md)**

    Define when billing occurs for a billing account with the new Billing Schedule field, which links the account to a platform schedule and its schedule entry records. The new billing account schedule viewer \[sn\_billing\_account.schedule\_viewer\] and writer \[sn\_billing\_account.schedule\_writer\] roles control read and write access to these schedules.

-   **New fields across the Customer Data Foundation tables**

    Added fields to the core customer data model tables to support segmentation, life cycle tracking, and external-system integration:

    -   **Account table**: Account stage, Account status, Customer since, Relationship tier, Market segment, Total ACV, and External ID
    -   **Contact table**: External ID
    -   **Consumer table**: Consumer stage, Consumer status, Customer since, Relationship tier, and External ID
    -   **Account Team Member table**: Active, Start date, and End date

### What's changed

-   **Project task assignment access for business organization staff**

    Gain write access to the Assignment group and Assigned to field, and read access to the Priority field, on business organization project tasks with the Location Project Member \[sn\_bus\_loc.location\_project\_stakeholder\] or Location Project Manager Contributor \[sn\_bus\_loc.location\_manager\_project\_stakeholder\] role.

-   **[Billing account roles and responsibility access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/granular-roles-and-supported-entities-CAM.md)**

    Updated billing account roles and responsibility access to align with the expanded billing account capabilities. Extended access to Billing Account Address, Billing Account Payment Profile, and Billing Schedule \(schedule and schedule entry\) through:

    -   Billing Account platform granular and CRM granular roles
    -   Billing Account responsibilities through the customer access management \(CAM\) framework
-   **[Create a sold product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/create-sold-item.md)**

    Edit and view multiple related parties in the sold product enable users to review the details of a deal and review deal context without leaving the record. **Deal type** and **Route to Market** aren't captured on the sold product, with route to market options filtered automatically based on the selected deal type.

-   **[Create return merchandize authorization \(RMA\) cases directly from the business portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/rma-case-self-service.md)**

    Initiate an RMA case from the business portal without contacting an agent to reduce the back-and-forth for returns and replacements.

    -   Enable customer contacts to view the list of their RMA cases from the **Request** menu on the portal to track their requests in progress.
    -   Customer contacts can open individual RMA cases and drill into case lines to review its status and details.

### Plugin information

-   **Renamed or changed plugins**

    Customer Service Base Entities \(com.snc.cs\_base\): Renamed to CRM Base Entities \(com.snc.cs\_base\).

    Customer Service Base Extension Entities \(com.snc.cs\_base\_extension\): Renamed to CRM Base Extension Entities \(com.snc.cs\_base\_extension\).

    Customer Data Models for B2B2C \(com.sn\_csm\_b2b\_consumers\): Renamed to CRM B2B2C Entities \(com.sn\_csm\_b2b\_consumers\).

    Customer Service Install Base Characteristics \(com.snc.install\_base\_characteristics\): Renamed to Customer Install Base Characteristics \(com.snc.install\_base\_characteristics\).

    Customer Service Install Base Management \(com.snc.install\_base\): Renamed to Customer Install Base Management \(com.snc.install\_base\).


