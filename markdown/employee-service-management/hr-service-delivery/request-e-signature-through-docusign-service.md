---
title: Request an electronic signature through the Docusign service
description: Request an electronic signature through the DocuSign service. When the case state changes to Ready, the flow triggers and creates DocuSign tasks for all of the signers. For parallel signing, the tasks are assigned all at once. For serial signing, the tasks are created in the order defined.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create an HR case, Use HR Case Management, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Request an electronic signature through the Docusign service

Request an electronic signature through the DocuSign service. When the case state changes to **Ready**, the flow triggers and creates DocuSign tasks for all of the signers. For parallel signing, the tasks are assigned all at once. For serial signing, the tasks are created in the order defined.

## Before you begin

An HR integrations administrator must have set up the integration between HR Service Delivery and the DocuSign system before requests can be made. See [Integrating with the DocuSign service](../concept/docusign-integration-for-hr.md) for more information.

Role required: sn\_hr\_core.case\_writer

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **Create New Case**.

2.  In the **Search for Employee** field, select the employee you are creating the case for.

3.  In the **Case Details** section, in the **HR service** field, select an HR service.

    -   Request Signature using DocuSign on Adhoc Document
    -   Request Signature using DocuSign Template
    -   &lt;Name of custom HR service&gt;
    ![Select the employee you are creating the background check request case for.](../image/request-background-check-1.png)

4.  Fill in the other fields on the form, as appropriate.

    For further details on the form fields, see [Create an HR case](search-hr-case.md).

5.  Click **Create Case**.


## What to do next

When the case state changes to **Ready**, the flow triggers and creates DocuSign tasks for all of the signers. For parallel signing, the tasks are assigned all at once. For serial signing, the tasks are assigned in the order defined.

**Note:**

-   The tasks are created using the HR task template named DocuSign Task Template.
-   Users with the sn\_hr\_core.admin role can track the flow execution with the **Show Flow** related link. If a case is cancelled from platform, you must manually cancel the associated flow. Otherwise, the flow will remain in waiting. To cancel the flow, click the **Show Flow** related link to open the flow designer in a new window, and then click **Cancel Flow**.
-   Signers must complete their DocuSign tasks through a self-service portal such as the Employee Center. Signing in platform is not supported.

<table id="table_gkn_cs4_f3b"><thead><tr><th>

Action

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Document signed by all

</td><td>

-   Case and tasks closed completed
-   Signed document\(s\) attached to case and tasks

</td></tr><tr><td>

Document declined

</td><td>

-   Case and declined task closed incomplete
-   Pending tasks canceled
-   No attachments to case

</td></tr><tr><td>

Document voided or flow errored

</td><td>

-   Case closed incomplete and tasks canceled
-   No attachments to case

</td></tr></tbody>
</table>**Parent Topic:**[Create an HR case](search-hr-case.md)

