---
title: Open cloud orchestrations
description: Cloud orchestration records show you the orders that your instance processed for each attempted operation on a stack. They also show you the values of the fields that the user submitted through the Cloud User Portal. Use cloud orchestrations to troubleshoot issues that occur when a user provisions a cloud resource or runs another operation on an existing cloud resource.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Troubleshooting tools for Cloud Provisioning and Governance, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Open cloud orchestrations

Cloud orchestration records show you the orders that your instance processed for each attempted operation on a stack. They also show you the values of the fields that the user submitted through the Cloud User Portal. Use cloud orchestrations to troubleshoot issues that occur when a user provisions a cloud resource or runs another operation on an existing cloud resource.

## Before you begin

Role required: sn\_cmp.cloud\_operator or sn\_cmp.cloud\_admin

## Procedure

1.  On the instance \(not the Cloud User Portal\), enter the following text into the application filter:

    ![Opening cloud orchestrations](../image/snmp-order-list.png)

    The list of Cloud Orchestrations appear.

2.  Sort and filter the list to find the error or other message you are looking for.

    For example, to sort the list by date, click the **Order Date** column. To show only errors that occurred, right-click **Error** in a cell and select **Show Matching**.

3.  Open a cloud orchestration record by clicking the **Order Date** field.

4.  Review the form fields:

    ![Cloud Orchestrations form](../image/cloud-orchestration-form.png)

    The example form shows you the type of message you can see when an operation fails due to the incorrect credentials. The OrderForm Data field shows the Sys ID of the credential record and the service account ID.

<table id="table_cwn_1jc_hfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Request Item

</td><td>

A service catalog request, if any, associated with this transaction.

</td></tr><tr><td>

Context Key

</td><td>

A key identifier for this message.

</td></tr><tr><td>

Context Object

</td><td>

This field is typically empty.

</td></tr><tr><td>

Context Instance

</td><td>

The blueprint used in transactions on a stack or the resource block used in transactions on a cloud resource.

</td></tr><tr><td>

Owner Instance

 Owner Table

</td><td>

The Owner Instance is the resource block on which the transaction took place. This field is only populated when the **Entity Type** is **Resource**.

 The owner table is always Stack \[sn\_cmp\_stack\] for the provisioning of a stack. Otherwise, the table is the CI type of the resource, such as Virtual Machine \[sn\_cmp\_vm\_instance\].

</td></tr><tr><td>

Entity Type

</td><td>

Whether the transaction occurred on **Blueprint** or a **Resource** \(resource block\).

</td></tr><tr><td>

Operation Name

</td><td>

The interface and operation that is triggered.

</td></tr><tr><td>

Order Date

</td><td>

The date of the transaction.

</td></tr><tr><td>

OrderForm Data

</td><td>

The data submitted through the user form.

</td></tr><tr><td>

Tag values

</td><td>

Any tag values involved in the transaction.

</td></tr><tr><td>

Resource

</td><td>

The resource block on which the operation took place. This field is populated only when the value of the Entity type field is **Resource**.

</td></tr><tr><td>

Status

</td><td>

The status of the message. If you are viewing an error, the **Error** option is listed.

</td></tr><tr><td>

Stack

</td><td>

The stack that the resource belongs to.

</td></tr><tr><td>

Status Message

</td><td>

The status message that explains the issue. Search the cloud provider documentation for the status codes and messages that appear in this field. The cloud provider might provide solutions available to you.

</td></tr><tr><td>

User

</td><td>

The user who triggered the operation.

</td></tr><tr><td>

Mid name

</td><td>

This field can show the name of the MID Server involved in the transaction. It is often left blank.

</td></tr></tbody>
</table>
