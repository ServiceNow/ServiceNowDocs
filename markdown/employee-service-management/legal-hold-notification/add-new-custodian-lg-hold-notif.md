---
title: Add a new custodian to an existing legal hold matter
description: Add a new custodian to issue the legal hold notice if a user is later identified as responsible for preserving data relevant to the existing legal hold.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/legal-hold-notification/add-new-custodian-lg-hold-notif.html
release: australia
product: Legal Hold Notification
classification: legal-hold-notification
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Legal Hold Notification, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Add a new custodian to an existing legal hold matter

Add a new custodian to issue the legal hold notice if a user is later identified as responsible for preserving data relevant to the existing legal hold.

## Before you begin

Role required: sn\_lg\_hold.legal\_hold\_fulfiller

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Select the List icon \(\[Omitted image "lsd-lcc-list-icon.png"\] Alt text: List icon\).

3.  In the **Default list** tab, navigate to **Matters** &gt; **All**

4.  Select the legal hold matter from the list.

5.  In the **Custodians** tab, select **New**.

6.  On the Create New Custodians form, in the **Custodian name** field, select the Search for Record icon \(\[Omitted image "lookup-using-list.png"\] Alt text:\) and search for and select the custodian name.

    Only users with the custodian role are available in the list. For more information, see [Assign the legal user role to a custodian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-hold-notification/assign-user-lg-hold-cust.md).

7.  On the form, fill in the remaining fields.

<table id="table_cpf_5yx_rfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Legal matter

</td><td>

Legal matter with which the custodian is associated.This field is automatically set to the parent matter number and a description.

</td></tr><tr><td>

Custodian email

</td><td>

Email of the custodian.This field is automatically set to the custodian’s email when the custodian is selected.

</td></tr><tr><td>

Data sources

</td><td>

Data source type related to the legal hold matter such as documents, spreadsheets, presentations, emails, and attachments.

</td></tr></tbody>
</table>8.  Select **Save**.

    -   A new custodian is added under the **Custodians** tab.
    -   A new task is created for a new custodian under the **Tasks** tab, with the initial state set to Draft.
9.  Issue a legal hold notice to the newly added custodian.

    1.  In the legal matter page, select **Preview and issue hold**.

    2.  In the legal hold notice, select **Edit**.

        A legal hold notice opens in an editable format.

        \[Omitted image "Customize-legal-hold-notice-template.png"\] Alt text: Legal hold notice template

    3.  Customize the template by substituting your company's name for the placeholder text and adding any additional information you want to include.

        **Warning:** Do not modify the JavaScript variables marked with $\{ \} in the legal hold template. Editing these variables might corrupt the template and prevent the legal hold notice from being generated.

        If you want to revert the changes, select **Discard changes**.

    4.  Select **Save and preview**.

    5.  Review the edited legal hold notice and select **Issue legal hold**.


## Result

The message **Legal hold notice has been sent to X custodians** appears in the **Activity** section.

A legal hold notice is issued to the custodian via email, with the fulfiller copied in the **Cc** field.

In the **Tasks** tab, the state of the task changes from Draft to Assigned.

In the **Artifacts** tab, the legal hold notice sent to the custodian is automatically attached.

**Parent Topic:**[Using Legal Hold Notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-hold-notification/use-lg-hold-notif.md)

