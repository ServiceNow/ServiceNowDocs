---
title: Create an Agent Client Collector configuration data file
description: Create an Agent Client Collector configuration data file and associate it with check definitions so that you can view the information about your instance. You can also add or delete an attachment to the configuration data files, which are used by check definitions during check executions.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Create an Agent Client Collector configuration data file

Create an Agent Client Collector configuration data file and associate it with check definitions so that you can view the information about your instance. You can also add or delete an attachment to the configuration data files, which are used by check definitions during check executions.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

A check definition is an individual check entry in the system. For details, see [Agent Client Collector configuration data files](../concept/acc-config-data-files.md).

Configuration data file attachments contain instance data, such as configuration item \(CI\) information, which is used when executing a check.

Domain separation is supported in the Agent Client Collector configuration data files.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Configuration** &gt; **Configuration Files**.

2.  Select **New**.

3.  Add or remove an attachment.

<table id="choicetable_v1p_3mr_3zb"><thead><tr><th align="left" id="d625990e116">

Action

</th><th align="left" id="d625990e119">

Description

</th></tr></thead><tbody><tr><td id="d625990e125">

**Add a file**

</td><td>

Synchronize the record and the relevant MID Servers.1.  Select the paper clip icon ![Paper clip icon.](../image/paper-clip-icon.png).

The Attachments dialog box opens.

2.  Select **Choose file** and select a file to attach.
3.  Close the Attachments dialog box.


</td></tr><tr><td id="d625990e159">

**Delete a file**

</td><td>

Optionally, delete an attachment you don’t want to be associated with the record.1.  Select **Manage Attachments**.

The Attachments dialog box opens.

2.  Select the check box next to the attachment that you want to remove.
3.  Select **Remove**.


</td></tr></tbody>
</table>    The attachment name must be unique for each domain and can consist only of alphanumeric characters.

    If the attachment contains invalid characters or is a duplicate of another attachment, the following situations occur:

    -   The configuration file is automatically set to **Active = False**.
    -   A message appears in the Error column indicating a problem with the attachment.
    Each record can contain only one attachment.

4.  In the **Description** field, enter a description for the configuration data file.

5.  Select **Submit**.


## Result

-   The configuration data file is listed on the Agent Client Collector Configuration File page.
-   The **Name** value is automatically set to the name of the attachment.

Checks use the configuration data file with instance data during check execution.

**Parent Topic:**[Deploying Agent Client Collector on servers](../concept/acc-server-deployment.md)

