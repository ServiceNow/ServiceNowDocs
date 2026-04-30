---
title: Connect to an RPA Hub instance from Attended Robot
description: Connect to an RPA Hub instance in three ways by using the Connection Manager so that you can establish a connection between the Attended Robot and ServiceNow RPA Hub instance.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Attended Robot, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Connect to an RPA Hub instance from Attended Robot

Connect to an RPA Hub instance in three ways by using the Connection Manager so that you can establish a connection between the Attended Robot and ServiceNow RPA Hub instance.

## Before you begin

Establish a connection between the Attended Robot and ServiceNow RPA Hub instance. For more information, see [Set up Attended Robot](set-up-rda-runtime.md).

Role required: none

## Procedure

1.  To connect to an RPA Hub instance, do any of the following actions in the Connection Manager dialog box.

<table id="choicetable_ag1_lyx_jrb"><thead><tr><th align="left" id="d331817e104">

Option

</th><th align="left" id="d331817e107">

Action

</th></tr></thead><tbody><tr><td id="d331817e113">

**If there is a single instance**

</td><td>

1.  In the RPA Hub section, select the RPA Hub instance.
2.  Select **Connect**.


</td></tr><tr><td id="d331817e140">

**If there are multiple instances and none of them are marked as default**

</td><td>

1.  In the RPA Hub section, select an RPA Hub instance.
2.  Select **Proceed**.
3.  In the RPA Hub section, select the RPA Hub instance.
4.  Select **Connect**.
5.  Enter a user name and password.
6.  From the Domain list, select a domain.
7.  Select **Log in**.


</td></tr><tr><td id="d331817e195">

**If an instance is marked as default**

</td><td>

1.  Enter a user name and password.
2.  From the Domain list, select a domain.
3.  Select **Log in**.


</td></tr></tbody>
</table>2.  In the Connection Manager dialog box, set the permission for the Attended Robot application to connect to your ServiceNow instance and access data.

    -   To allow Attended Robot to connect to your ServiceNow instance and access data, select **Allow**.
    -   To prevent Attended Robot from connecting to your ServiceNow instance and accessing data, select **Deny**. You won't be able to proceed further.

