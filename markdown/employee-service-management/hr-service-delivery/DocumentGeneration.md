---
title: HR document generation
description: There are multiple ways to generate documents in HR Service Delivery.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Work an HR case, Use HR Case Management, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR document generation

There are multiple ways to generate documents in HR Service Delivery.

-   Automatically
-   Multiple signatures are collected.
-   Preview, Sign, or Save

## Automatically

The document is made available for the subject person to sign. Only after the signature is added, the document will be generated automatically. Following are some examples:

-   A document such as Tuition Reimbursement Request must be sent to the employee for signature. The Request Tuition Reimbursement service has a work flow that triggers a task for the subject person \(employee\) of the case.

    An administrator enables the**Automatically Create Draft Document** case option on the HR service and sets up the HR service. When a case is created with that HR service and its state is changed to Work in Progress or Ready, a task gets automatically generated for the employee with the document available for signing.

-   A document such as Employee Verification Letter must be sent to the employee that does not require any signature.

    An administrator selects the template on the HR service. An HR case is created with that HR service. The HR agent previews the document using the **Preview Document** option, generates the document, and sends an email to the employee using the **Send email** option on the case.


![Case options for HR service form.](../image/HRService.png)

## Multiple signatures are collected

Documents like offer letters can require multiple signatures. When all signatures are collected, the document is automatically generated.

**Note:** For more information on setting this feature up, please see [Advanced form configuration](https://www.servicenow.com/docs/access?context=advanced-form-administration&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Advanced Forms Management in HR Service Delivery](https://community.servicenow.com/community?id=community_article&sys_id=a1676d67dba71410b1b102d5ca961941).

## Preview, Sign, or Save

Some documents require an HR agent to review, sign, or save it prior to sending it to a subject person for an HR case. An example is when a subject person requests an employment verification letter. This document requires an HR agent to review it for accuracy, sign it, and send it to the requested email address.

-   Open a case requiring a document to be sent to the subject person.
-   Ensure that the state is **Work in Progress**.
-   The Form Header shows:![Form header for HR workforce administration case form.](../image/HRCaseButtons.png)
-   Click **Preview Document** to view the document.
-   Click **Sign Document** for documents that require an HR signature.

    **Note:** By default, the document is available for the subject person to view once you preview it. Change this behavior by changing the **State** field on the HR task template. You can access the task template from the HR Case form by selecting the **HR service** &gt; **Service Activities** &gt; **Child task template**.


## Change values

When there are errors in the document:

-   Check the table the incorrect information is pulled from.
-   Check the HR case to ensure correct case information.
-   Check the document template for errors within the body of the document, incorrect field mapping, or variable information.

-   **[Edit a generated document](../task/agent-edit-document.md)**  
Support rendering values of variables, scripts, and blocks in edit mode in Preview Document. View the content of variables, scripts, or blocks rather than only viewing the variable or block names.

**Parent Topic:**[Work an HR case](../task/t_CreateAnHRCase.md)

