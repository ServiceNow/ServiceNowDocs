---
title: Create an HR case
description: Create HR cases for employees or other individuals that require an HR service. Note that employees can also use the HR Service Portal to create HR cases for themselves.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Use HR Case Management, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Create an HR case

Create HR cases for employees or other individuals that require an HR service. Note that employees can also use the HR Service Portal to create HR cases for themselves.

## Before you begin

Role required: sn\_hr\_core.case\_writer

## About this task

-   For information about configuring case creation, see [Configure how HR cases are created](CreateModCaseCreationConfig.md).
-   Employees can also create HR cases for themselves using the record producers in Employee Center. The details entered by the employee get recorded in the description of the HR case.

    **Note:** If a value entered by the user does not match with the value in the HR profile of opened for, only then the value entered by the user gets recorded in the description of HR case. This behavior is not observed when the HR service of the case is either New Hire Onboarding or New Hire Journey.


## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **Create New Case**.

    Or, from any case list, click **New**.

2.  Determine the person for whom you are filing the case.

<table id="choicetable_iql_hwq_yqb"><thead><tr><th align="left" id="d442375e96">

Status of the person related to the case

</th><th align="left" id="d442375e99">

Action

</th></tr></thead><tbody><tr><td id="d442375e105">

**Anonymous employee or external individual**

</td><td>

Select **Skip verification** to create the case without having to enter an employee name or case number.

 Selecting this option takes you directly to the **Case Details** section and the **Employee information** section is not displayed.

 **Note:** The **Skip verification** option is displayed only if **Allow skipping verification** was selected during the configuration of HR case creation.

</td></tr><tr><td id="d442375e138">

**An employee**

</td><td>

Validate the employee by using the **Search Employee** field to search for the employee.You can search by employee name, case number, or any indexed field on the HR Profile of the sys\_user table.

 Additional information about the employee appears in the **Employee Information** section to help verify that you are creating an HR case for the correct person.

</td></tr></tbody>
</table>3.  Fill out the information in the **Case Details** section.

<table id="table_wm1_crx_qhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

COE

</td><td>

The **Center of Excellence** associated with the HR case you are creating. Selecting a COE filters the choices for HR service. See [HR Centers of Excellence data model](../concept/hr-centers-of-excellence-coes.md).**Note:** If an HR service is selected first, the associated COE automatically populates.

</td></tr><tr><td>

HR service

</td><td>

The HR service based on the COE selected or what you select based on communication with the employee request. The HR services that are available to an employee are filtered by:-   The COE selected
-   HR criteria for the **Subject person** based on the HR service configuration

The limit services filter on the **Case Creation Configuration** form. If the HR service field is empty, ensure that you did not remove the **Opened for** field.

</td></tr><tr><td>

Document Template Type

</td><td>

The category for the document template.**Note:** This option appears only when the Document Templates \[com.snc.document\_templates\] plugin is activated, and the **Document Template Type** field is selected while configuring the HR service.

</td></tr><tr><td>

Document Template

</td><td>

The document template associated to the case to generate document template tasks. **Note:** This option appears only when the Document Templates \[com.snc.document\_templates\] plugin is activated, and **Document Template** was selected when the HR service was configured.

</td></tr><tr><td>

Work notes

</td><td>

Information specific to the case that can help other HR agents. Text in the **Work Notes** field is not visible to the user named in the **Subject person** field.The sn\_hr\_core.restrict\_guest\_email system property allows a user to send an email from a personal email account referencing an HR case. If this property is set to false \(the default\), the text from the email appears in the Work notes field.

 **Note:** You can translate the text in your preferred language using the **Translate** option. For configuring the dynamic translation framework, see [Dynamic translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>4.  Select the person responsible for the service request in the **Opened for** field.

    -   If the case is being created by the person making the request, the values for **Subject person** and **Opened for** are the same.
    -   If the case is being created for a different user, for example, a manager filing a case for an employee, use the choice list to select a different user.
5.  Select the subject of the case in the **Subject person** field by selecting the Lookup using list icon \(![Lookup using list icon](../image/magnifying-glass.png)\) and searching for and selecting another employee.

    **Note:** Advanced reference qualifiers on a reference field is not supported in the case creation configuration page. When the limit user search filter is applied to the employee search, it will not be applied to **Opened for** and **Subject person**.

6.  Click **Create Case**.

7.  Continue working on the case.

    For more information, see [Work an HR case](t_CreateAnHRCase.md)


## Result

The **HR case** form appears with additional information about the case. The values selected for the **COE** and **HR service** fields determine the fields that appear.

-   **[Open an HR case to create a Journey Accelerator action plan](create-journey-accelerator-plan.md)**  
Journey Accelerator action plans can be created by opening an HR case with a related lifecycle event.
-   **[Request a background check through a third-party background check provider](request-background-check-by-background-check-system.md)**  
Request a background check for an employee through a third-party background check provider such as First Advantage, Accurate, or Sterling.
-   **[Request an electronic signature through the Docusign service](request-e-signature-through-docusign-service.md)**  
Request an electronic signature through the DocuSign service. When the case state changes to **Ready**, the flow triggers and creates DocuSign tasks for all of the signers. For parallel signing, the tasks are assigned all at once. For serial signing, the tasks are created in the order defined.
-   **[Request an electronic signature through the Adobe Acrobat Sign service](request-e-signature-through-adobe-sign-service.md)**  
Request an electronic signature through the Adobe Sign service. When the case state changes to **Ready**, the flow triggers and creates Adobe Sign tasks for all of the signers. For parallel signing, the tasks are assigned all at once. For serial signing, the tasks are created in the order defined.

**Parent Topic:**[Use HR Case Management](../concept/c_HRCaseManagement.md)

