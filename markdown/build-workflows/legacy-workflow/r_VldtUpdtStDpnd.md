---
title: ValidateUpdateSetDependencies
description: The ValidateUpdateSetDependencies validator identifies all the subflows called in the current workflow and determines if any of those subflows are being edited in a different \(in progress\) update set.
locale: en-US
release: xanadu
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Workflow validator, Workflow validation, Workflow management, Classic Workflow, Build workflows]
---

# ValidateUpdateSetDependencies

The **ValidateUpdateSetDependencies** validator identifies all the subflows called in the current workflow and determines if any of those subflows are being edited in a different \(in progress\) update set.

This warning informs the user that this workflow and one or more of its dependencies are being actively modified in a way that will not deploy concurrently to another instance without additional effort.

For information about update sets, see [Create and select an update set](https://www.servicenow.com/docs/access?context=create-select-update-set&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

## Validation summary

-   Risk: If a parent workflow is edited in one update set and its dependent subflow is edited in another, the two workflows might not be compatible when moved to a different instance. Making independent changes, such as to common or expected values, can make the two workflows incompatible.
-   Severity Level: Warning
-   Valid Result: Valid
-   Valid Message: There were no Update Set dependency issues found.
-   Invalid Result: Invalid
-   Invalid Message: This workflow has dependent workflows that are in a different update set.
-   Suggested Action: Modify and deploy both workflows in the same update set. If you must modify dependencies in separate update sets, use one of these methods:
    -   Ensure that all update sets migrate concurrently.
    -   Prior to deploying the main flow update set, merge the dependencies into one update set before completing that update set.
-   Publishable: Yes
-   Runnable: Yes
-   Related Information: [Workflow movement with update sets](../../workflow-administration/concept/c_WorkflowMovementWithUpdateSets.md#)

## Troubleshooting

A workflow is added to an update set only when the workflow is published. This validator issues a warning when either of the following conditions exist:

-   A published subflow is in a different update set than the parent workflow and that update set is In progress.
-   A subflow is checked out by another user, who is working in a different update set than the current user.

**Note:** This validator does not look for update sets that have been closed. It looks only at update sets that are In progress or at the update sets of all subflows being used by the current workflow that are checked out to users who are working in a different update set.

## Example

Following is an example of an at-risk development scenario in which two users create dependencies between workflows in different update sets.

User A:

1.  Sets Update Set A to the current update set.
2.  Checks out Workflow A.
3.  Changes the return value of the **String** type in Workflow A to a **Reference/User** type.
4.  Publishes Workflow A, causing an entry into Update Set A.

User B:

1.  Sets Update Set B to the current update set.
2.  Checks out Workflow B.
3.  Includes Workflow A as a subflow.
4.  Uses the user reference return value from Workflow A as an approval assignment.
5.  Publishes Workflow B, causing an entry into Update Set B.

## Risks

-   User B moves Update Set B to a different instance that has an older version of Workflow A. The return value is not a user reference, which causes the outcome of Workflow B to be different than it was when tested in development.
-   User B moves Update Set B to a new instance that does not have a version of Workflow A. Workflow B experiences a validation failure at runtime and cannot execute. A log entry is added to the workflow log of the current record.

## Possible solutions

Solution 1

Migrate the parent workflow and all dependent workflows to a new instance together using the same update set.

1.  Set the update set to the one you want to migrate to new instances.
2.  Check out and republish the workflows that need to be included, this action forces an entry into the current update set.
3.  Complete the update set with all dependencies.
4.  Follow standard procedures for migrating update sets to local instances.

Solution 2

Move dependent workflows between update sets.

1.  Identify the update set containing the main workflow to be migrated.
2.  Navigate to **System Update Sets &gt; Local Update Sets**.
3.  Find and select the update set that contains the dependencies to the main workflow.
4.  In the **Customer Updates** related list, select the workflow version of the subflow you want to move.
5.  Select the update set containing the parent workflow in the **Update set** field. If this field is not on the Customer Update form, configure the form and add the field.
6.  Click **Update** and the base system moves the dependent subflow to the update set selected.
7.  Repeat steps 4-6 to add additional dependent subflows to the parent flow update set.

**Parent Topic:**[Workflow validator](r_WorkflowValidator.md)

