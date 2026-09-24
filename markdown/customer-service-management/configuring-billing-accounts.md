---
title: Billing accounts
description: Billing Account Core application provides a foundational data model for managing billing accounts across organizations and users. It enables businesses to define, organize, and maintain billing relationships, supporting accurate billing, payments, and scalable financial operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/configuring-billing-accounts.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Customer data, Set up your environment, Configure, Customer Service Management]
---

# Billing accounts

Billing Account Core application provides a foundational data model for managing billing accounts across organizations and users. It enables businesses to define, organize, and maintain billing relationships, supporting accurate billing, payments, and scalable financial operations.

## Billing account overview

A billing account is a centralized record that manages payment and invoicing for services. Use billing accounts to organize billing schedules, payment profiles, addresses, currency settings, and to link billing to your customers—individuals or organizations.

Unlike a customer account, which represents the organizational relationship, a billing account is a financial entity specifically for managing billing and payments. A single customer can have multiple billing accounts for different billing arrangements, and you can consolidate charges from multiple accounts under a single parent billing account. Billing accounts support both B2B and B2C scenarios, including complex structures modeled through parent-child hierarchies.

Billing Account Core \(sn\_billing\_account\) is a foundational data model application with no standalone navigation — you work with billing accounts within Customer Service Management. The core tables, fields, billing schedules, and platform roles are available with Billing Account Core. The capabilities that connect a billing account to a customer require the CSM plugins `com.sn_customerservice` and `com.snc.cs_base`. These plugins provide the account, contact, and consumer relationships, related parties, the Address Type field, and the CRM and customer access management \(CAM\) roles.

## Simple use case

A telecommunications customer subscribes to mobile, broadband, and streaming services. Rather than tracking three separate charges, you create one billing account for the customer and:

-   Associate the service location as the billing address.
-   Add a monthly billing schedule so invoices generate on a regular cycle.
-   Add a payment profile with a direct-debit method so that charges are collected automatically.

If a parent company pays the customer's charges, set the paying party to Parent and select the paying billing account. The result is a single record that answers who is billed, for what, when, and how they pay.

## Key capabilities

-   Billing schedule: Define billing frequency \(monthly, quarterly, annual\) and billing cycles.
-   Bill-to address and currency: Specify invoice delivery address and billing currency.
-   Customer associations: Link billing accounts to customers, contacts, and households.
-   Hierarchy support: Create parent-child structures for consolidated billing, sub-accounts, or delegated payment responsibilities. The billing account hierarchy visualization shows these relationships as a tree on the billing account form so that you can review the structure and move between related billing accounts without leaving the record.

    You can view and navigate these relationships from the billing account form. The hierarchy appears following the Description field on the Default and Case views. It shows the parent billing account, the child billing accounts, and identifies the billing account you're currently viewing. From the hierarchy, you can:

    -   Expand or collapse nodes to show or hide child billing accounts.
    -   Select a billing account in the tree to open that record.

## When to use billing account

Use billing accounts when your organization needs to:

-   Separate billing from customer relationship management
-   Support multiple billing arrangements for a single customer
-   Consolidate charges from multiple business units, geographies, or product lines
-   Manage payment responsibility separately from service consumption
-   Track billing-related cases and interactions distinct from general customer cases

**Related topics**  


[billing-account-data-model]

[Data management for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-data-management.md)

