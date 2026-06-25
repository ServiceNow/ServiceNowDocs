---
title: Submit a complaint through Employee Center
description: Submit a complaint through the Employee Center portal to report a compliance violation incident for investigation and resolution.Submit a complaint through the Legal menu in the Employee Center portal.Submit a complaint through the Quick Link in the Employee Center portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/legal-investigations/submit-complaint-employee-center.html
release: australia
product: Legal Investigations
classification: legal-investigations
topic_type: task
last_updated: "2026-05-19"
reading_time_minutes: 3
breadcrumb: [Requests, Legal Investigations, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Submit a complaint through Employee Center

Submit a complaint through the Employee Center portal to report a compliance violation incident for investigation and resolution.

## Before you begin

Role required: sn\_lg\_ops.legal\_user

## About this task

To submit a complaint anonymously, see [Submit a complaint through the Anonymous Report Center portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-investigations/submit-complaint-arc.md).

## Procedure

1.  In the Employee Center portal, submit a complaint using either the **Help center** &gt; **Legal services** menu or the **Quick links** section.


**Parent Topic:**[Submitting a complaint for investigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-investigations/submitting-legal-investigations-request.md)

**Related topics**  


[Submit a complaint through Legal Service Portal]()

[Submit a complaint through the Anonymous Report Center portal]()

## Submit a complaint through the Legal menu in Employee Center

Submit a complaint through the Legal menu in the Employee Center portal.

### Before you begin

Role required: sn\_lg\_ops.legal\_user

### About this task

**Note:** This option is available if the admin has activated the record producer that is mapped to the Ethics \[sn\_lg\_ops\_ethics\] table. For more information, see [Record producers for legal investigations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-investigations/record-producers-legal-investigation.md).

### Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  Navigate to **Help center** &gt; **Legal services**

3.  Select the **Ethics and Compliance** option.

4.  In the Ethics and Compliance request category page, click **Ethics Complaints**.

5.  On the Ethics Complaints form, fill in the fields.

    For a description of the field values, see [Ethics complaints intake form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-investigations/ethics-complaint-intake-form.md).

6.  To add an involved party, in the **Involved Parties** section, click **Add**.

    1.  In the Add Row dialog box, select an involved party type option to indicate if the involved party is an employee of the organization or a user from outside the organization.

    2.  Provide the involved party's name, email id, and other notes.

        **Note:** For an internal employee, the **Email id** field is auto-populated from the user's profile.

    3.  Click **Add**.

        The involved party record appears in the Involved Parties list on the Ethics Complaints intake form.

    Repeat these steps to add more involved parties.

7.  On the Ethics Complaints form, click **Submit**.


### Result

A legal request is created and assigned to a [request fulfiller or an assignment group as configured](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-request-management/create-assignment-rules-intake-form.md).

## Submit a complaint through the Quick Link in Employee Center

Submit a complaint through the Quick Link in the Employee Center portal.

### Before you begin

Role required: sn\_lg\_ops.legal\_user

### About this task

**Note:** This option is available if the admin has activated the record producer that is mapped to the Universal Request \[universal\_request\] table. For more information, see [Record producers for legal investigations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-investigations/record-producers-legal-investigation.md).

### Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  In the Employee Center portal, click the **Ethics Complaints** link under the **Quick links** section.

3.  On the Ethics Complaints form, provide the summary of the complaint.

4.  In the **Detailed description** field, provide the details of the complaint, the names of the people involved, and the approximate date and time of the incident.

5.  Click **Add attachments** to upload any documents supporting your complaint.

6.  Click **Submit**.


### Result

A universal request is created and is assigned to the [the assignment group as configured](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-investigations/integrate-lsd-hrsd.md). A universal request routing agent can triage and work on it.

