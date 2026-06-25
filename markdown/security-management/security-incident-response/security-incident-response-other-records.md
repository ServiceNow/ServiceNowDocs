---
title: Security Incident Response Other Records
description: This section displays the other records such as IT related records and email records. Under IT records, Incident, Change Request, Problem and Outages are displayed.Create an incident within a security incident.Link related multiple IT Service Management \(ITSM\) incidents, problems or change requests to a security incident.Create a problem task.Create a change request.Crete an outage from an incident to track the down time of a configuration item.As an analyst, you can compose emails directly from security incidents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/security-incident-response-other-records.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Response Other Records

This section displays the other records such as IT related records and email records. Under IT records, Incident, Change Request, Problem and Outages are displayed.

Under Email, Draft, Sent Emails and Received Emails are displayed.

\[Omitted image "other-records.png"\] Alt text: Other Records tab

**Parent Topic:**[Working with Security Incident Records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/using-analyst-workspace.md)

**Related topics**  


[Security Incident Overview section]()

[Security Incident Details section]()

[SIR Workspace Orchestration]()

[Security Incident Response Tasks]()

[Security Incident Response Post Incident Review]()

[Update information in security incident related records]()

[TISC integration within SIR Workspace]()

[Reports in Security Incident Response]()

[Collaborate using conference call or chat in Security Incident Response]()

[Viewing incident details with a relationship graph]()

[MITRE attack and defend technique graph]()

[View and filter the incident timeline]()

## Create an incident

Create an incident within a security incident.

### Before you begin

Role required: sn\_si.analyst.

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Open any incident record.

3.  Click **Create Incident**.

    \[Omitted image "create-incident.png"\] Alt text: create incident

4.  Enter the details such as Configuration Item, Impact, Urgency, Location, Priority, and Short Description.

5.  Click **Create**.

6.  An incident gets created.


## Link multiple ITSM incidents, problems or change requests to a security incident

Link related multiple IT Service Management \(ITSM\) incidents, problems or change requests to a security incident.

### Before you begin

Role required: sn\_si.analyst

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Select the Security Incidents icon \[Omitted image "listview-icon.png"\] Alt text:.

3.  Open the incident record.

4.  Select the **Other Records** tab.

5.  Under **IT records**, select **Incident** or **Problems** or **Change Requests**.

6.  Select **Link**.

7.  Select the ITSM record you want to link to the selected security incident.

8.  Select **Link**.


### Result

The selected ITSM records are listed in the IT records section of the selected security incident record.

## Create a problem task

Create a problem task.

### Before you begin

Role required: sn\_si.analyst

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Open any incident record.

3.  Select **Create Problem**.

4.  Fill in the details such as Configuration Item, Location, Impact, Urgency, Priority, and Short description.

5.  Select **Create**.

6.  A problem task gets created.


## Create a change request

Create a change request.

### Before you begin

Role required: sn\_si.analyst.

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Open any incident record.

3.  Click **Create Change Request**.

4.  Enter the details such as Configuration Item, Location, Priority, and Short description.

5.  Click **Create**.

6.  A change request gets created.


## Create outage

Crete an outage from an incident to track the down time of a configuration item.

### Before you begin

Role required: sn\_si.analyst

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Open any incident record.

3.  Click **Create outage**.

4.  Enter the details such as Configuration Item, Begin date, End date, Type, and Short description.

5.  Click **Create**.


## Compose Emails

As an analyst, you can compose emails directly from security incidents.

### Before you begin

Role required: sn\_si.analyst

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Select and open the incident for which you want to compose an email.

3.  Click the overflow and select **Compose Email**.

    \[Omitted image "compose-email-form-ui.png"\] Alt text: User Reported Phishing view: Compose Email section.

4.  Enter the **To** and **CC** field.

5.  **Add** attachments, if any.

6.  Within the Email form, click **Quick Messages** to view the quick messages which is displayed on the right side of the **Compose Emails** section.

    The available quick messages are displayed. Select the message and click **Insert**. The messages gets inserted in the body of the email.

    \[Omitted image "quick-message-insert.png"\] Alt text: User Reported Phishing email.

7.  Compose your email and click **Send Email**.

    **Note:** You can save an email as a draft. These draft emails will be available under the Other records tab.

    **How to configure Quick Messages:**

    1.  Navigate to **All** &gt; **System Definitions** &gt; **Tables**.

    2.  Search for **Quick Message \(sys\_email\_canned\_message\)** table.

        \[Omitted image "quick-messages-table.png"\] Alt text: System Definitions

    3.  Go to **Related Links** &gt; **Show List**.

    4.  Create **New**.

    5.  Enter the **Title**, **body of the message**, select the **Table: Security Incident \(sn\_si\_incident\)** and **Active** check box.

        \[Omitted image "quick-msg-new-record.png"\] Alt text: Quick message - New record.

    6.  Click **Submit**.

        After a new entry is created within the table, the quick message appears in the contextual menu.

8.  Click **Templates** to add any template if required.

9.  Select the **Response Template** and click **Copy to clipboard** and apply the template, if required.

    \[Omitted image "emil-template.png"\] Alt text: Compose email template. **How to configure Response Templates:**

    1.  Navigate to **System Definitions** &gt; **Tables**.

    2.  Search for the **Response Template \(sn\_templated\_snip\_note\_template\)** table.

        \[Omitted image "response-template.png"\] Alt text: Response Template Table.

    3.  Go to **Related Links** &gt; **Show List**.

    4.  Create **New**.

    5.  Enter the **Name**, **Short Name**, select the **Table: Security Incident \(sn\_si\_incident\)** and **Template body**.

        \[Omitted image "response-template-new-record.png"\] Alt text: Response Template: record view.

    6.  Click **Submit**.

        After a new entry is created within the table, the new template appears in the contextual menu.


