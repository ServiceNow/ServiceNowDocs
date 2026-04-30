---
title: Approval with e-signature
description: Approve or reject an approval record by re-entering your login credentials. See the history of an approval from its activity stream or its audit history.
locale: en-US
release: zurich
product: Approvals
classification: approvals
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Classic approvals, Build workflows]
---

# Approval with e-signature

Approve or reject an approval record by re-entering your login credentials. See the history of an approval from its activity stream or its audit history.

## Support for Title 21 Code of Federal Regulations \(CFR\) Part 11

The Approval with e-signature plug-in is validated for Title 21 CFR Part 11 electronic signature requirements. This plug-in is required for compliance to 21 CFR Part 11.

Each time someone approves a record, the system stores this information.

-   The printed name of the signer
-   The date and time when the signature was made
-   The meaning of the signature \(approval or rejection\)

This information is stored as part of the activity stream and audit history of the record.

## Approval tables

By default, Approval with e-signature supports these tables.

-   Change Request \[change\_request\]
-   Standard Change Proposal \[std\_change\_proposal\]

When you add an approval table, any approval for the table needs an e-signature authorization. See [Select an approval table](../task/t_SelectAnApprovalTable.md) to add or remove a table from supporting Approval with e-signature.

## Approver Authentication dialog

Approvers must enter their user credentials to change the approval state. If the credentials fail, then the approval remains unchanged. The system checks the user credentials against local user records or an active single sign-on integration.

![Dialog to enter user credentials](../image/approval-authentication-dialog-cropped.png)

## Approval History

Each Approval \[sysapprover\_approver\] record has an activity stream that tracks changes to it. Approvals made by e-signature are stored as field changes.

![Example approval showing Bow Ruggeri approving a change request](../image/activity-stream-approval.png "Example activity stream")

## Available approval options

The Change Request \[change\_request\] table provides these approval options.

-   **List options**

    The Change Request table provides context menu options to approve or reject records. When someone selects either the Approve or Reject context menu option, the system displays the Approver Authentication confirmation dialog.

-   **UI actions**

    The Change Request form provides UI actions to approve or reject a record. When someone selects either the Approve or Reject UI action, the system displays the Approver Authentication confirmation dialog.

-   **Change record state**

    The Change Request table provides a State field to approve or reject a record. When someone selects either the Approved or Rejected state, the system displays the Approver Authentication confirmation dialog.


## User credential sources

Approval with e-signature supports these types of user credential sources.

-   A set of local User \[sys\_user\] records.
-   A remote identity provider service accessed by the Multi-Provider Single Sign-On \(SSO\) integration.

User credentials must be set up before enabling Approvals with e-signature. See [Creating users](https://www.servicenow.com/docs/access?context=ua-creating-users&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) to create local User records.

See [Multi-Provider single sign-on \(SSO\)](https://www.servicenow.com/docs/access?context=c_MultipleProviderSingleSignOn&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) to create an integration to a Security Assertion Markup Language \(SAML\) 2.0 identity provider.

