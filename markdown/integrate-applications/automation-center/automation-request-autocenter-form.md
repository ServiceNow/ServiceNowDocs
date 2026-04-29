---
title: Automation request form from Automation Center
description: Use the Automation request form to create an automation request, action request, or review request from Automation Center.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Automation Center, Workflow Data Fabric]
---

# Automation request form from Automation Center

Use the Automation request form to create an automation request, action request, or review request from Automation Center.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Request Type

</td><td>

Select the type of request you want to create.

 -   If you are creating an automation request, select **Automation**. Create automation requests when you want to automatically streamline your business processes, reduce the time that you spend on manual activities, and reduce your costs.

-   If you are creating an action request, select **Action**. Create action requests when you want an automated solution to repeated issues that are causing the automations to fail.

-   If you are creating a review request, select **Review**. Create a review request when you want the COE team to review an automation and analyze if the automation is required.


</td></tr><tr><td>

Number

</td><td>

Auto-generated number of the request.

</td></tr><tr><td>

Process name

</td><td>

Name of the process.

</td></tr><tr><td>

Description

</td><td>

Description about the process.

</td></tr><tr><td>

Department

</td><td>

Associated department of the process.

</td></tr><tr><td>

Number of steps

</td><td>

Steps that are involved in the process.

 A step is an individual activity, action, or decision that contributes to the completion of the process.

</td></tr><tr><td>

Interval type

</td><td>

Interval type of the manual business process execution:-   **Minutes**: The process executes every n minutes that you specify in the **Frequency** field.
-   **Hours**: The process executes every n hours that you specify in the **Frequency** field.
-   **Days**: The process executes every n days that you specify in the **Frequency** field.
-   **Weeks**: The process executes every n weeks that you specify in the **Frequency** field.
-   **Months**: The process executes every n months that you specify in the **Frequency** field.

</td></tr><tr><td>

Frequency

</td><td>

Number of times that the manual process must be executed per interval.

 For example, every 90 minutes or every 2 hours.

</td></tr><tr><td>

Actual time spent per run

</td><td>

Time that the manual process run takes to complete.

</td></tr><tr><td>

State

</td><td>

State of the automation request:-   New
-   Deferred
-   Rejected
-   Planned
-   In progress
-   Published

For more information about these states, see [Life-cycle stages of an automation request](lifecycle-stages-automation-req.md).

</td></tr><tr><td>

Intake source

</td><td>

Source type of the automation request, which refers to how the automation request is submitted:-   **Web**
-   **Integration**
-   **Process Mining**

**Note:** The default intake source type is **Web**.

This field is visible only when you submit the form.

</td></tr><tr><td>

Applications used

</td><td>

Associated business applications of the process.For example, Ariba, Microsoft Excel, or Google Chrome.

</td></tr><tr><td>

Requested for

</td><td>

Person responsible for designing an effective and efficient process.

</td></tr><tr><td class="sub-head" colspan="2">

Additional Details

</td></tr><tr><td>

Actual cost per run

</td><td>

Cost per process execution.

</td></tr><tr><td>

Goal

</td><td>

Desired goal of automating the process.

</td></tr><tr><td>

Priority

</td><td>

Complexity of the business process. Complexity is based on number of processes and applications involved, number of steps required, and human involvement.

</td></tr><tr><td>

Business criticality declared

</td><td>

Criticality of the business process. Criticality is based on your subjective assessment.

</td></tr><tr><td>

Number of users benefited

</td><td>

Number of users who would benefit with this process.

</td></tr><tr><td>

Number of transactions

</td><td>

Expected volume of transactions across the applications or systems.

</td></tr><tr><td>

Score

</td><td>

Execution priority of the request. The higher the score, the higher the priority of the request.

</td></tr><tr><td>

Process managers

</td><td>

Person responsible for the end-to-end execution of the process.

</td></tr><tr><td>

Assignment group

</td><td>

Name of the process group.

</td></tr><tr><td>

Manual steps %

</td><td>

Estimated percentage of steps that require human action to complete the process.

</td></tr><tr><td>

Expected cost savings per year

</td><td>

Cost saved per process at the end of a year.

</td></tr><tr><td>

Expected time savings per year

</td><td>

Time saved per process at the end of a year.

</td></tr><tr><td>

Work notes

</td><td>

Work notes for the process.

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td>

Notes that are visible to the customer.

</td></tr></tbody>
</table>**Parent Topic:**[Automation Center reference](../concept/automation-center-reference.md)

