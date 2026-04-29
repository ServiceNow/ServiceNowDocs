---
title: Modify a request type for the Platform UI
description: Review and modify the case interceptors that are available with Financial Services Operations applications as needed. These interceptors enable your agents to create cases for various request types from the Platform UI.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Request types, Configure, Financial Services Operations \(FSO\)]
---

# Modify a request type for the Platform UI

Review and modify the case interceptors that are available with Financial Services Operations applications as needed. These interceptors enable your agents to create cases for various request types from the Platform UI.

## Before you begin

Ensure that the scope is selected for the application for which you are configuring an interceptor.

Role required: Based on the application that you are configuring, you need the following roles:

-   For Financial Services Payment Operations: sn\_bom\_payment.admin and admin
-   For Financial Services Card Operations: sn\_bom\_card.admin and admin

## About this task

**Note:** If you create additional request types for an application, make sure that you add them to both the case interceptor and Workspace record type selector so that the request type selections are available in both the Platform and Workspace UIs.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Interceptors**.

2.  Filter the list to show the interceptors for the application and then select an interceptor.

    The following interceptors are installed with Financial Services Operations applications:

<table id="table_dvk_z2m_3mb"><thead><tr><th>

Application

</th><th>

Interceptor

</th></tr></thead><tbody><tr><td>

Financial Services Payment Operations

</td><td>

-   Payment Inquiry Case
-   Claim


</td></tr><tr><td>

Financial Services Card Operations

</td><td>

Credit Card Service

</td></tr></tbody>
</table>    The Answers related list specifies what choices are presented and where the agent is redirected after a choice is selected.

3.  Modify the Answers related list.

    For example, to add a new request type to an interceptor, follow these steps:

    1.  Click **New** in the Answers related list.

    2.  On the form, fill in the required fields.

    3.  Click **Submit**.

4.  Test the interceptor by clicking **Try It**.


## Result

The interceptor is updated with the configured request types. When an agent clicks the **New** button on a case list in Platform UI, it launches the interceptor with these request types. The agent can select one of the request types to create the case.

