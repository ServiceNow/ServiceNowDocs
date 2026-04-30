---
title: Automated Test Framework use case: test a Service Catalog request
description: This use case illustrates testing a service catalog request with the Automated Test Framework.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Automated Test Framework use case examples, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Automated Test Framework use case: test a Service Catalog request

This use case illustrates testing a service catalog request with the Automated Test Framework.

## Before you begin

Role required: atf\_test\_admin

## About this task

With the Replay Request Item test step, you can test the service catalog ordering process once a request exists and has a record in the request item table. In the Xanadu release, you cannot create an automated test for the process by which the user creates a new request.

![Test steps](../image/atf-use-serv-cat.png "Automated Test Framework: Service catalog example")

## Procedure

1.  Replay an existing service catalog request item.

    This test step inserts a new record in the \[sc\_request\] table for the catalog request item RITM0010001.

    ![Replay request item](../image/atf-use-sc-step-01.png "Service Catalog test step 1 details: Replay Request Item")

    This insertion triggers the Service Catalog Request workflow, which checks the price of the item, determines that it exceeds $1000.00, and therefore generates approval records for users belonging to the Catalog Request Approvals group. In this example, only one user– Eric Schroeder – belongs to this group.

    ![Service catalog request workflow](../image/atf-use-sc-scrwf-a.png "Screenshot of triggered Service Catalog Request workflow")

2.  Impersonate Eric Schroeder, the user who needs to approve this Service Catalog Request.

    ![Impersonate test step](../image/atf-use-sc-step-02.png "Test step - Impersonate Eric Schroder")

3.  Verify that the system created an approval record for Eric Schroeder and this request.

    Note that for the **Approval for** field, you assign the output value from Step 1.

    ![Record query test step](../image/atf-use-sc-step3.png "Step 3 details: Record Query for Approval record")

4.  Set the state of this approval record to Approved.

    ![Update setting approval state](../image/atf-use-sc-step-04.png "Step 4 details: set approval record to Approved")

    The Service Catalog Request workflow sees that all required approval records have the state of Approved and transitions to the Approval Action which marks the request record \[sc\_request\] as Approved.

    ![Sc workflow with approval portion highlighted](../image/atf-use-sc-scrwf-b.png "Step 4: Triggered workflow marks request record as approved")

    When the record in \[sc\_request\] changes to the Approved state, an associated business rule generates request items \[sc\_request\_item\] for each item in the request. In this example, the request contains only one item, so the business rule inserts one record into the \[sc\_request\_item\] table. This insertion triggers the Service Catalog Item Request workflow.

    ![Service catalog item request workflow](../image/atf-use-sc-item-wf.png)

    The first activity in the Service Catalog Item Request workflow generates an approval record for the head of the department in which the requesting user works. In this example, the department head is Natasha Ingram.

    ![Service catalog item workflow](../image/atf-use-sc-ir-01.png)

5.  The workflow does not continue until the department head approves it, so the next test step impersonates Natasha Ingram.

    ![Impersonate user test step](../image/atf-use-sc-step-05.png "Step 5 - Impersonate User")

6.  Obtain the sys\_id for the new approval record with the Record Query step.

    Note that Record Query creates an output variable with the sys\_id of the first record returned from the query.

    ![Record query test step](../image/atf-use-sc-step-06.png "Step 6 - Record Query test step")

7.  Set the approval record to Approved.

    ![Approval user test step](../image/atf-use-sc-step-07.png "Step 7 - Approval User test step")

    Note how Step 7 refers to the **First record**output variable from Step 6 to specify which record to approve. When the record is approved, the workflow transitions to the next Approval - User activity, which generates an approval record for the CIO. In this example, the CIO is Bow Ruggeri.

    ![Service catalog item workflow](../image/atf-use-sc-ir-02.png)

8.  Impersonate Bow Ruggeri.

9.  Obtain the sys\_id for the approval record for Bow Ruggeri.

10. Set the approval record to Approved.

    When the record is approved, the workflow transitions to the Approval Action activity which sets the record for this item in the \[sc\_request\_item\] table to **Approved**. The workflow transitions to the Catalog Task activity labelled Asset Mgmt. Fulfills Order. This Catalog Task activity generates a new record in the \[sc\_task\] table that instructs a user in the Fulfillment group to order the item.

    ![Service catalog item workflow](../image/atf-use-sc-ir-03.png "Step 10 - Service Catalog Item workflow")

11. Impersonate a user in the Fulfillment group, in this example ATF.User.

    ![Impersonate user test step](../image/atf-use-sc-step-11.png "Step 11 - Impersonate User test step")

12. Obtain the sys\_id for the new catalog task with the Record Query step.

    Note that Record Query creates an output variable with the sys\_id of the first record returned from the query.

    ![Record query test step](../image/atf-use-serv-cat-step12.png "Step 12 - Record Query test step")

13. Mark the \[sc\_task\] record as **Closed Complete**.

    ![Record update test step](../image/atf-use-sc-step-13.png "Step 13 - Record Update test step")

    Note how Step 13 uses the **First record**output variable from Step 12 to specify which record to mark as **Closed Complete**.

    When the record is marked **Closed Complete**, the workflow exits the Catalog Task activity along the In Stock exit path.

    ![Service catalog item request workflow](../image/atf-use-sc-ir-04.png "Step 13 - Service Catalog Item Request workflow")

    The workflow transitions to the Notification activity, then to the Catalog Task activity labelled Deploy Item to User.The Deploy Item to User Catalog Task activity inserts a new record into the \[sc\_task\] table that instructs a user in the Deployment group to deliver the item.

14. Obtain the sys\_id for the new catalog task with the Record Query step.

    Note that Record Query returns an output variable with the sys\_id of the first record returned from the query.

    ![Record query test step](../image/atf-use-sc-step-14.png "Step 14 - Record Query test step")

15. Mark the \[sc\_task\] record as Closed Complete.

    Note how Step 15 uses the **First record**output variable from Step 14 to specify which record to mark as Closed Complete.

    ![Record update test step](../image/atf-use-sc-step-15.png "Step 15 - Record Update test step")

    When the record is marked Closed Complete, the workflow exits the Catalog Task activity, logs a message, and exits.

    ![Service catalog item request workflow](../image/atf-use-sc-ir-05.png "Step 15 - Service Catalog Item Request workflow")

16. Verify that the request item in \[sc\_request\_item\] has the state Closed Complete.

    ![Record validation dialog](../image/atf-use-sc-step-15.png "Step 15 details - Record Validation")

17. Verify that the request \[sc\_request\] has the state Closed Complete.

    ![Record validation test step](../image/atf-use-sc-step-16.png "Step 16 - Record Validation test step")


**Parent Topic:**[Automated Test Framework use case examples](../concept/atf-use-cases.md)

**Related topics**  


[Replay Request Item](../reference/test-steps-server-category.md#)

