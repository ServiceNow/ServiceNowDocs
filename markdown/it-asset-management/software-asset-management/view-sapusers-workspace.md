---
title: View SAP users in workspace
description: View all the discovered users pulled from the SAP systems in the Software Asset Workspace.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# View SAP users in workspace

View all the discovered users pulled from the SAP systems in the Software Asset Workspace.

## Before you begin

The Discovered Users \[samp\_discovered\_user\] table maps the discovered SAP users to system user records in the Users \[sys\_user\] table.

Role required: sam\_admin or sam\_user

## Procedure

1.  Navigate to **All** &gt; **Software asset** &gt; **Software Asset Workspace** &gt; **License operations**.

2.  Select **All SAP users**.

3.  Select a record to view details such as SAP user roles, SAP user active transactions, SAP user activities, and SAP web activities.

    -   SAP User Roles \[samp\_sap\_user\_has\_role\]: SAP users and their assigned roles.
    -   SAP User Active transactions \[samp\_named\_user\_type\_has\_transactions\]: Data related to a named user's transaction activity on a SAP client. User transaction activity is based on SAP transaction codes, which are shortcuts for performing transactions or tasks on an SAP client. For example, the ME21N transaction code enables you to create a purchase order in SAP.
    -   SAP User Activity \[samp\_sap\_user\_activity\]: Data related to a user’s activity on a SAP client, such as the amount of time spent on a SAP system or the number of database records created or updated.
    -   SAP Web Activity \[samp\_sap\_web\_activity\]: Data related to web activity or RFC connections performed on the SAP client, such as the number of calls or amount of data received or sent by each connection.

**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

