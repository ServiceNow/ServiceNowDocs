---
title: View active transaction codes for your SAP users
description: View the SAP transaction codes \(t-codes\) that were actively used by your SAP users. This list is compared against your reclamation rules to determine whether the user is assigned an optimized license.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [User transaction activity for named user types, Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# View active transaction codes for your SAP users

View the SAP transaction codes \(t-codes\) that were actively used by your SAP users. This list is compared against your reclamation rules to determine whether the user is assigned an optimized license.

## Before you begin

Role required: admin

**Important:** You can view these SAP transaction codes in both the Software Asset Management classic application and the Software Asset Workspace. The following steps provide details on viewing these transaction codes in the Software Asset Management classic application. For details on viewing these transaction codes in the Software Asset Workspace, see [View SAP users in workspace](view-sapusers-workspace.md).

## Procedure

1.  On the page header of your ServiceNow® instance, select **All**.

2.  In the menu navigation filter, enter `samp_sap_system_user_list.do`.

    The SAP System Users \[samp\_sap\_system\_user\] table opens.

3.  Select the SAP user that you want to view active SAP transaction codes for.

4.  On the SAP System User record, select the **SAP User Active Transactions** related tab to view the complete list of SAP transaction codes that were discovered for the given user.


**Parent Topic:**[User transaction activity for named user types](../concept/sap-named-user-transaction-activity.md)

