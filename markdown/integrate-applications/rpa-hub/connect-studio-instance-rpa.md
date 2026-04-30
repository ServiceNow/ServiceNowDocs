---
title: Connect to an RPA Hub instance from RPA Desktop Design Studio
description: Connect to an RPA Hub instance in three ways using the Connection Manager so that you can establish a connection between the RPA Desktop Design Studio and ServiceNow RPA Hub instance.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Connect to an RPA Hub instance from RPA Desktop Design Studio

Connect to an RPA Hub instance in three ways using the Connection Manager so that you can establish a connection between the RPA Desktop Design Studio and ServiceNow RPA Hub instance.

## Before you begin

Set up the RPA Desktop Design Studio application to add ServiceNow instance details. For more information, see [Set up RPA Desktop Design Studio](set-up-rpa-studio.md).

Open an automation project. For more information, see [Open a local automation project in RPA Desktop Design Studio](open-project-rpa-studio.md) and [Open a cloud automation project in RPA Desktop Design Studio](open-project-remote-rpa-studio.md).

Role required: none

## About this task

After you launch the RPA Desktop Design Studio, you can connect to the same instance using different credentials.

You cannot connect to a different instance after the RPA Desktop Design Studio is launched.

To connect to a different instance, you must close and reopen the RPA Desktop Design Studio application.

## Procedure

1.  To connect to an RPA Hub instance, do any of the following actions in the Connection Manager dialog box.

<table id="choicetable_ag1_lyx_jrb"><thead><tr><th align="left" id="d300985e153">

Option

</th><th align="left" id="d300985e156">

Action

</th></tr></thead><tbody><tr><td id="d300985e162">

**If there is a single instance**

</td><td>

1.  In the RPA Hub section, select the RPA Hub instance.
2.  Select **Connect**.


</td></tr><tr><td id="d300985e189">

**If there are multiple instances and none of them are marked as default**

</td><td>

1.  In the RPA Hub section, select an RPA Hub instance.
2.  Select **Proceed**.
3.  In the RPA Hub section, select the RPA Hub instance.
4.  Select **Connect**.
5.  Enter a user name and password.
6.  From the Domain list, select a domain.
7.  Select **Log in**.


</td></tr><tr><td id="d300985e244">

**If an instance is marked as default**

</td><td>

1.  Enter a user name and password.
2.  From the Domain list, select a domain.
3.  Select **Log in**.


</td></tr></tbody>
</table>2.  In the Connection Manager dialog box, set the permission for the RPA Desktop Design Studio application to connect to your ServiceNow instance and to access the data:

    -   To enable RPA Desktop Design Studio to connect to your ServiceNow instance and access the data, select **Allow**.

        **Note:** When you enter credentials in the Connection Manager dialog box but do not select the **Allow** button, an error occurs after 30 minutes. Close the Connection Manager dialog box and reopen.

    -   To prevent RPA Desktop Design Studio from connecting to your ServiceNow instance and accessing the data, select **Deny**. You won't be able to proceed further.

