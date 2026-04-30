---
title: Security Incident Response Other Records
description: This section displays the other records such as IT related records and email records. Under IT records, Incident, Change Request, Problem and Outages are displayed.Create an incident within a security incident.Link related multiple IT Service Management \(ITSM\) incidents, problems or change requests to a security incident.Create a problem task.Create a change request.Crete an outage from an incident to track the down time of a configuration item.As an analyst, you can compose emails directly from security incidents.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Response Other Records

This section displays the other records such as IT related records and email records. Under IT records, Incident, Change Request, Problem and Outages are displayed.

Under Email, Draft, Sent Emails and Received Emails are displayed.

![Other Records tab](../image/other-records.png "Other Records")

**Parent Topic:**[Working with Security Incident Records](using-analyst-workspace.md)

**Related topics**  


[Security Incident Overview section](security-incident-overview.md)

[Security Incident Details section](security-incident-details.md)

[SIR Workspace Orchestration](security-incident-response-workspace-orchestration-activities.md)

[Security Incident Response Tasks](security-incident-response-tasks.md)

[Security Incident Response Post Incident Review](security-incident-response-post-incident-review.md)

[Update information in security incident related records](../task/edit-related-records-in-list.md)

[TISC integration within SIR Workspace](../../secops-integration-threat-security-center/concept/tisc-sir-workspace.md)

[Reports in Security Incident Response](report-templates-sir.md)

[Collaborate using conference call or chat in Security Incident Response](collab-sir-call-chat.md)

[Viewing incident details with a relationship graph](sir-relationship-graph.md)

[MITRE attack and defend technique graph](mitre-attack-defend-graph-sir.md)

## Create an incident

Create an incident within a security incident.

### Before you begin

Role required: sn\_si.analyst.

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Open any incident record.

3.  Click **Create Incident**.

    ![create incident](../image/create-incident.png)

4.  Enter the details such as Configuration Item, Impact, Urgency, Location, Priority, and Short Description.

5.  Click **Create**.![Created incident](../image/incident-created.png)

6.  An incident gets created.


## Link multiple ITSM incidents, problems or change requests to a security incident

Link related multiple IT Service Management \(ITSM\) incidents, problems or change requests to a security incident.

### Before you begin

Role required: sn\_si.analyst

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Select the Security Incidents icon ![](../image/listview-icon.png).

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

3.  Click **Create Problem**.

    ![Create problem](../image/create-problem.png)

4.  Fill in the details such as Configuration Item, Location, Impact, Urgency, Priority, and Short description.

5.  Click **Create**.

    ![Created problem](../image/problem-creted.png "Create problem task")

6.  A problem task gets created.


## Create a change request

Create a change request.

### Before you begin

Role required: sn\_si.analyst.

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Open any incident record.

3.  Click **Create Change Request**.

    ![Create change request](../image/create-change-request.png)

4.  Enter the details such as Configuration Item, Location, Priority, and Short description.

5.  Click **Create**.

    ![Created change request](../image/created-change-request.png)

6.  A change request gets created.


## Create outage

Crete an outage from an incident to track the down time of a configuration item.

### Before you begin

Role required: sn\_si.analyst

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Open any incident record.

3.  Click **Create outage**.

    ![Create outage for a configuration item](../image/create-outage.png)

4.  Enter the details such as Configuration Item, Begin date, End date, Type, and Short description.

5.  Click **Create**.

    ![Create Outage](../image/created-outage.png)


## Compose Emails

As an analyst, you can compose emails directly from security incidents.

### Before you begin

Role required: sn\_si.analyst

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Select and open the incident for which you want to compose an email.

3.  Click the overflow and select **Compose Email**.

    ![User Reported Phishing view: Compose Email section.](../image/compose-email-form-ui.png)

4.  Enter the **To** and **CC** field.

    ![Compose email](../image/compose-email.png)

5.  **Add** attachments, if any.

6.  Within the Email form, click **Quick Messages** to view the quick messages which is displayed on the right side of the **Compose Emails** section.

    The available quick messages are displayed. Select the message and click **Insert**. The messages gets inserted in the body of the email.

    ![User Reported Phishing email.](../image/quick-message-insert.png)

7.  Compose your email and click **Send Email**.

    **Note:** You can save an email as a draft. These draft emails will be available under the Other records tab.

    **How to configure Quick Messages:**

    1.  Navigate to **System Definitions** &gt; **Tables**.

    2.  Search for **Quick Message \(sys\_email\_canned\_message**\) table.

        ![System Definitions](../image/quick-messages-table.png)

    3.  Go to **Related Links** &gt; **Show List**.

    4.  Create **New**.

    5.  Enter the **Title**, **body of the message**, select the **Table: Security Incident \(sn\_si\_incident\)** and **Active** check box.

        ![Quick message - New record.](../image/quick-msg-new-record.png)

    6.  Click **Submit**.

        After a new entry is created within the table, the quick message appears in the contextual menu.

8.  Click **Templates** to add any template if required.

9.  Select the **Response Template** and click **Copy to clipboard** and apply the template, if required.

    ![Compose email template.](../image/emil-template.png) **How to configure Response Templates:**

    1.  Navigate to **System Definitions** &gt; **Tables**.

    2.  Search for the **Response Template \(sn\_templated\_snip\_note\_template\)** table.

        ![Response Template Table.](../image/response-template.png)

    3.  Go to **Related Links** &gt; **Show List**.

    4.  Create **New**.

        ![Creating a New template and viewing available Response Templates.](../image/create-new-response-template.png)

    5.  Enter the **Name**, **Short Name**, select the **Table: Security Incident \(sn\_si\_incident\)** and **Template body**.

        ![Response Template: record view.](../image/response-template-new-record.png)

    6.  Click **Submit**.

        After a new entry is created within the table, the new template appears in the contextual menu.


