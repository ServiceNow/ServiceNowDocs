---
title: ServiceNow Quote Experience: Access Control
description: ServiceNow Quote Experience controls access at two levels: record access, which determines who can view or modify a quote, and field access, which controls the fields a user sees within a quote. Record access can be managed by your CRM or natively within ServiceNow Quote Experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/cpq-transaction-manager-transaction-access-control.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [CPQ Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# ServiceNow Quote Experience: Access Control

ServiceNow Quote Experience controls access at two levels: record access, which determines who can view or modify a quote, and field access, which controls the fields a user sees within a quote. Record access can be managed by your CRM or natively within ServiceNow Quote Experience.

ServiceNow Quote Experience supports two approaches to record access control:

-   CRM-managed access control, where the CRM system determines which records a user can access.
-   Quote-managed access control, where access is controlled through functionality native to ServiceNow Quote Experience. This approach is recommended only for headless implementations.

The appropriate model depends on your implementation architecture and on which system acts as the source of truth for user access.

## Field access control

Regardless of the record-level approach you use, field access is managed in CPQ Administration through the Views and Personas features of the quote blueprint. For more information, see [Quote transaction views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-views.md) and [Quote transaction personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-personas.md).

## CRM-managed access control

When ServiceNow Quote Experience is deployed with Sales CRM, record access is managed through standard ServiceNow AI Platform table access controls \(ACLs\). The access controls on the quote tables determine whether a user can create, read, update, or delete a quote record, and ServiceNow Quote Experience validates access based on those permissions.

For more information on the roles that govern quote access, see [Components Installed with Quote Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/components-installed-quote-management.md).

**Note:** On the opportunity record, the fields shown in the quote list are governed by the quote table ACLs.

## Quote-managed access control

In quote-managed access control, access is governed by functionality native to ServiceNow Quote Experience rather than by the CRM. This approach improves security and compliance by giving you precise control over who can view and edit each quote, and is recommended for headless implementations, where it can limit a list of quotes to those the current user is authorized to access.

Quote-managed access control is governed by a tenant setting and is turned off by default. When the setting is inactive, all users can access all quotes.

## Access levels

When quote-managed access control is active, each user has one of the following access levels.

-   **Admin**
    -   Can view and edit all quotes.
    -   Can grant full access to other users.
    -   Can revoke full access, but not owner status.
    -   Cannot be removed.
-   **Owner**
    -   Assigned to the creator of a quote.
    -   Can view and edit the owned quote.
    -   Can grant or revoke full access.
    -   Cannot be removed if they are the last owner.
-   **Full access**
    -   Can view and edit specified quotes.
    -   Can grant or revoke full access for other users.

## Manage quote-managed access

You manage quote-managed access from the runtime UI.

Any user with access can grant or remove access for other users. However, admins and owners cannot have their access removed. When a user without access tries to open a restricted quote, an error is displayed.

When quote-managed access control is enabled on an instance that already contains quotes, the creator of each quote automatically becomes its owner, and any user who has edited a quote receives full access.

## API support

You can grant or revoke quote-managed access through API calls. You can also use the API to retrieve the list of quotes a user can access and to return a history of users who were granted or revoked access. For a Postman collection of ServiceNow Quote Experience access control API calls, contact support.

