---
title: Enable external customers to approve requests and changes
description: Enable your external customers to approve change and request records related to customer service cases from the Customer Service Portal.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-08-08"
reading_time_minutes: 1
breadcrumb: [Setting up CSM integration with IT Service Management, Integrate with IT Service Management, Integrate, Customer Service Management]
---

# Enable external customers to approve requests and changes

Enable your external customers to approve change and request records related to customer service cases from the Customer Service Portal.

## Before you begin

Role required: admin

## About this task

Changes and requests related to a case typically require end user approval before the tasks can be completed. The tasks can be initiated by customers and by external users. For example:

-   A customer creates a change in order to apply a patch. This change requires approval from the contact before the patch can be applied.
-   A contact requests a catalog item from the Customer Service Portal. This request requires approval by another employee within the contact's organization before the request can be fulfilled.

Use this feature to send approval requests and enable external customers with the snc\_external role to approve those requests as part of the task approval workflow. From the Customer Service Portal, external customers can:

-   View and approve requests and change requests.
-   View the details of the requested items in a request record.
-   View the status of a request or change request in the Related Records widget.

**Important:** Approving requests and changes requires the approver\_user role, which is a licensed role. For more information, see [KB0716592](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0716592).

## Procedure

1.  Add external users to approval groups or assign roles for approval users in order to see approval records on the Customer Service Portal.

2.  Add the necessary ACLs to the snc\_external role for the following tables.

    -   Change Request \(change\_request\)
    -   Request \(sc\_request\)
    -   Request Item \(sc\_req\_item\)
    **Note:** The sn\_esm\_user role provides access to the approval records where the logged-in user is the approver and enables the logged-in user to either approve or reject the approval request. Customer Service Management requester roles \(including the customer contact, partner contact, customer admin, and partner admin roles\) contain the sn\_esm\_user role, which enables these roles to perform the approve and actions.

    For more information, see [Table ACL rules](https://www.servicenow.com/docs/access?context=acl-rule-types&version=zurich&pubname=zurich-platform-security&ft:locale=en-US#section_tjv_xcn_l1b) and [Field ACL rules](https://www.servicenow.com/docs/access?context=acl-rule-types&version=zurich&pubname=zurich-platform-security&ft:locale=en-US#section_tgm_xcn_l1b).


