---
title: Major, candidate, and child cases
description: Major issue management uses major case candidates to identify potential issues that impact multiple customers. With approval, candidate cases are promoted to major cases, which you can use to manage issues to resolution. Child cases are created for customers impacted by an issue and are associated with the corresponding major case.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Major issue management overview, Administer Customer Service Management, Customer Service Management]
---

# Major, candidate, and child cases

Major issue management uses major case candidates to identify potential issues that impact multiple customers. With approval, candidate cases are promoted to major cases, which you can use to manage issues to resolution. Child cases are created for customers impacted by an issue and are associated with the corresponding major case.

## Major cases

A major case contains information about a specific issue that impacts multiple customers. It is not associated with any accounts, contacts, or consumers. This customer-specific information resides in the child cases associated with the major case.

The recipients list associated with the major case identifies customers impacted by the issue. Select a list in the **Affected Customers** field in the Major Case Information form section of the Major Case form. After adding the list, you can automatically create child cases for all customers on the list. These cases are added to the **Child Cases** related list on the Major Case form.

With [synchronization](major-candidate-child-case-types.md#section_lx3_1tv_ndb) enabled, updates to the parent major case are automatically synchronized to the associated child cases. When the major case is closed, the associated child cases in the following states are also closed: New, Open, Awaiting Customer Info.

To identify major cases in the list view, check the value in the **Major case state** field.

-   Major cases have a state of Accepted.
-   Major case candidates have a state of either Proposed or Rejected.
-   Regular cases have a blank value.

In the form view, major cases and major case candidates display the Major Case Information form section.

**Note:** Related links on a major case form do not synchronize to associated child cases.

## Major case candidates

A customer service agent uses a major case candidate, or candidate case, to flag an issue that could be a wider issue impacting multiple customers. An agent can create a major case candidate in the following ways:

-   By promoting an existing customer service case with a reported issue to a major case candidate.
-   By creating a new major case candidate.

A major case candidate requires the approval of the customer service manager or major case manager before being promoted to a major case.

-   If a major case candidate was promoted from an existing case, a new major case is created and the candidate case becomes a child case of that major case.
-   If a new major case candidate was created directly, that same case becomes the major case.

If a major case candidate is rejected, it reverts to a regular case.

## Child cases

Child cases are associated with a major case. One child case is created for each account \(B2B\) or consumer \(B2C\) impacted by the major case issue. Child cases are created from the recipients list on the major case and can also be added manually by the major issue manager.

When child cases are created, the short description from the major case is copied to each of the child cases. Duplicate child cases are not created. If a child case already exists for an account or consumer, it is not created again.

As child cases are created, you can enter text in a pop-up window that is added to the **Additional comments** field on the child case form. These comments are added only to the newly created child cases. The major case and any existing associated child cases are not updated.

The primary contact for an account is the contact on the child case and is automatically added to the child case watchlist.

## Synchronization between major cases and associated child cases

The system administrator can set system properties that enable or disable the synchronization between the major case and associated child cases and also define the fields to synchronize. Synchronization occurs from the major case to the child cases. If the state of a child case is Resolved, Closed, or Canceled, the synchronization does not take place.

A major case and the associated child cases maintain synchronization on the fields identified by the **sn\_customerservice.case\_fields\_to\_sync** property. This property specifies the list of fields to synchronize from the major case to the associated child cases. By default, these fields include:

-   Priority
-   State
-   Comments
-   Work notes
-   Close notes
-   Resolution code

If the **State** field is synchronized from the major case to the child cases, the **Close notes** and **Resolution code** fields must also be synchronized.

**Note:** Child cases can be manually added to a major case at any time. There is no retroactive synchronization for newly added child cases.

When synchronization is enabled, saving changes to a major case results in a pop-up window. Verify the update by clicking **OK**.

**Note:** In the base system, parent-child case synchronization is available only for the Case table \(sn\_customerservice\_case\). This feature must be configured for tables that extend the Case table.

