---
title: CPQ Support Team access to customer Salesforce sites
description: Learn how CPQ support team members can securely access customer Salesforce and CPQ Admin environments for troubleshooting. This article outlines recommended access methods, user-management practices, and considerations for customers with stricter security policies.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# CPQ Support Team access to customer Salesforce sites

Learn how CPQ support team members can securely access customer Salesforce and CPQ Admin environments for troubleshooting. This article outlines recommended access methods, user-management practices, and considerations for customers with stricter security policies.

This document outlines the standard processes for CPQ support team members to gain access to customer environments. These procedures ensure secure, efficient support while maintaining appropriate access controls.

**Note:** Some enterprise customers have stricter security policies that prohibit direct access to their environments, requiring support methods other than those described here.

## Salesforce user access

When support requires access to a customer's Salesforce environment, customers can create a Salesforce user with an email address of provisioning@logik.io and system administrator permissions. This ensures that every member of our support team has access, not just the one currently working on your case.

For assistance with this process, see Salesforce's official documentation: [Adding New Users in Salesforce](https://help.salesforce.com/s/articleView?id=platform.adding_new_users.htm&type=5)

## CPQ Admin access

Support team members may need access to CPQ Admin in customer environments. To learn how to grant access, see [User Access](https://customer.help.logik.io/servicedesk/customer/portal/4/article/1614643465).

## User management

There is no standard timeline for access removal. Customers can modify access levels by changing CPQ support users to End User or by deactivating the SFDC user.

In test environments, many customers let our provisioning user stay active indefinitely. Some utilize our user as the integration user for product/pricebook synchronization, which lets us troubleshoot more quickly because we can directly investigate the issue.

During a support case, disabled user accounts can be reactivated upon request.

**Parent Topic:**[CPQ reference](../reference/servicenow-cpq-reference.md)

