---
title: Configure request parameters for EMR systems
description: Define parameters to include EMR variables from an EMR system in a ServiceNow service request.
locale: en-US
release: australia
product: EMR Help
classification: emr-help
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure request parameters for EMR systems

Define parameters to include EMR variables from an EMR system in a ServiceNow service request.

## Before you begin

Role required: sn\_ind\_rmt\_help.admin or admin

## About this task

Parameters are EMR variables defined in an EMR system that enrich a service request.

You can also create system-specific parameters as remote request parameters to send data as EMR variables that are automatically populated on the help form of a request. For example, you can use a system-specific parameter to store the workstation or environment setting for a user.

## Procedure

1.  Navigate to **All** &gt; **EMR Help** &gt; **Administration** &gt; **Request Parameters**.

2.  In the Remote Request Parameters list, modify an existing parameter or create another parameter.

    -   To modify an existing request parameter, select the parameter in the **ID** column of the Remote Request Parameters list.
    -   To create another request parameter, click **New** in the Remote Request Parameters list.
3.  On the form, fill in the fields.

<table id="table_x4l_sdh_4nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ID

</td><td>

Unique identifier for the parameter made available to an EMR system.

**Note:** You can't modify an ID after the request definition is created.

</td></tr><tr><td>

Name

</td><td>

Name to identify the request parameter.

</td></tr><tr><td>

Active

</td><td>

Option for activating the request parameter.

</td></tr><tr><td>

Source system

</td><td>

EMR system to which the parameter is mapped.

 The source system types with which the parameter can be associated are:

-   **Epic**: Epic EMR system.
-   **Cerner**: Cerner EMR system.
-   **Any system**: Any type of EMR system, including an Epic EMR system or a Cerner EMR system.
**Note:** To add more source system entries, you can modify the dictionary entry of the **Source system** column of the Remote Request Parameter \[sn\_ind\_rmt\_help\_request\_param\] table.

</td></tr><tr><td>

Sensitive data

</td><td>

Option to indicate that the parameter contains sensitive data.

</td></tr></tbody>
</table>4.  Save the remote request parameter settings.

    -   To save a new parameter, click **Submit**.
    -   To save the changes to an existing parameter, click **Update**.
5.  If you have created a new request parameter, add an equivalent column in the Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table or its extended child data table.

    **Note:** If a column for an EMR variable already exists in the data table, you can reuse the same column instead of creating another column. For example, if you have multiple EMR systems with a few common EMR variables, you can map the common variable from different EMR systems to the same column in the data table.


