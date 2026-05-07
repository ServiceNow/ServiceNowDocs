---
title: Work order form
description: Create and track field service work orders for on-site correction, containment, or repair activities linked to a QIM record.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-16"
reading_time_minutes: 3
breadcrumb: [Quality issue management form, Reference, Manufacturing Commercial Operations]
---

# Work order form

Create and track field service work orders for on-site correction, containment, or repair activities linked to a QIM record.

<table id="table_ajg_3n3_y3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Work order number that is automatically generated. The number starts with WO and incremented for every new report.

</td></tr><tr><td>

Company

</td><td>

Company for which the work order was opened. The lookup list shows only those companies designated as Customers in their company record.

</td></tr><tr><td>

Contact

</td><td>

Person that requires the work. The lookup list shows only users associated with the selected Company.

</td></tr><tr><td>

Requestor service organization

</td><td>

Represents the requestor service organization that has initiated creation of the work order. **Note:** The Requestor Service Organization field appears only when the Service Organization \(com.snc.service\_organization\) plugin is installed.

</td></tr><tr><td>

Asset

</td><td>

The asset tag number or the serial number of the asset involved in this case. If there are multiple assets, provide the details of the primary asset and add the rest under **Affected Products** in the Related Links panel.

</td></tr><tr><td>

Affected CI

</td><td>

Primary item that requires work, such as a broken laptop or a printer that needs ink. Configuration Item lookup lists are based on the selected Company. If more than one item requires work, add them to the Affected CIs related list.

</td></tr><tr><td>

Location

</td><td>

Geographical area \(physical location\) where the work must be done. Location field is automatically populated with the location that is mapped with the selected **Provider Service Organization**.

</td></tr><tr><td>

Template

</td><td>

Template for creating this work order \(optional\).

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

Current stage of the work order in the work order life cycle.

</td></tr><tr><td>

Provider Service Organization

</td><td>

Represents the fulfiller service organization. **Note:** The Provider Service Organization field appears only when the Service Organization \(com.snc.service\_organization\) plugin is installed.

</td></tr><tr><td>

Qualification group

</td><td>

Group that can specify the technical details of the work order. The lookup list shows only the qualification groups associated with the selected Location. If no qualification groups exist for the location, all qualifications groups are listed and any can be selected.

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

Short description is auto fetched from the correction action.

</td></tr><tr><td>

Description

</td><td>

Detailed information describing the work to be performed.Initiators create work orders, but qualifiers should add as much detail about the work to be performed as possible to avoid extra communication with the caller.

</td></tr><tr><td>

Work notes

</td><td>

Information about the work order and how it was completed. This field is not visible to customers. Work notes are added throughout the work order life cycle to help users who work on it to communicate useful information.

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td>

Add any additional notes, if required.

</td></tr><tr><td>

Parent

</td><td>

Select the parent record from the list.

</td></tr><tr><td colspan="2">

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

Estimated date when the latest task will be completed. The Lead Time for the maintenance schedule is subtracted from the Requested due by date for the work order to determine this date.

</td></tr><tr><td>

Latest completion date

</td><td>

Date when the previous work order for the schedule occurrence was completed.

</td></tr></tbody>
</table>**Parent Topic:**[Quality issue management form](mco-qim-form.md)

**Related topics**  


[Create a work order](../task/mco-create-work-order.md)

