---
title: Create a work order
description: When off-site work is requested, create a work order to provide information for the agents who fulfill the request. You can create an entirely new work order, or you can create a work order from these other record types: problem, incident, change, or project task. You can also create a work order from another existing work order.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Manage work orders, Prepare work orders, Use, Field Service Management]
---

# Create a work order

When off-site work is requested, create a work order to provide information for the agents who fulfill the request. You can create an entirely new work order, or you can create a work order from these other record types: problem, incident, change, or project task. You can also create a work order from another existing work order.

## Before you begin

Role required: wm\_initiator, wm\_initiator\_qualifier, or admin

Ensure to install the following plugins

-   Customer Service with Field Service Management \(com.snc.csm\_fsm\_integration\) to create case-related work orders from the Customer Service and Consumer Service Portals.
-   Customer Service Install Base Management \(com.snc.install\_base\) to create work orders against install base items, identify assets, configuration items \(CI\), or affected install base items.
-   Use roles such as wm\_location\_agent, wm\_location\_assignment.manager to restrict work order and task access based on the provider's service organization when the Work Management and Service Organization plugins are installed.

## About this task

-   In the work order, specify the nature of the work required and identify the configuration items \(CI\) affected.
-   To create work orders for common tasks such as the onboarding of new employees, you can use work order model templates to create all the necessary records automatically.
-   Restrict access to work orders and tasks so that users can only view and manage those assigned to their own service organization, ensuring sensitive information is securely managed within the appropriate organization.

## Procedure

1.  Create the work order.

<table id="choicetable_psz_bkq_v1b"><thead><tr><th align="left" id="d45051e103">

Option

</th><th align="left" id="d45051e106">

Steps

</th></tr></thead><tbody><tr><td id="d45051e112">

**Create a new work order**

</td><td>

1.  Navigate to **Field Service** &gt; **Work Order** &gt; **Create New**.
2.  Enter a **Short description**.

Optionally, you can click the search knowledge icon \(![Search knowledge icon.](../image/SearchKnowledgeIcon.png)\) to view articles in the knowledge base relating to this product model, plan, or CI. Doing so could provide a solution related to the reason you are submitting a work order.

3.  Click **Submit**.


</td></tr><tr><td id="d45051e159">

**Create a work order from an incident, problem, change, project task, or another work order.**

</td><td>

1.  Open the record that you want to create the work order from.

**Note:** Before work orders can be created from project tasks, Field Service Management must be integrated with Project Portfolio Management.

2.  Right-click the form title bar and select **Create Work Order**.


</td></tr></tbody>
</table>    The work order is created in the **Draft** stage.

    If you created the work order from another record, the short description of the original record is copied as the short description of the work order. Some of the work order fields are auto-filled with information from the original record. For details, see [Prepare work orders](../../field-service-management/concept/preparing-work-orders.md).

2.  Fill in the fields on the Work Order form, as appropriate.

<table id="table_vst_5nf_2r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated identification number for the work order.

</td></tr><tr><td>

Company

</td><td>

Company for which the work order was opened. The lookup list shows only those companies designated as **Customers** in their company record.

</td></tr><tr><td>

Contact

</td><td>

Person that requires the work. The lookup list shows only users associated with the selected **Company**.

</td></tr><tr><td>

Asset

</td><td>

The asset tag number or the serial number of the asset involved in this case. If there are multiple assets, provide the details of the primary asset and add the rest under **Affected Products** in the **Related Links** panel. You can select linear asset only if Enterprise Asset Management is installed.

</td></tr><tr><td>

Affected CI

</td><td>

Primary item that requires work, such as a broken laptop or a printer that needs ink. Configuration Item lookup lists are based on the selected **Company**. If more than one item requires work, add them to the Affected CIs related list.

 When assigning CIs to individual tasks, the qualifier and dispatcher can choose only from the CIs in the **Work Order Affected CIs** related list. The same CI in a work order can be applied to multiple work order tasks.

</td></tr><tr><td>

Part Requirement

</td><td>

Additional parts or assets required to complete the work order.This option is displayed in the **Related Links** panel and can be applied to the related work order tasks.

</td></tr><tr><td>

Linear Work

</td><td>

Option to indicate that the work order is for a linear asset, and ensure that the tasks are arranged in a single progressive line. **Linear Work** option is selected by default.This option appears only when a linear asset is selected in the **Asset** field.

</td></tr><tr><td>

Start location

</td><td>

Geographical area that marks the starting of physical location for a linear asset. **Start location** field is automatically populated with the location that is mapped with the selected linear asset.This option appears only when a linear asset is selected in the **Asset** field.

</td></tr><tr><td>

End location

</td><td>

Geographical area that marks the ending of physical location for a linear asset. **End location** field is automatically populated with the location that is mapped with the selected linear asset.This option appears only when a linear asset is selected in the **Asset** field.

</td></tr><tr><td>

Requestor Service Organization

</td><td>

Represents the requestor service organization that has initiated creation of the work order. &lt;re word&gt;**Note:** The Requestor Service Organization field appears only when the Service Organization \(com.snc.service\_organization\) plugin is installed.

</td></tr><tr><td>

Provider Service Organization

</td><td>

