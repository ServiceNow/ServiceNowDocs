---
title: Customize the URL and REST API task parameters for EMR systems
description: Use scripted extension points to manipulate URL parameters and REST API task parameters for an EMR system.
locale: en-US
release: zurich
product: EMR Help
classification: emr-help
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Customize the URL and REST API task parameters for EMR systems

Use scripted extension points to manipulate URL parameters and REST API task parameters for an EMR system.

## Before you begin

Install the EMR Help application. For more information, see [Install EMR Help](install-emr-help.md).

Role required: admin

## About this task

By using extension points, you can easily integrate customizations without having to alter the base code. You can extend standard base functionality using customized scripts. For more information, see [Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** column, search for and select **sn\_ind\_rmt\_help.RemoteHelpParamTransformer**.

3.  On the Extension Point form, either modify a script include to use the sn\_ind\_rmt\_help.RemoteHelpParamTransformer extension point or create and register a custom script include.

    -   Create and register a custom script include.

        For more information, see [Registering custom script includes against the scripted extension points](https://www.servicenow.com/docs/access?context=impl-scripted-ext-pts-custom-code&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

    -   Modify the existing script include by going to the Implementations related list and selecting a script include in the **Class** column.

        **Note:** By default, the RemoteHelpParamTransformer script include that use the sn\_ind\_rmt\_help.RemoteHelpParamTransformer extension point is available for the EMR Help application.

4.  Customize parameters for an EMR system by adding the sn\_ind\_rmt\_help.RemoteHelpParamTransformer extension point to the script include.

    You can create multiple implementations for an extension point and provide an order number for each implementation. The implementation that has the lowest order number is executed first.

<table id="table_czh_m5m_5nb"><thead><tr><th>

Customization

</th><th>

Implementation

</th></tr></thead><tbody><tr><td>

Incoming task parameters

</td><td>

Include the transformIncomingTaskParams method in the sn\_ind\_rmt\_help.RemoteHelpParamTransf​ormer extension point. The method is called from the REST APIs prior to creating and updating IT service requests from an EMR system and enables you to modify any input parameters.

</td></tr><tr><td>

Outgoing task parameters

</td><td>

Include the transformOutgoingTaskParams method in the sn\_ind\_rmt\_help.RemoteHelpParamTransformer extension point. The method is called from the REST APIs for getting a task list and task details before sending the task-related data to the EMR system.

</td></tr><tr><td>

Incoming URL parameters

</td><td>

Include the transformURLParams method in the sn\_ind\_rmt\_help.RemoteHelpParamTransformer extension point. This method is called from a service portal before storing the URL parameters.

**Note:** If your EMR system has an encryption algorithm, you can configure the Incoming URL parameters method in the sn\_ind\_rmt\_help.RemoteHelpParamTransformer extension point to decrypt any encrypted task parameters from your ServiceNow instance.

</td></tr></tbody>
</table>5.  On the Extension Point form, click **Update**.


