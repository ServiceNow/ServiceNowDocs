---
title: Domain separation and Financial Services Payment Operations
description: Domain separation is supported for Financial Services Payment Operations. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Payment Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Domain separation and Financial Services Payment Operations

Domain separation is supported for Financial Services Payment Operations. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## How domain separation works in Financial Services Payment Operations

All [Financial Services Operations \(FSO\)](../../fso-common/concept/fso-overview.md) applications are built on top of Customer Service Management \(CSM\) and use many CSM tables. The key reference tables are the customer tables such as Consumer, Account, and Contact, and these tables are domain-separated.

## Tables

All new tables added in Payment Operations are domain-separated:

-   sn\_bom\_payment\_inquiry
-   sn\_bom\_payment\_inquiry\_task
-   sn\_bom\_payment\_service
-   sn\_bom\_payment\_claim
-   sn\_bom\_payment\_claim\_task
-   sn\_bom\_checking\_account
-   sn\_bom\_saving\_account

## Use cases

-   **Payment Inquiry**

    Customers have the ability create a payment inquiry via the portal for the following use cases:

    -   Beneficiary Claim Non-Receipt \(BCNR\): The customer has sent a payment, but the intended recipient claims to have never received the money.
    -   Payment in Error \(PiE\) – The customer makes a mistake when sending a payment and is trying to retrieve the money.
    Branch workers and call center agents can create these inquiries on behalf of the customer. Payment Operations staff receive inquiries from their customers as well as from external banks.

    -   Internal inquiries come from the bank’s own customers. The recipient customer could be internal or external to the bank. The distinction between internal or external recipients is important because it determines which route Payment Operations takes to resolve the inquiry.
    -   External inquiries come from third-party banks, which means that the payment recipient is always internal.

        **Note:** There can never be a case where the inquiry is external and the recipient is external.

    -   Some inquiries may result in the creation of a claim.
-   **Payment Claim**

    Inquiry agents can create a claim on behalf of a customer when the bank determines that the claim is valid and the customer is entitled to a refund.

    Payment Operations staff receive the claims either internally from an inquiry or from an external bank. When they receive the claim, they start determining where to get the refund.

    -   Internal claims come from customers of the bank either from an inquiry or directly from bank staff \(Branch or Call Center\). Agents can resolve the claim if they know where to get the refund. The refund could be either external \(payment to a third-party bank customer\) or internal \(payment to the bank's customer\). If the refund is internal, a Debit Approval must be created \(see **Debit Approval** below\).
    -   External claims come from third-party banks. The refund is always internal for external claims. Agents may need to create a Debit Approval for internal refunds \(see **Debit Approval** below\).
-   **Debit Approval**

    Claim agents create Debit Approvals for customers to approve a refund from a claim. The customer can either accept the debit or dispute or reject it.


**Note:** Sometimes a ServiceNow® platform feature or application may be able to effectively support service provider use cases even though the domain framework is not being used. In this case, the application may be assigned Basic\*, Standard\*, or Enhanced\* for its domain support level, and include detailed use cases. For example: Before the New York release, Service Catalog had no domain support. But the instance owner was able to configure separate catalogs and items for each customer in a domain-separated instance. This allowed Service Catalog to be used at a **Standard** support level. To learn more, see domain separation [Application levels of support](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

**Parent Topic:**[Financial Services Payment Operations reference](payment-operations-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

