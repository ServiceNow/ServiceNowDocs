---
title: Request an electronic signature through the Adobe Acrobat Sign service
description: Request an electronic signature through the Adobe Sign service. When the case state changes to Ready, the flow triggers and creates Adobe Sign tasks for all of the signers. For parallel signing, the tasks are assigned all at once. For serial signing, the tasks are created in the order defined.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create an HR case, HR Case Management, Explore and use HR Case and Knowledge Management, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Request an electronic signature through the Adobe Acrobat Sign service

Request an electronic signature through the Adobe Sign service. When the case state changes to **Ready**, the flow triggers and creates Adobe Sign tasks for all of the signers. For parallel signing, the tasks are assigned all at once. For serial signing, the tasks are created in the order defined.

## Before you begin

An HR integrations administrator must have set up the integration between HR Service Delivery and the Adobe Sign system before requests can be made.

Role required: sn\_hr\_core.case\_writer

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **Create New Case**.

2.  In the **Search for Employee** field, select the employee for whom you are creating the case.

3.  In the **Case Details** section, in the **HR service** field, select an HR service.

    -   &lt;Name of custom HR service&gt;
    -   Signature using Adobe Sign
    ![Selecting the HR service](../image/signature-adobe.png)

4.  Fill in the other fields on the form, as appropriate.

    For further details on the form fields, see [Create an HR case](search-hr-case.md).

5.  Click **Create Case**.


## What to do next

When the case state changes to **Ready**, the flow triggers and creates Adobe Sign tasks for all of the signers. For parallel signing, the tasks are assigned all at once. For serial signing, the tasks are created in the order defined.

Signers must complete their Adobe Sign tasks through a self-service portal such as the Employee Center. The Adobe Sign task is displayed as a URL in the to-dos page in the Employee Center.

On clicking the URL, the signer is directed to the Adobe Sign system to sign the document. After completing the task, the signer is redirected to the to-dos page in the Employee Center. The status of the Adobe Sign task is not updated immediately because the callback is asynchronous.

**Note:**

-   The Adobe Sign tasks are created using the HR task template named the Adobe Sign task template.
-   Auto-close integration type tasks are created using the HR task template.
-   Users with the sn\_hr\_core.admin role can track the flow execution with the **Show Flow** related link. If a case is canceled from platform, you must manually cancel the associated flow. Otherwise, the flow remains in waiting. To cancel the flow, click the **Show Flow** related link to open the flow designer in a new window, and then click **Cancel Flow**.

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

