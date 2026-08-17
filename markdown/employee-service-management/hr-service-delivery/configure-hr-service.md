---
title: Configure an HR service
description: Create or modify an HR service to define the request to fulfillment process for that case type. Examples of HR services include benefits enrollment, direct deposit setup, and background check requests by third-party providers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/configure-hr-service.html
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [HR service configuration, HR services, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Configure an HR service

Create or modify an HR service to define the request to fulfillment process for that case type. Examples of HR services include benefits enrollment, direct deposit setup, and background check requests by third-party providers.

## About this task

\[Omitted video\]\[Omitted image ""\] Alt text: Configuring an HR service

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **HR Services** &gt; **HR Service Configuration**.

2.  Click **New** or open a record.

    **Note:**

3.  Fill in the fields on the form, as appropriate.

<table id="table_s3f_c43_lfb"><thead><tr><th>

Field

</th><th colspan="2">

Description

</th></tr></thead><tbody><tr><td>

HR service name

</td><td colspan="2">

Name of the HR service.

</td></tr><tr><td>

Value

</td><td colspan="2">

This field is automatically set to the name of the HR service.

</td></tr><tr><td>

Badge

</td><td colspan="2">

Badge to use with the HR service. Badges display on the portal to indicate to the employee which department is fulfilling that activity. See  for more information.

</td></tr><tr><td>

Fulfillment type

</td><td colspan="2">

Fulfillment type of the HR service. Select one of the following values:

</td></tr><tr><td>



</td><td>

Manual

</td><td>

A simple fulfillment type with no associated configurations. For example, for a medical benefits inquiry, the HR agent would fulfill the employee's request by answering the employee's question.

</td></tr><tr><td>



</td><td>

Service Activity

</td><td>

Service activities fulfill the HR service. In the **Service Activities** section at the bottom of the HR Service form, add one or more service activities to fulfill the HR service.**Note:** Service activities can be approvals, tasks, or child HR services. See  for more information.

</td></tr><tr><td>



</td><td>

Workflow

</td><td>

A workflow fulfills the HR service.

</td></tr><tr><td>



</td><td>

Lifecycle Event

</td><td>

\( only\) A lifecycle event fulfills the HR service. In the **Lifecycle Event Type** field, select a lifecycle event to fulfill the HR service.**Note:** A lifecycle event is a collection of activities that comprise an employee experience such as new hire onboarding. See  for more information.

</td></tr><tr><td>



</td><td>

Advanced

</td><td>

An advanced option to fulfill the HR service using a combination of workflows and service activities.

</td></tr><tr><td>



</td><td>

Flow

</td><td>

A flow fulfills the HR service. Select a flow in the **Flow** field to automate fulfillment of this HR service. **Note:** This assignment alone will not trigger the flow. The flow requires a trigger condition that references the HR service. For example, set the condition to `HR Service.flow = <current flow> AND State = Ready`.

A flow is an automated process that executes a sequence of reusable actions in order. For more information, see .

</td></tr><tr><td>

Topic detail

</td><td colspan="2">

HR topic detail that the HR service is categorized under.**Note:** The HR topic detail is the second-level of categorization for HR services. See  for more information.

</td></tr><tr><td>

Topic category

</td><td colspan="2">

HR topic category that the HR service is categorized under.**Note:** The HR topic category is the first-level of categorization for HR services. See  for more information.

</td></tr><tr><td>

COE

</td><td colspan="2">

HR Center of Excellence \(COE\) that the HR service is categorized under.**Note:**

-   The COEs are organized around functional disciplines and are extensions of the HR Case \[sn\_hr\_core\_case\] table. See  for more information.
-   \(  only\) An HR service for a lifecycle event can be associated with any COE.


</td></tr><tr><td rowspan="3">

Automatically close case

</td><td colspan="2">

Option to automatically close the HR case after all of the to-dos or all of the mandatory to-dos are complete. This field appears when **Service Activity** or **Lifecycle Event** is selected from **Fulfillment type**.

</td></tr><tr><td>

Close when

</td><td>

Select one of the following:-   All to-dos are complete
-   Mandatory to-dos are complete


</td></tr><tr><td>

Close offset

</td><td>

Number of days to offset the closure of the HR case. The maximum offset that you can apply is 90 days. For example, if the offset is set to three, then the HR case will close three days after the completion of all \(or all mandatory\) to-dos.**Note:** If a case has only optional tasks and its HR Service has auto\_close\_case set to true and close\_when set to mandatory \(close when mandatory to-dos are complete\), the case will automatically close when the scheduled job runs, ignoring the auto\_close\_offset field.

</td></tr><tr><td>

Opened for / Approver view

</td><td colspan="2">

Different view of the HR case \(with different fields\) based on role.

</td></tr><tr><td>

Subject person / Task assignee view

</td><td colspan="2">

Different view of the HR case \(with different fields\) based on role.

</td></tr><tr><td>

Active

</td><td colspan="2">

Option to activate the HR service for use.

</td></tr><tr><td>

Show case to subject person

</td><td colspan="2">

\(  only\) Option to show the HR case to the subject person when it is created, including:-   HR tasks assigned to the subject person
-   Child HR cases where the subject person is also the opened for
-   Child HR cases when the subject person has a task assigned
-   Requests where the subject person is the requested for
 If the HR case has one or more child cases, the child cases are automatically rolled up with the parent case up to three generations. HR child cases that are rolled up with the parent do not appear as separate requests on the requests page. Non-HR child cases appear both as a separate request and as part of the roll-up on the parent case.

</td></tr><tr><td>

Template

</td><td colspan="2">

HR case template to use with the HR service.**Note:** The HR case template automatically populates fields on the HR case form when a request for that service is made. See  for more information.

</td></tr><tr><td>

Automatically move attachments

</td><td colspan="2">

Option to enable the movement of attachments to a document repository.**Note:** This option appears if the Employee Document Management \[com.sn\_employee\_document\_management\] plugin is activated.

</td></tr><tr><td>

Employee Document Type

</td><td colspan="2">

Option to specify a document type into which you want to move attachments.**Note:** This option appears if the **Automatically move attachments** check box is enabled.

</td></tr><tr><td>

Record producer

</td><td colspan="2">

\(Employee self-service only\) Record producer to use with the HR service if you want to make the service available as an HR catalog item in the HR service catalog. The record producer defines the required fields and how the HR catalog item appears in the HR service catalog to employees. For more information, see .**Tip:** For best results, do not configure multiple record producers to invoke a single HR service.

</td></tr><tr><td>

Case options

</td><td colspan="2">

Additional case options for the HR service. For example, you can:-   Add Manager to Watchlist: The manager of the opened for person is added to the watchlist and receives notifications about the case.
-   Agent Can Add An Approval: Allow agents the flexibility to add adhoc approvers to a case. For more information, see .
-   Automatically Create Draft Document: Automatically place a document for HR services to the subject person on the HR Service Portal. An example is when an employee requests tuition reimbursement. An education expense agreement document is automatically sent to the employee to sign.
-   Automatically Initiates Document tasks: Tasks are created for participants who are mapped to a document template. This option appears only when the Document Templates \[com.snc.document\_templates\] plugin is installed and a document template is selected on a HR service.
-   Do Not Default Subject Person: Subject Person is not defaulted from the Opened for person when a case is created.
-   Skip Auto Assign: HR case is not automatically assigned to an HR group or agent using the HR template or matching rules.

**Note:** Skipping auto assignment does not affect the HR templates, assignment rules, or the workflows.

-   Skip Automatic User Acceptance State: Select to bypass the user acceptance state.
-   User Cannot Cancel: Opened for person on HR case cannot cancel it via the  \(\) or service portal.


</td></tr><tr><td>

HR criteria

</td><td colspan="2">

HR criteria to apply to the HR service.**Note:**

-   HR criteria defines the conditions that an employee must meet for an HR agent to be able to access that HR service on their behalf. For example, you can configure the HR criteria for a 401\(k\) request so that the HR service is only available to U.S. employees from the **Create New Case** module. See  for more information.
-   \(Employee self-service only\) HR criteria applied to the HR service is internal-facing only, and has no relation to the user criteria that is used to control what HR catalog items an employee can access from the HR service catalog. See  for more information.
-   When defining conditions like case sensitivity or null values, see API GlideFilter - Scoped, Global.


</td></tr><tr><td>

Case creation service config

</td><td colspan="2">

Configuration of the HR case creation form for the HR service.**Note:** The HR case creation form is what displays when an HR agent selects an HR service from the **Create New Case** module. You can configure the form to include additional fields to collect relevant information. See  for more information.

</td></tr><tr><td>

Description

</td><td colspan="2">

Description of the HR service.

</td></tr></tbody>
</table>4.  In the **Checklist** related list, you can provide steps to help HR agents fulfill HR cases for the associated HR service.

    |Field|Description|
    |-----|-----------|
    |Checklist|Provide a checklist of items for HR agents to check off when fulfilling the HR case.|

5.  In the **HR Service Additional Information** related list, you can configure the fields that appear on the HR case form after a request for that service is made.

    This is a two-part process. In addition to the configuration here, you must also configure the HR case form for the HR Center of Excellence \(COE\) that the HR service is categorized under.

    **Note:** The HR case form is what displays after an HR case is created. Configuration of the HR case form is a two-part process. See  for more information.

6.  Click **Submit** or **Update**.

    **Note:** If you added a custom column to an HR COE table, you must create a UI policy action \(**Visible** field is set to **False**\) to hide it from other HR services that use that HR COE table. For example, if you add a custom column to the HR Payroll Case \[sn\_hr\_core\_case\_payroll\] table, it appears in all HR services related to this table. The custom column appears even after you add it for a specific HR service. For more information, see UI policies.


-   **[Configure a service activity for an HR service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/configure-service-activity-for-hr-service.md)**  
If the fulfillment type of an HR service is set to **Service Activity**, configure one or more service activities. Service activities can be approvals, tasks, or child HR services.
-   **[Configure the HR case creation form for an HR service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/configure-case-creation-form-for-hr-service.md)**  
Configure the fields that appear on the HR case creation form for an HR service.
-   **[Configure the HR case form for an HR service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/configure-case-form-for-hr-service.md)**  
Configure the fields that appear on the HR case form for an HR service.
-   **[Add a custom column \(field\) to an HR table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/configure-custom-column-hr-table.md)**  
You can add custom columns \(fields\) to an HR table.

**Parent Topic:**[HR service configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/hr-service-configuration.md)

**Previous topic:**[HR service configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/hr-service-configuration.md)

**Next topic:**[Configure a service activity for an HR service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/configure-service-activity-for-hr-service.md)

