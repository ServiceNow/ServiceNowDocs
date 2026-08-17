---
title: Major, candidate, and child cases
description: Major issue management uses major case candidates to identify potential issues that impact multiple customers. Managers approve candidate cases for promotion to major cases, which you use to manage issue resolution. The system creates child cases for impacted customers and links them to the corresponding major case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/major-candidate-child-case-types.html
release: australia
topic_type: concept
last_updated: "2026-06-22"
reading_time_minutes: 4
breadcrumb: [Major issue management overview, Manage cases, Use, Customer Service Management]
---

# Major, candidate, and child cases

Major issue management uses major case candidates to identify potential issues that impact multiple customers. Managers approve candidate cases for promotion to major cases, which you use to manage issue resolution. The system creates child cases for impacted customers and links them to the corresponding major case.

## Major cases

A major case contains information about a specific issue that affects multiple customers. The major case itself is not linked to specific accounts, contacts, or consumers. Instead, customer-specific information is stored in the child cases that are linked to the major case.

The recipients list associated with the major case identifies customers impacted by the issue. Select a list in the **Affected Customers** field in the Major Case Information form section of the Major Case form. After adding the list, you can automatically create child cases for all customers on the list. These cases are added to the **Child Cases** related list on the Major Case form.

With [synchronization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/major-candidate-child-case-types.md) enabled, updates to the parent major case are automatically synchronized to the associated child cases. When the major case is closed, the system also closes associated child cases in the following states: New, Open, Awaiting Customer Info.

When the `enable_case_type_for_major_case` property is set to `true`, the system uses the `sys_class_name` of the candidate case to determine the case type of the resulting major case and its child cases, rather than defaulting to the base Case table.

To identify major cases in the list view, check the value in the **Major case state** field.

-   Major cases have a state of Proposed or Accepted.
-   Regular cases have a blank value.

In the form view, major cases and major case candidates display the Major Case Information form section.

**Note:** Related links on a major case form don't synchronize to associated child cases.

## Major case candidates

A customer service agent uses a major case candidate \(also called a candidate case\) to flag an issue that might affect multiple customers. An agent can create a major case candidate in two ways:

-   By promoting an existing customer service case to a major case candidate.
-   By creating a new major case candidate directly.

A customer service manager or major case manager must approve a major case candidate before it can be promoted to a major case.

-   If a candidate case was promoted from an existing case, the system creates a new major case and the candidate case becomes a child case of that major case.
-   If a new candidate case is created directly, that case becomes the major case.

If a major case candidate is rejected, the system reverts it to a regular case.

## Child cases

Child cases are linked to a major case. The system creates one child case for each account \(B2B\) or consumer \(B2C\) that is affected by the major case issue. Child cases are created from the recipients list on the major case, and a major issue manager can also add them manually.

When the system creates child cases, it copies the short description from the major case to each child case. The system does not create duplicate child cases. If a child case already exists for an account or consumer, the system does not create another one.

When you create child cases, you can enter text in a pop-up window. This text is added to the **Work notes** field on the child case form. These comments are added only to the newly created child cases. The major case and any existing child cases are not updated.

The primary contact for an account is automatically added to the child case as a contact and is included on the child case watchlist.

## Suggested child cases

When a major case is in the **Proposed** state, the AI detection workflow populates the **Suggested child cases** related list with cases that have been identified as potential members of the major case group.

As a major issue manager, take the following steps:

-   Review the suggested child cases
-   Use the **Add to major case** action on the **Suggested child cases** related list to add the cases as child cases of that major case.

    **Note:** This action is available only when the major case state is **Accepted** and the case is in a non-terminal state.


When a suggested child case is added to the major case, it is removed from the **Suggested child cases** list and added to the **Child Cases** related list.

When a major case moves to the **Accepted** state, all of the suggested child cases are moved to the **Child Cases** related list.

## Synchronization between major cases and associated child cases

The system administrator can set system properties to enable or disable synchronization between the major case and child cases, and to specify which fields to synchronize. Synchronization is one-directional: it occurs from the major case to the child cases. If a child case is in Resolved, Closed, or Canceled state, synchronization does not occur.

A major case and its child cases maintain synchronization on fields that are identified by the **sn\_customerservice.case\_fields\_to\_sync** property. This property specifies which fields are synchronized from the major case to the child cases. By default, these fields include:

-   Priority
-   State
-   Comments
-   Work notes
-   Close notes
-   Resolution code

If the **State** field is synchronized from the major case to the child cases, the **Close notes** and **Resolution code** fields must also be synchronized.

**Note:** Child cases added to a major case manually can be added at any time. Newly added child cases do not receive synchronization retroactively.

When synchronization is enabled, the system displays a pop-up window when you save changes to a major case. Verify the update by clicking **OK**.

**Note:** In the base system, parent-child case synchronization is available only for the Case table \(`sn_customerservice_case`\). You must configure this feature for tables that extend the Case table.

