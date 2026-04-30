---
title: Enable external customers to access problem, change, and request records
description: With access to problem, change, and request records, external customers can view these records associated with their customer service cases from the Customer and Consumer Service Portals.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setting up CSM integration with IT Service Management, Integrating with IT Service Management, Integrating Customer Service Management with other applications, Customer Service Management]
---

# Enable external customers to access problem, change, and request records

With access to problem, change, and request records, external customers can view these records associated with their customer service cases from the Customer and Consumer Service Portals.

## Before you begin

Role required: admin

## About this task

Users with the snc\_internal or snc\_external role and with read access to the related problem, change, and request records can view these records from the Customer and Consumer Service Portals. After logging in, users can:

-   Select a case and view the records related to that case in the Case Related Records widget.
-   Click a record in the Case Related Records widget to open the record details in the Ticket Fields widget.

**Note:** The Related Records list shows data only if the logged in user has access to view the related records.

Customers, customer partners, and internal users with the proxy contact role \(sn\_customerservice.proxy\_contact\) can also create requests from the Customer and Consumer Service Portals. For more information about this feature, see [Create cases as a proxy contact](../concept/employee-create-case-for-customer.md).

Customers can also view Known Error articles for a problem related to a case. These articles are displayed:

-   If there is a KE article present for the problem record. If there are multiple articles associated with the problem, the customer has access to the primary article. If there are no articles, the customer does not see the link.
-   If the customer has access to the KE article.

## Procedure

1.  Provide access to problem, change, and request records by configuring ACLs for the snc\_external role.

    This access is not provided out of box. You must add these ACLs to the snc\_external user role based on case access. For more information, see [Access control list rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

    **Note:** Existing ACLs on the problem, change, and request records may impact the visibility for external users.

2.  Configure the Case Related Records widget.

    By default, this widget is displayed for users with the snc\_internal and snc\_external roles. For more information, see [Service Portal widgets](https://www.servicenow.com/docs/access?context=service-portal-widgets&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

3.  Define the views for the problem, change, and request records and select the fields that are visible to external customers.

    For more information, see [Create and delete views](https://www.servicenow.com/docs/access?context=create-delete-view&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

    **Note:** For the Consumer Service Portal, you can define views and select fields for problem and change records. Request records display a default set of fields in the Ticket Fields widget.


