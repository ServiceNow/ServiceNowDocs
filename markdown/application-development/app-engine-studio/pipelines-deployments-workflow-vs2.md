---
title: Pipelines and Deployments workflow version 24.1.2
description: As you manage requests for app deployment in App Engine Management Center \(AEMC\), use this workflow to understand how app deployments move through your pipelines in version 24.1.2, released in November 2023.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Managing app deployments using Pipelines and Deployments, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Pipelines and Deployments workflow version 24.1.2

As you manage requests for app deployment in App Engine Management Center \(AEMC\), use this workflow to understand how app deployments move through your pipelines in version 24.1.2, released in November 2023.

![Infographic depicting a standard Pipelines and Deployments workflow. For a text description, refer to the workflow steps that follow.](../image/pipelines-flow-vs2.png "Pipelines and Deployments workflow")

In this workflow:

1.  The requester selects **Submit** in App Engine Studio, which triggers the main flow.
2.  The system performs the following tasks behind the scenes:
    1.  Validates the payload.
    2.  Fetches the App Manifest from the **sys\_app** record on the source instance.
    3.  Creates a deployment request on the controller instance.
    4.  Sends an email from the controller instance to notify the requester that the request was created.
    5.  Publishes the application to the Application Repository.
3.  The system performs different actions depending on if there are errors or not during publication.
    1.  If there are errors in the app publication, and the error severity is **Error**, then the system creates and waits for approval for the updated record.
    2.  If there are no errors, or if there are errors, but the error severity isn’t **Error**, then the system looks up the next environment on the Pipeline record.
        1.  If the next environment doesn’t exist, the system sends an email from the Controller instance to notify the requester that the request was closed and the app has been published to the target instance. This action ends the workflow.
        2.  If the next environment does exist, the system updates the **Target environment** field on the deployment request to the next environment. Then, the system creates and waits for approval for the updated record.
4.  The system performs different actions depending on if the new record was approved.
    1.  If the record isn’t approved, the system sends an email from the Controller instance to notify the requester that the request wasn’t approved and the request has been closed. This action ends the workflow.
    2.  If the record is approved, and if the **Target environment** is **Testing**, then the system performs the following actions:
        1.  Deploys app to test environment, if the app is not available there.
        2.  Runs the Scoped App Definitions Instance Scan and any other suites on the Scan Suites \[\[scan\_suites\]\] table on the Testing instance.

            **Note:** The Scan Suites table should be populated on the Controller instance.

        3.  Runs the Application Deployment Test Suite Automated Test Framework \(ATF\) suite and any suites on the Scan Suites \[scan\_suites\] table on the Testing instance.
        4.  Writes Instance Scan and ATF test results to the Deployment Environment Result table and to the Activity Stream on the deployment request.
        5.  Returns the workflow to step 3, where it checks for errors.
    3.  If the record is approved, and the **Target environment** is **Production**, the app begins the scheduled deployment process with Change Management integration.
        1.  The App Engine Admin selects **Approve &amp; Create Change request**. A change request is created based on the template chosen during Guided Setup.
        2.  The system performs different actions depending on if the app is registered as a configuration item \(CI\).
            1.  If the app is not registered as a CI, the system registers the app as a CI and then adds the affected CI to the change request.
            2.  If the app is registered as a CI, the system adds the affected CI to the change request.
        3.  The system performs different actions depending on if the change request is in the **Implement** state.
            1.  If the change request state is not **Implement**, and the state is not **Assess** or **Authorize**, the system sends an email from the Controller instance to notify the requester that their request was not approved and has been closed. This ends the workflow.
            2.  If the change request state is not **Implement**, and the state is **Assess** or **Authorize**, the system waits for the state to be **Implement**.
            3.  If the change request is in the **Implement** state, the system creates a change task to schedule the app deployment.
        4.  If the change request state is **Implement** and the **Planned Start Date** is not **Now** or in the past, the system waits for those two conditions to be true
        5.  If the change request state is **Implement** and the **Planned Start Date** is **Now** or in the past, but the request is **Rejected** or **Cancelled**, the system sends an email from the Controller instance to notify the requester that their request was not approved and has been closed. This ends the workflow.
        6.  If the change request state is **Implement** and the **Planned Start Date** is **Now** or in the past, the system schedules the app deployment to Production based on the **Planned Start Date** in the change request. The system closes the change task, and then closes the deployment request. This ends the workflow.
    4.  If the record is approved, and the **Target environment** isn’t **Testing** or **Production**, then the system deploys the app to the target environment, if it isn't available there.

        The workflow starts over when a requester selects **Submit** again in App Engine Studio.


**Parent Topic:**[Managing app deployments using Pipelines and Deployments](../../app-engine-studio/concept/aes-review-apps-p-and-d.md)

