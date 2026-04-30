---
title: Deployment Request form in the Pipelines and Deployments app
description: The Deployment Request form is accessed from within the App Engine Studio \(AES\) Pipelines and Deployments app.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [App Engine Studio reference, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Deployment Request form in the Pipelines and Deployments app

The Deployment Request form is accessed from within the App Engine Studio \(AES\) Pipelines and Deployments app.

To view the Deployment Request form, navigate to **All** &gt; **App Engine** &gt; **Pipelines and Deployments** &gt; **Deployment Requests** and open a record.

<table id="id_um3_4hq_rrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number to track the deployment request.

</td></tr><tr><td>

Assignment group

</td><td>

Group to which the deployment request is assigned.

</td></tr><tr><td>

State

</td><td>

State of the deployment request. All states are automatically updated by the pipeline flows:-   **New**

The submitted request is new.

-   **In Review**

The submitted request is ready for review.

-   **Closed - Published**

The submitted request has been deployed to the production instance.

-   **Closed - Rejected**

The submitted request is not ready to publish. This state is enabled when you select **Reject** on the associated approval record at any time during the deployment process. The system then prompts you to include the reason why the application is rejected. These comments are then sent via email to the address included in the **Requestor Email** field on the **Requestor Details** related list.

-   **Closed - Failed**

This state is enabled when any of the pipeline flows or sub-flows fail for any reason.

-   **Canceled**

The submitted request has been canceled.


</td></tr><tr><td>

Assigned to

</td><td>

The user in the assignment group to whom this request is assigned.

</td></tr><tr><td>

Short description

</td><td>

A brief description for the request.

</td></tr><tr><td>

Release notes

</td><td>

Text that appears on the ServiceNow Store for this application after it is published.

</td></tr><tr><td class="sub-head" colspan="2">

App Details

</td></tr><tr><td>

App name

</td><td>

Name of the submitted application.

</td></tr><tr><td>

App version

</td><td>

Version of the submitted application.

</td></tr><tr><td>

App Sys ID

</td><td>

System ID of the submitted application.

</td></tr><tr><td>

App Development URL

</td><td>

Link to app in App Engine Studio.

</td></tr><tr><td class="sub-head" colspan="2">

Requestor Details

</td></tr><tr><td>

Requestor First/Last Name

</td><td>

First and last name of the user who requested to the app deployment.

</td></tr><tr><td>

Requestor User ID

</td><td>

Identifier of the user who requested to the app deployment.

</td></tr><tr><td>

Requestor Email

</td><td>

Email address of the user who requested to the app deployment.

</td></tr><tr><td class="sub-head" colspan="2">

Deployment Details

</td></tr><tr><td>

Originating Environment

</td><td>

The instance of the originating environment.

</td></tr><tr><td>

Pipeline

</td><td>

Pipeline being used for deployment.

</td></tr><tr><td>

Current Environment

</td><td>

The target environment for the app.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td>

Any additional comments to be shared with the customer, including the app manifest, which lists the number of each type of file in the app, and any ATF or instance scan results are shown.

</td></tr><tr><td>

Work notes

</td><td>

Internal notes.

</td></tr></tbody>
</table>When you have saved the form, additional tabs for approval-related information display. The AES admin can use these tabs to approve the request.

**Parent Topic:**[App Engine Studio reference](aes-reference.md)

