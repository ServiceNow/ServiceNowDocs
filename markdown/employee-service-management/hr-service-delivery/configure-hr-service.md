---
title: Configure an HR service
description: Create or modify an HR service to define the request to fulfillment process for that case type. Examples of HR services include benefits enrollment, direct deposit setup, and background check requests by third-party providers.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [HR service configuration, HR services, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Configure an HR service

Create or modify an HR service to define the request to fulfillment process for that case type. Examples of HR services include benefits enrollment, direct deposit setup, and background check requests by third-party providers.

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **HR Services** &gt; **HR Service Configuration**.

2.  Click **New** or open a record.

    **Note:** The COEs available to you may differ depending on the HR package you have.

    -   The categorization of HR catalog items are employee-facing only, and have no relation to the categorization of HR services under the HR Centers of Excellence \(COEs\) data model.
    -   If you are creating a new HR service and plan to make it available for employee self-service, see [HR catalog item configuration](../concept/hr-catalog-item-configuration.md). Creating a new HR catalog item automatically creates a corresponding HR service, and you can avoid creating duplicate services.
    -   If you have an existing HR service that you want to make available for employee self-service, do not create an HR catalog item. \(Creating a HR catalog item automatically creates a corresponding HR service.\) Instead, see [Configure a record producer for an HR service](configure-hr-record-producer.md) to add the existing service as an HR catalog item in the HR service catalog.
    -   The Agent Workspace for HR Case Management is highly configurable for HR agents. It supports the same functionality in the Classic HR Service Delivery Agent Workspace.
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

Badge to use with the HR service. Badges display on the portal to indicate to the employee which department is fulfilling that activity. See [Configure an HR badge](CreateModHRBadges.md) for more information.

</td></tr><tr><td rowspan="7">

Fulfillment type

</td><td colspan="2">

Fulfillment type of the HR service. Select one of the following values:

</td></tr><tr><td>

Manual

</td><td>

A simple fulfillment type with no associated configurations. For example, for a medical benefits inquiry, the HR agent would fulfill the employee's request by answering the employee's question.

</td></tr><tr><td>

Service Activity

</td><td>

Service activities fulfill the HR service. In the **Service Activities** section at the bottom of the HR Service form, add one or more service activities to fulfill the HR service.**Note:** Service activities can be approvals, tasks, or child HR services. See [Configure a service activity for an HR service](configure-service-activity-for-hr-service.md) for more information.

</td></tr><tr><td>

Workflow

</td><td>

A workflow fulfills the HR service.

</td></tr><tr><td>

Lifecycle Event

</td><td>

\(Enterprise Onboarding and Transitions only\) A lifecycle event fulfills the HR service. In the **Lifecycle Event Type** field, select a lifecycle event to fulfill the HR service.**Note:** A lifecycle event is a collection of activities that comprise an employee experience such as new hire onboarding. See [Building a lifecycle event](../concept/hr-lifecycle-event-configuration.md) for more information.

</td></tr><tr><td>

Advanced

</td><td>

An advanced option to fulfill the HR service using a combination of workflows and service activities.

</td></tr><tr><td>

Flow

</td><td>

A flow fulfills the HR service. In the **Flow** field, select a flow that will be invoked to fulfill the HR service. To link flow to the HR service, a flow condition needs to be created for the HR service. A flow is an automated process of sequential and reusable actions. For more information, see [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=australia&pubname=australia-application-development&ft:locale=en-US).

</td></tr><tr><td>

Topic detail

</td><td colspan="2">

HR topic detail that the HR service is categorized under.**Note:** The HR topic detail is the second-level of categorization for HR services. See [HR service categorization](../concept/hr-service-categorization.md) for more information.

</td></tr><tr><td>

Topic category

</td><td colspan="2">

HR topic category that the HR service is categorized under.**Note:** The HR topic category is the first-level of categorization for HR services. See [HR service categorization](../concept/hr-service-categorization.md) for more information.

</td></tr><tr><td>

COE

</td><td colspan="2">

HR Center of Excellence \(COE\) that the HR service is categorized under.**Note:**

-   The COEs are organized around functional disciplines and are extensions of the HR Case \[sn\_hr\_core\_case\] table. See [HR service categorization](../concept/hr-service-categorization.md) for more information.
-   \( Enterprise Onboarding and Transitions only\) An HR service for a lifecycle event can be associated with any COE.


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

\(Employee Service Center only\) Configuration of the HR ticket page header for the person that the HR case was opened for and any approvers. **Note:** The HR ticket page is where users can view the details of an HR case in the Employee Center. See  for more information.

</td></tr><tr><td>

Subject person / Task assignee view

</td><td colspan="2">

\(Employee Center only\) Configuration of the HR ticket page header for the subject person of the HR case and any task assignees. **Note:** The HR ticket page is where users can view the details of an HR case in the Employee Center. See  for more information.

</td></tr><tr><td>

Active

</td><td colspan="2">

Option to activate the HR service for use.

</td></tr><tr><td>

Show case to subject person

</td><td colspan="2">

\(Employee Service Center Employee Center only\) Option to show the HR case to the subject person when it is created, including:-   HR tasks assigned to the subject person

**Note:** The ticket page of the Employee Center shows all to-dos and requests for an HR case when the Opened for and Subject person are identical. If you want the Subject person to only see tasks assigned to them, change the Opened for person to someone different \(possibly the Subject person's manager\).

-   Child HR cases where the subject person is also the opened for
-   Child HR cases when the subject person has a task assigned
-   Requests where the subject person is the requested for
 If the HR case has one or more child cases, the child cases are automatically rolled up with the parent case up to three generations. HR child cases that are rolled up with the parent do not appear as separate requests on the requests page. Non-HR child cases appear both as a separate request and as part of the roll-up on the parent case.

 **Note:** The HR ticket page is where users can view the details of an HR case in the Employee Center. See  for more information.

</td></tr><tr><td>

Template

</td><td colspan="2">

HR case template to use with the HR service.**Note:** The HR case template automatically populates fields on the HR case form when a request for that service is made. See [Configure an HR case template](configure-hr-case-template.md) for more information.

</td></tr><tr><td>

Record producer

</td><td colspan="2">

\(Employee self-service only\) Record producer to use with the HR service if you want to make the service available as an HR catalog item in the HR service catalog. The record producer defines the required fields and how the HR catalog item appears in the HR service catalog to employees. For more information, see [Configure a record producer for an HR service](configure-hr-record-producer.md).**Tip:** For best results, do not configure multiple record producers to invoke a single HR service.

</td></tr><tr><td>

Case options

</td><td colspan="2">

Additional case options for the HR service. For example, you can:-   Add Manager to Watchlist: The manager of the opened for person is added to the watchlist and receives notifications about the case.
-   Agent Can Add An Approval: Allow agents the flexibility to add adhoc approvers to a case. For more information, see [Add adhoc approvers to a case](add-approvers-cm.md).
-   Automatically Create Draft Document: Automatically place a document for HR services to the subject person on the HR Service Portal. An example is when an employee requests tuition reimbursement. An education expense agreement document is automatically sent to the employee to sign.
-   Automatically Initiates Document tasks: Tasks are created for participants who are mapped to a document template. This option appears only when the Document Templates \[com.snc.document\_templates\] plugin is installed and a document template is selected on a HR service.
-   Do Not Default Subject Person: Subject Person is not defaulted from the Opened for person when a case is created.
-   Skip Auto Assign: HR case is not automatically assigned to an HR group or agent using the HR template or matching rules.

**Note:** Skipping auto assignment does not affect the HR templates, assignment rules, or the workflows.

-   Skip Automatic User Acceptance State: Select to bypass the user acceptance state.
-   User Cannot Cancel: Opened for person on HR case cannot cancel it via the Employee Center \(EC\) or service portal.


</td></tr><tr><td>

HR criteria

</td><td colspan="2">

HR criteria to apply to the HR service.**Note:**

-   HR criteria defines the conditions that an employee must meet for an HR agent to be able to access that HR service on their behalf. For example, you can configure the HR criteria for a 401\(k\) request so that the HR service is only available to U.S. employees from the **Create New Case** module. See [HR criteria](../concept/hr-criteria.md#) for more information.
-   \(Employee self-service only\) HR criteria applied to the HR service is internal-facing only, and has no relation to the user criteria that is used to control what HR catalog items an employee can access from the HR service catalog. See [Edit the record producer for an HR catalog item](edit-hr-record-producer-for-hr-catalog-item.md) for more information.
-   When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](../concept/hr-service-configuration.md).


</td></tr><tr><td>

Case creation service config

</td><td colspan="2">

Configuration of the HR case creation form for the HR service.**Note:** The HR case creation form is what displays when an HR agent selects an HR service from the **Create New Case** module. You can configure the form to include additional fields to collect relevant information. See [Configure the HR case creation form for an HR service](configure-case-creation-form-for-hr-service.md) for more information.

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

    **Note:** The HR case form is what displays after an HR case is created. Configuration of the HR case form is a two-part process. See [Configure the HR case form for an HR service](configure-case-form-for-hr-service.md#) for more information.

6.  Click **Submit** or **Update**.

    **Note:** If you added a custom column to an HR COE table, you must create a UI policy action \(**Visible** field is set to **False**\) to hide it from other HR services that use that HR COE table. For example, if you add a custom column to the HR Payroll Case \[sn\_hr\_core\_case\_payroll\] table, it appears in all HR services related to this table. The custom column appears even after you add it for a specific HR service. For more information, see [UI policies](../concept/hr-service-configuration.md).


-   **[Configure a service activity for an HR service](configure-service-activity-for-hr-service.md)**  
If the fulfillment type of an HR service is set to **Service Activity**, configure one or more service activities. Service activities can be approvals, tasks, or child HR services.
-   **[Configure the HR case creation form for an HR service](configure-case-creation-form-for-hr-service.md)**  
Configure the fields that appear on the HR case creation form for an HR service.
-   **[Configure the HR case form for an HR service](configure-case-form-for-hr-service.md#)**  
Configure the fields that appear on the HR case form for an HR service.
-   **[Add a custom column \(field\) to an HR table](configure-custom-column-hr-table.md)**  
You can add custom columns \(fields\) to an HR table.

**Parent Topic:**[HR service configuration](../concept/hr-service-configuration.md)

**Previous topic:**[HR service configuration](../concept/hr-service-configuration.md)

**Next topic:**[Configure a service activity for an HR service](configure-service-activity-for-hr-service.md)

