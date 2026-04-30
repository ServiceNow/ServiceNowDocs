---
title: Submit a complaint through Employee Center
description: Submit a complaint through the Employee Center portal to report a compliance violation incident for investigation and resolution.Submit a complaint through the Legal menu in the Employee Center portal.Submit a complaint through the Quick Link in the Employee Center portal.
locale: en-US
release: xanadu
product: Legal Investigations
classification: legal-investigations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Submitting a complaint for investigation, Legal Investigations, Legal Service Delivery Practice Applications, Legal Service Delivery, Employee Service Management]
---

# Submit a complaint through Employee Center

Submit a complaint through the Employee Center portal to report a compliance violation incident for investigation and resolution.

## Before you begin

Role required: sn\_lg\_ops.legal\_user

## About this task

To submit a complaint anonymously, see [Submit a complaint through the Anonymous Report Center portal](submit-complaint-arc.md).

## Procedure

1.  In the Employee Center portal, submit a complaint using either the **Legal** menu or the **Quick links** section.


**Parent Topic:**[Submitting a complaint for investigation](../concept/submitting-legal-investigations-request.md)

**Related topics**  


[Submit a complaint through Legal Service Portal](submit-complaint-legal-svc-portal-1.md)

[Submit a complaint through the Anonymous Report Center portal](submit-complaint-arc.md)

## Submit a complaint through the Legal menu in Employee Center

Submit a complaint through the Legal menu in the Employee Center portal.

### Before you begin

Role required: sn\_lg\_ops.legal\_user

### About this task

**Note:** This option is available if the admin has activated the record producer that is mapped to the Ethics \[sn\_lg\_ops\_ethics\] table. For more information, see [Record producers for legal investigations](../reference/record-producers-legal-investigation.md).

### Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  In the Employee Center portal, click the **Legal** menu and select the **Ethics and Compliance** option.

3.  In the Ethics and Compliance request category page, click **Ethics Complaints**.

4.  On the Ethics Complaints form, fill in the fields.

    For a description of the field values, see [Ethics complaints intake form](../reference/ethics-complaint-intake-form.md).

5.  To add an involved party, in the **Involved Parties** section, click **Add**.

    1.  In the Add Row dialog box, select an involved party type option to indicate if the involved party is an employee of the organization or a user from outside the organization.

    2.  Provide the involved party's name, email id, and other notes.

        **Note:** For an internal employee, the **Email id** field is auto-populated from the user's profile.

    3.  Click **Add**.

        The involved party record appears in the Involved Parties list on the Ethics Complaints intake form.

    Repeat these steps to add more involved parties.

6.  On the Ethics Complaints form, click **Submit**.


### Result

A legal request is created and assigned to a [request fulfiller or an assignment group as configured](../../legal-request-management/task/create-assignment-rules-intake-form.md).

## Submit a complaint through the Quick Link in Employee Center

Submit a complaint through the Quick Link in the Employee Center portal.

### Before you begin

Ensure that the record producer that is mapped to the Universal Request \[universal\_request\] table is activated. For more information, see [Record producers for legal investigations](../reference/record-producers-legal-investigation.md).

Ensure that the **Ethics Complaints** widget is added under Quick Links in the Employee Center. For more information, see [Modify the Quick links widget display](../../employee-center/task/config-quick-links-widget.md).

Role required: sn\_lg\_ops.legal\_user

### Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  In the Employee Center portal, click the **Ethics Complaints** link under the **Quick links** section.

3.  On the Ethics Complaints form, provide the summary of the complaint.

4.  In the **Detailed description** field, provide the details of the complaint, the names of the people involved, and the approximate date and time of the incident.

5.  Click **Add attachments** to upload any documents supporting your complaint.

6.  Click **Submit**.


### Result

A universal request is created and is assigned to the [the assignment group as configured](integrate-lsd-hrsd.md#step_li_prop_group). A universal request routing agent can triage and work on it.

