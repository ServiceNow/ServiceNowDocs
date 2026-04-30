---
title: Domain separation and entity relationships
description: With domain separation in Customer Service Management, you can further control visibility and access to data by using contact, partner, and parent-child relationships.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Domain separation and Customer Service Management, Administer Customer Service Management, Customer Service Management]
---

# Domain separation and entity relationships

With domain separation in Customer Service Management, you can further control visibility and access to data by using contact, partner, and parent-child relationships.

## Partner-customer account relationships

In partner-customer account relationships, the partner account can see data in the customer account’s domain. When setting up an account relationship, the domain visibility direction is **From &gt; To**. The account in the **From** field contains the domain of the account in the **To** field.

When a partner admin creates a case for a customer account, the case is created in the customer account's domain so that all relevant parties can access the case.

In partner-customer account relationships where the customer account has child relationships, the partner admin can create a case for the customer account but not for the child accounts. The partner admin can only create cases for the account with which the relationship has been established.

## Contact relationships

In contact relationships, the contact included in the relationship can see data for the specified account domain.

## Parent-child relationships

The account hierarchy feature creates a parent-child relationship between accounts. This relationship is defined by selecting the parent in the **Parent Account** field on the Account form for the child account. Domain hierarchy is also achieved using the **Parent Account** field. In parent-child account relationships, parent domains can see data in child domains.

To provide access from the child account to the parent account, you need to set domain visibility. Navigate to the child account and set visibility in the Visibility Domains related list \(sys\_user\_visibility\) by connecting the user to the domain.

**Parent Topic:**[Domain separation and Customer Service Management](../concept/domain-separation-customer-service.md)

