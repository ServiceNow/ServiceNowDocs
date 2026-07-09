---
title: Add an existing case as a child to a major case
description: A major issue manager can add an existing case as a child to an accepted major case, either by selecting from a list of cases or by adding a case from the Suggested child cases related list.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/add-existing-case-to-major-case.html
release: australia
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 2
breadcrumb: [Major issue management overview, Manage cases, Use, Customer Service Management]
---

# Add an existing case as a child to a major case

A major issue manager can add an existing case as a child to an accepted major case, either by selecting from a list of cases or by adding a case from the **Suggested child cases** related list.

## Before you begin

Role required: sn\_majorissue\_mgt.major\_issue\_manager, sn\_customerservice\_manager

## About this task

There are two ways to add child cases to an accepted major case:

-   **From the Child Cases related list**: Search for and select any existing case that is not already a major case.
-   **From the Suggested child cases related list**: Add one or more cases that the AI detection workflow has identified as potential members of the major case group.

## Procedure

1.  Add a case from the Child Cases related list
2.  Open the desired major case.

3.  In the **Child Cases** related list, select **Add** to display the Add Child Cases pop-up window.

4.  The Add Child Cases pop-up window displays a list of customer service cases that are not major cases.

5.  Use the filters to narrow the list of cases displayed in the window.

6.  Select the cases to add to the major case by enabling the check box for each case.

7.  Select **Submit**.

    The system evaluates the selected cases and adds none, some, or all cases to the **Child Cases** related list. A message on the major case form informs you of the results by displaying one of the following:

    -   No selected cases were added as child cases.
    -   \(x\) of \(y\) selected cases were added as child cases.
    -   All \(y\) selected cases were added as child cases.
    A work note is added to the **Activities** field for each child case added to the major case.

8.  Add a case from the Suggested child cases related list: Use this method when the AI detection workflow has identified cases as potential members of the major case group. These cases appear in the **Suggested child cases** related list.
9.  Open the accepted major case.

    **Note:** The **Add to major case** action is only available when the major case state is **Accepted** and the case is in a non-terminal state.

10. In the **Suggested child cases** related list, select the check box for one or more cases to add.

11. Select **Add to major case**.

    The selected cases are removed from the **Suggested child cases** list and added to the **Child Cases** related list. A confirmation message is displayed when the action succeeds.


**Related topics**  


[Recipients lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/major-issue-recipient-lists.md)

