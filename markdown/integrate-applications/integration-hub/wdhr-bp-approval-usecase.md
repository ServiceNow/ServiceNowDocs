---
title: Business process change for the approval use case
description: Perform business process change for all the required business processes and for definitions \(default definition and org based definition\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/wdhr-bp-approval-usecase.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-12-04"
reading_time_minutes: 1
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Business process change for the approval use case

Perform business process change for all the required business processes and for definitions \(default definition and org based definition\).

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the business process which you want to include and navigate to **Actions** &gt; **Business Process Policy** &gt; **Edit**.

    \[Omitted image "wdhr-bp-approval-usecase-1.jpg"\] Alt text: Edit the business process definition.

2.  Select ISSG created for ISU in **Security Groups** under **Action** as **Approve**.

    \[Omitted image "wdhr-bp-approval-usecase-2.jpg"\] Alt text: Select ISSG.

3.  Search for **Activate Pending Security Policy Changes** Task, enter comment in comment box and click **OK**.

    \[Omitted image "wdhr-bp-approval-usecase-3.jpg"\] Alt text: Activate pending security policy changes.

4.  Select the **Confirm** check box and click **OK**.

    \[Omitted image "wdhr-bp-approval-usecase-4.jpg"\] Alt text: Confirm the changes.

5.  Navigate to the business process and navigate to **Actions** &gt; **Business Process** &gt; **Edit definition**.

    \[Omitted image "wdhr-bp-approval-usecase-5.jpg"\] Alt text: Edit definition.

6.  Select the effective date and click **OK**.

    \[Omitted image "wdhr-bp-approval-usecase-6.jpg"\] Alt text: Select the effective date.

7.  Select Integration system security group created for approval use case in group column of all approval steps.

    **Note:** Do not remove already assigned sec group.

    \[Omitted image "wdhr-bp-approval-usecase-7.jpg"\] Alt text: Select integration system security group.

8.  Include additional **Service type** step in between two Approval steps and select **Step Configuration Placeholder Service**.

    \[Omitted image "wdhr-bp-approval-usecase-8.jpg"\] Alt text: Include additional service type step.

    These are Workday IDs of the business processes for use case.

    |Usecase|Business process|Workday ID|
    |-------|----------------|----------|
    |Time off|Request Time Off|cd0c4190446c11de98360015c5e6daf6|
    |Termination|Termination|cd09bb46446c11de98360015c5e6daf6|
    |Submit Resignation|939f15e2eb371000099ebe0876cd932b|
    |Correct time off|Correct Time Off|cd0c42da446c11de98360015c5e6daf6|
    |Job requisition|Job Requisition|956972d0179342df82c26bb0781d9660|
    |Change job|Change Job|c24592468ed147b2ac6d0de4d699a7da|
    |Leave of absence|Request leave of absence|cd0c14d6446c11de98360015c5e6daf6|
    |Compensation change|Propose Compensation Hire|cd0a03bc446c11de98360015c5e6daf6|
    |Change Default Compensation|cd0cabbc446c11de98360015c5e6daf6|
    |Requisition Compensation|448e44df783a100005ba3ddd7e1a021c|
    |Propose Compensation Change|cd0a18a2446c11de98360015c5e6daf6|
    |Request Compensation Change|cd09f2e6446c11de98360015c5e6daf6|
    |Request Compensation Change for Leave of Absence|6766cfa1f9444f9ab8dffbff5ba87b50|

    Workday ID of **In Progress** event status is e2d08afc53614c37b32b31270bb8bee3.


