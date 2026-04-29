---
title: Create a record from incident
description: Create a problem, change, or request record from an incident.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Create a record from incident

Create a problem, change, or request record from an incident.

## Before you begin

Role required: itil, itil\_admin, or admin

## About this task

When the cause of an incident is an error or widespread issue, a problem is generated from the incident. When the issue requires a change to the infrastructure or a business service, a change record is created from the incident. When the resolution for the user is to request hardware or software, a request is created from an incident.

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  Open the incident record.

3.  Right-click on the header form and on the context menu, select the appropriate option.

<table id="choicetable_s5g_lgw_xy"><thead><tr><th align="left" id="d75054e108">

Task record

</th><th align="left" id="d75054e111">

Option

</th></tr></thead><tbody><tr><td id="d75054e117">

**Problem**

</td><td>

Create Problem. For more information, refer to [Create a problem](../../problem-management/task/create-a-problem-v2.md).**Note:** Use the property **List of attributes \(comma-separated\) that will be copied from the incident to create a new problem** \(**com.snc.problem.create\_from\_incident.attributes**\) to specify fields on the Incident form. The values of these fields are copied to the respective fields on the Problem form. The property is available for customers starting the Madrid release.

</td></tr><tr><td id="d75054e142">

**Request**

</td><td>

Create Request. For more information, refer to [Create a request from an incident](create-request-from-incident.md).

</td></tr><tr><td id="d75054e158">

**Change**

</td><td>

Create Normal, Standard, or Emergency Change. For more information, refer to [Create a change request](../../change-management/task/t_CreateAChange.md).**Note:**

The **Create Normal Change**, **Create Standard Change**, and **Create Emergency Change** scripts copy these fields from the Incident form:

-   short\_description
-   description
-   cmdb\_ci
-   priority
-   company
The syntax for copying a field from the Incident form to the Change form is:

`changeRequest.setValue("field_name", current.field_name);`. The admin adds this information in the script block of the incident record.

</td></tr></tbody>
</table>    The form for the new record appears and is already saved. Some specific fields are copied to the newly generated record from the incident. You can find reference of the newly created task record in the Related Records section of the Incident form.

4.  Complete the Problem, Change, or Request form with additional information and click **Update**.