Represents the fulfiller service organization. &lt;used for task fulfillment re word&gt;**Note:** The Provider Service Organization field appears only when the Service Organization \(com.snc.service\_organization\) plugin is installed.

</td></tr><tr><td>

Install base item

</td><td>

The install base item you have a question on or issue with.

</td></tr><tr><td>

Location

</td><td>

Geographical area \(physical location\) where the work must be done. Location field is automatically populated with the location that is mapped with the selected **Provider Service Organization**. **Note:** For the work orders that are initiated from case, the **Location** field is filled automatically based first on the **Affected CI** field and then, if no affected CI or location is provided, on the **Caller**.

 If you do not want to use the auto-populated location, you can add an ad hoc location. For more information, see [Setting ad-hoc locations in work orders and work order tasks](../../field-service-management/concept/service-locations-work-orders.md).

</td></tr><tr><td>

Template

</td><td>

Template for creating this work order \(optional\). Click the lookup icon and select a template. The description of the selected template will populate the **Description** field. If you selected **Tasks will be dispatched manually** in the Field Service Configuration screen, work order tasks that were created for orders that use templates are automatically transitioned to **Pending dispatch**. For more information on templates, see Creating Service Order Templates.

 **Note:** If defined in advance, the template may contain task dependencies, which the tasks in your work order will inherit.

</td></tr><tr><td>

Opened

</td><td>

Date and time the work order was opened.

</td></tr><tr><td>

Priority

</td><td>

Precedence of the work order, based on severity of the impact, number of users affected, or other factors. The SLA applied to this work order is determined by the priority selected in this field.

</td></tr><tr><td>

State

</td><td>

Current stage of the work order in the work order life cycle.**Note:** The **Scheduled** state appears in between **Pending Dispatch** and **Assigned** states only if your administrator enables **Use Scheduled state** option in [Global domain configurations](t_ConfigureFieldService.md).

</td></tr><tr><td>

Qualification group

</td><td>

Group that can specify the technical details of the work order. The lookup list shows only the qualification groups associated with the selected **Location**. If no qualification groups exist for the location, all qualifications groups are listed and any can be selected. This field is hidden when Field Service Management is configured for [automatic qualification](../concept/c_QualifyWorkOrders.md#AutomaticConfiguration).

</td></tr><tr><td>

Initiated from

</td><td>

Record number of the original problem, incident, change request, or other work order from which the work order was created.

</td></tr><tr><td>

Billable

</td><td>

Option for issuing a statement of fees or charges for the work order. This is useful for running reports on billable work orders.

</td></tr><tr><td>

Short description

</td><td>

Brief explanation of the work order.

</td></tr><tr><td>

Description

</td><td>

Detailed information describing the work to be performed. Initiators create work orders, but qualifiers should add as much detail about the work to be performed as possible to avoid extra communication with the caller .

</td></tr><tr><td>

Work Notes

</td><td>

Information about the work order and how it was completed. This field is not visible to customers. Work notes are added throughout the work order life cycle to help users who work on it to communicate useful information.

</td></tr><tr><td class="sub-head" colspan="2">

Scheduling

</td></tr><tr><td>

Scheduled start

</td><td>

Date and time when the earliest task is scheduled to start.

</td></tr><tr><td>

Estimated end

</td><td>

Estimated date when all tasks will be completed.

</td></tr><tr><td>

Actual work start

</td><td>

Date and time when the earliest task actually started.

</td></tr><tr><td>

Actual work end

</td><td>

Date and time when the last task actually ended.

</td></tr><tr><td>

Requested due by

</td><td>

Estimated date when the latest task will be completed. The **Lead Time** for the maintenance schedule is subtracted from the **Requested due by** date for the work order to determine this date.

</td></tr></tbody>
</table>3.  Click **Submit** or **Update** to save your changes.


## Result

The work order is created and awaits for qualification to create a work order task.

**Note:** You must enable the **Apply Work Order template in draft status** option and **wm\_task\_initiator** role to create tasks for the work order based on the applied template, without qualifying the work order when it is in the draft state. For more information about these configurations, see [Global domain configurations](t_ConfigureFieldService.md) and [Roles installed with Field Service Management](../reference/r_UserRoleInstallWFieldSrvMgmnt.md).

## What to do next

After you complete the Work Order form, move it to the next state that is [configured for Field Service Management](t_ConfigureFieldService.md#BusinessProcess). In the next state, other users with appropriate roles for the state will process the work order.

On the Work Order form, click whichever of the following options is available:

<table id="table_dtm_n4h_w1b"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ready for Approval

</td><td>

Click **Ready for Approval** to move the work order to the Waiting for Approval state.

</td></tr><tr><td>

Ready for Qualification

</td><td>

Click **Ready for Qualification** to move the work order to the Awaiting Qualification state.

 A work order task is automatically created if one does not exist. The short description, description, and location of the work order are copied into the task.

 The **Ready for Qualification** option is available only when **Qualification is required for new requests** is enabled in the configuration for Field Service Management.

</td></tr><tr><td>

Ready for Dispatch

</td><td>

Click **Ready for Dispatch** to move the work order to the Ready for Dispatch state.The **Ready for Dispatch** option is available only when **Approval for new request required** and **Qualification is required for new requests** are disabled in the configuration for Field Service Management.

</td></tr></tbody>
</table>