---
title: Configure request definitions for EMR systems
description: Create or modify request definitions to accept service requests from an EMR system on your ServiceNow instance.
locale: en-US
release: xanadu
product: EMR Help
classification: emr-help
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring EMR Help, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure request definitions for EMR systems

Create or modify request definitions to accept service requests from an EMR system on your ServiceNow instance.

## Before you begin

-   Set the application scope to EMR Help using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).
-   Ensure that request parameters and equivalent columns for all request parameters exist in the Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table. For more information, see [Configure request parameters for EMR systems](configure-emr-help-req-parm.md).

Role required: sn\_ind\_rmt\_help.admin or admin

## About this task

A request definition is a model of the request type originated from an EMR system. By default, the IT Service Request \[sn\_it\_request\] request definition is provided for task records of type Incident and mapped to the EMR system. The parameters associated with this request definition are also predefined and mapped to the columns in the Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table or its extended data table \(for example, EMR Request Data \[sn\_ind\_rmt\_help\_incident\_data\] table\).

**Note:** A user with the sn\_ind\_rmt\_help.admin role can't delete the predefined request definition and configuration mapping settings.

## Procedure

1.  Navigate to **All** &gt; **EMR Help** &gt; **Administration** &gt; **Request Definitions**.

2.  In the Remote Request Definitions list, modify an existing request definition or create another request definition.

    -   To modify an existing request definition, click a request definition in the **ID** column of the Remote Request Definitions list.
    -   To create another request definition, click **New** in the Remote Request Definitions list.
3.  On the form, fill in the fields.

<table id="table_x4l_sdh_4nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ID

</td><td>

Unique identifier for the request definition.

**Note:** You can't modify an ID after the request definition is created.

</td></tr><tr><td>

Name

</td><td>

Name to identify the request definition.

</td></tr><tr><td>

Task type

</td><td>

Task table associated with the IT service request.

 For example, Incident \[incident\] table.

</td></tr><tr><td>

Request data table

</td><td>

Data table to store additional data from the EMR system.

 Additional data might include environment, workstation, and other data from the EMR system.

</td></tr><tr><td>

Record producer

</td><td>

Record producer to modify the fields in a task record and make them available on an IT service request form.

 You use a record producer with a dedicated service portal.

</td></tr><tr><td class="sub-head" colspan="2">

Rest API Task Parameters

</td></tr><tr><td colspan="2">

Parameters of scripted REST APIs. You can use scripted REST APIs with system support modules. For more information, see [Remote help request API](https://www.servicenow.com/docs/access?context=remote_help_request-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Task create parameters

</td><td>

Parameters of a task record available when creating an IT service request in the EMR system.

</td></tr><tr><td>

Task list parameters

</td><td>

Parameters of a task record available when viewing a list of IT service requests in the EMR system.

</td></tr><tr><td>

Task detail parameters

</td><td>

Parameters of a task record available when viewing the details of an IT service request in the EMR system.

</td></tr><tr><td>

Task update parameters

</td><td>

Parameters of a task record available when updating an IT service request in the EMR system.

</td></tr></tbody>
</table>    **Note:** To be able to enter Rest API task parameters, click the lock icon corresponding to the parameter type. For example, to enter task create parameters:

    1.  Click the unlock task create parameters icon \(![Unlock task create parameters icon.](../image/lock.png)\).
    2.  Move the desired parameters from the available parameters in the **Available** column to the **Selected** column.
    3.  Click the up or down icon to arrange the parameters in the order in which you want them to appear on the IT service request page of the EMR system, and then click the lock task create parameters icon \(![Lock task create parameters icon.](../image/unlock.png)\).
4.  Save the remote request definition settings.

    -   To save a new request definition, click **Submit**.
    -   To save the changes to an existing request definition, click **Update**.
5.  Store the data from a request parameter into the Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table by mapping the request parameter to a column in the request data table.

    1.  In the Request configuration mappings section, modify an existing configuration mapping or create another configuration mapping.

        -   To modify an existing configuration mapping, click the preview icon \(![Preview icon.](../image/preview.png)\) next to a request parameter in the **Request parameter** column of the Request configuration mappings section and then click **Open Record**.
        -   To create another configuration mapping, click **New** in the Request configuration mappings section.
    2.  On the form, fill in the fields.

<table id="table_bls_xpj_qnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Request parameter

</td><td>

Request parameter received from the EMR system.

</td></tr><tr><td>

Request data column

</td><td>

Column name in the Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table or its extension in the ServiceNow instance.

</td></tr></tbody>
</table>        **Note:** You map one request parameter to a unique column in the data table. However, when similar parameters from different EMR systems are available, you can map them to the same column in the data table.

    3.  Save the configuration mapping.

        -   If you created a new configuration mapping, click **Submit**.
        -   If you modified an existing configuration mapping, click **Update**.

