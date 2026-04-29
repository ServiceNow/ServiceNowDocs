---
title: Issue a legal hold notice
description: Issue the legal hold notice to the custodian to ensure timely preservation of relevant data.
locale: en-US
release: australia
product: Legal Hold Notification
classification: legal-hold-notification
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Legal Hold Notification, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Issue a legal hold notice

Issue the legal hold notice to the custodian to ensure timely preservation of relevant data.

## Before you begin

Role required: sn\_lg\_hold.legal\_hold\_fulfiller

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Select the List icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

3.  In the **Default lists** tab, navigate to **Matters** &gt; **All**

4.  Select the legal matter from the list.

5.  Select **Start work**.

    The legal matter state changes from Assigned to Work in progress.

6.  In the legal matter page, select **Preview and issue hold**.

    The legal hold notice appears in the window.

7.  Select **Edit**.

    A legal hold notice opens in an editable format.

    ![Legal hold notice template](../image/Customize-legal-hold-notice-template.png)

8.  Customize the notice by substituting your organization's company name for placeholder text and adding any additional text you want to include.

    **Warning:** Do not modify the JavaScript variables marked with $\{ \} in the legal hold template. Editing these variables might corrupt the template and prevent the legal hold notice from being generated.

    If you need to revert changes, select **Discard changes**.

9.  Select **Save and preview**.

10. Review the edited legal hold notice and select **Issue legal hold**.


## Result

In the **Activity** section, a message is displayed as **Legal hold notice has been sent to X custodians**.

In the **Tasks** tab, the state of the task assigned to the custodian changes from Draft to Assigned.

A legal hold notice is issued to the custodian via email, with the fulfiller copied in the **Cc** field.

A copy of the legal hold notice sent to the custodian is attached under the **Artifacts** tab within the corresponding legal matter.

**Parent Topic:**[Using Legal Hold Notification](../concept/use-lg-hold-notif.md)

