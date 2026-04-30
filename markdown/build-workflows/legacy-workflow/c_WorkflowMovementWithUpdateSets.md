---
title: Workflow movement with update sets
description: The system tracks workflows in update sets differently than other records because workflow information is stored across multiple tables.Create a new workflow with no dependencies and then migrate the workflow in an update set.Successfully edit and migrate an existing workflow and its dependent subflow.Edit and migrate an existing workflow from a test instance to a production instance that fails to run on the production instance because of a missing dependent subflow.Multiple users migrate a workflow from a test instance to a production instance without proper coordination. This use case can succeed, but only when each user understands the dependencies and properly migrates the dependent parts of the workflow to the new instance.
locale: en-US
release: zurich
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Workflow administration, Classic Workflow, Build workflows]
---

# Workflow movement with update sets

The system tracks workflows in update sets differently than other records because workflow information is stored across multiple tables.

Changes made to a workflow version are not added to the update set until the [workflow is published](../task/work-on-workflows.md#), at which point the entire workflow is added into the update set. Update sets store workflows as a single Workflow \[wf\_workflow\] record and only retain the latest version with the update type of Workflow.

For information about update sets, see [System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

**Parent Topic:**[Workflow administration](../../workflow/concept/c_WorkflowAdministration.md)

## Workflow update set migration use case - simple

Create a new workflow with no dependencies and then migrate the workflow in an update set.

1.  User A selects Update Set A.
2.  User A creates a new workflow called Workflow A.
3.  User A publishes Workflow A.

    A customer update set record is added to Update Set A containing an XML payload, including the published Workflow A and all activity dependencies. The XML payload also contains the workflow input variables associated with the workflow.

4.  User A completes Update Set A and migrates it to the production instance.
5.  Update Set A commits successfully.
6.  Workflow A works as expected.

## Workflow update set migration use case - subflow dependency \(success\)

Successfully edit and migrate an existing workflow and its dependent subflow.

1.  User A selects Update Set B.
2.  User A checks out Workflow A.
3.  User A adds a subflow called Workflow B to Workflow A.

    Assume that Workflow B was previously published and migrated to the production instance.

4.  User A publishes Workflow A.

    A customer update set record is added to Update Set B containing an XML payload, including the published Workflow A and all activity dependencies. The XML payload also contains the workflow input variables associated with the workflow.

5.  User A completes Update Set B and migrates it to the production instance.
6.  Update Set B commits successfully.
7.  Workflow A works as expected with Workflow B as a subflow.

## Workflow update set migration use case - subflow dependency \(failure\)

Edit and migrate an existing workflow from a test instance to a production instance that fails to run on the production instance because of a missing dependent subflow.

1.  User A selects Update Set C.
2.  User A checks out Workflow A.
3.  User A adds a subflow called Workflow B to Workflow A.

    Assume that Workflow B was previously published, but has not been migrated to the production instance.

4.  User A publishes Workflow A.

    A customer update set record is added to Update Set C containing an XML payload, including the published Workflow A and all activity dependencies. The XML payload also contains the workflow input variables associated with the workflow.

    Notably absent from Update Set C is the subflow called Workflow B. Workflow B was published before User A selected Update Set C.

5.  User A completes Update Set C and migrates it to the production instance.
6.  Update Set C commits with warnings.
7.  Workflow A is invoked on the production instance with the following results:

    Workflow A fails the runtime validation check and is prevented from running on the production system. The system adds to the workflow context a workflow log entry detailing the cause of the failure, notably the absence of a dependent workflow.

    To learn more about the validation checks on workflow dependencies and update sets see [../../workflow-validation/reference/r\_VldtUpdtStDpnd.md](../../workflow-validation/reference/r_VldtUpdtStDpnd.md).


## Workflow update set migration use case - subflow dependency \(risk\)

Multiple users migrate a workflow from a test instance to a production instance without proper coordination. This use case can succeed, but only when each user understands the dependencies and properly migrates the dependent parts of the workflow to the new instance.

This example does not represent an update set failure, although update sets are most often blamed in this use case. Validation increases the visibility of workflow dependencies across multiple update sets and provides designers with better information. In most cases, the warnings do not prevent an action, but only identify risk. The designer is responsible for taking action on advice given in the validation checks.

1.  User A selects Update Set C.
2.  User A checks out Workflow A.
3.  User A adds a subflow called Workflow B that returns a **User ID**.

    **Note:** Assume that Workflow B was previously published and migrated to the production instance.

4.  User A uses the return value of Workflow B to generate approvals.
5.  User B selects Update Set D.
6.  User B checks out Workflow B \(the subflow in Workflow A\).
7.  User B modifies the return value of the workflow by changing it from a **User ID** to a **String Message**.
8.  User A publishes Workflow A.

    **Note:** A dialog box displays warnings associated with Workflow A and encourages User A to validate the workflow before publishing.

9.  User A cancels publishing and [validates](../../workflow-validation/concept/c_WorkflowValidation.md) Workflow A.
10. User A is warned that Workflow B was modified by a user in a different update set.
11. User A ignores this warning and publishes Workflow A.

    **Note:** A customer update set record is added to Update Set C containing an XML payload, including the published Workflow A and all activity dependencies.The XML payload also contains the workflow input variables associated with the workflow.

12. User A completes Update Set C and migrates it to the production instance.
13. Workflow A is invoked on the production instance and runs successfully using the older version of Workflow B already on the system.
14. User B publishes Workflow B.

    **Note:** User B is not warned of the Update Set C dependency, because the update set is no longer In progress. However, User B is informed via a dialog box that there are warnings associated with the workflow version and is instructed to validate Workflow B. If User B cancels publication and validates the workflow, User B is warned that there are workflows that use Workflow B as a subflow. Knowing the return value was changed, User B should test those workflows as well. See [../../workflow-validation/reference/r\_VldtUpdtStDpnd.md](../../workflow-validation/reference/r_VldtUpdtStDpnd.md) to understand the parameters of update set warnings.

15. User B finally publishes Workflow B.

    **Note:** A customer update set record is added to Update Set D containing an XML payload, including the published Workflow B and all activity dependencies.

16. User B completes Update Set D and migrates it to the production instance.
17. Update Set D commits without warnings.
18. Workflow A is invoked on the production instance and fails to run successfully, because the return value of Workflow B no longer generates a User ID.

