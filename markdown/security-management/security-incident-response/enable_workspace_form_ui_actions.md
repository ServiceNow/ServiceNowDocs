---
title: Working with Form UI actions
description: Following are the UI actions that are displayed on the security incident form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/enable\_workspace\_form\_ui\_actions.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 6
breadcrumb: [Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Working with Form UI actions

Following are the UI actions that are displayed on the security incident form.

To navigate to the form UI actions:

1.  Go to **Workspaces** &gt; **Security Incident Response Workspace**.
2.  Select any security incident from the list view.
3.  All the UI actions are present in the top-right corner of the security incident form.

<table id="table_jph_zrr_blb"><thead><tr><th>

Field Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Discuss**

</td><td>

Create or start a sidebar discussion for the security incident.

</td></tr><tr><td>

**Save**

</td><td>

Save or update the Security Incident Response record after making any changes.

</td></tr><tr><td>

**Create Response Task**

</td><td>

Create a response task for the security incident.

</td></tr><tr><td>

**Compose Emails**

</td><td>

Compose emails for the security incident.

</td></tr><tr><td>

**Add Playbook**

</td><td>

Add the playbook manually for the security incident.

</td></tr><tr><td>

**Create Incident**

</td><td>

Create an incident within the security incident.

</td></tr><tr><td>

**Create Customer Service Case**

</td><td>

Create a customer service case for the security incident that will be tracked by the Customer Service Management \(CSM\) team. **Note:** This option is available only when Customer Service Management \(CSM\) is installed.

</td></tr><tr><td>

**Open Associated Wokflow\(s\)**

</td><td>

Open any workflow\(s\) context associated with the security incident. This option would be visible only if there are any workflows.

</td></tr><tr><td>

**Create Change Request**

</td><td>

Create a change request within the security incident.

</td></tr><tr><td>

**Create Problem**

</td><td>

Create a problem within the security incident.

</td></tr><tr><td>

**Create Outage**

</td><td>

Create an outage within the security incident.

</td></tr><tr><td>

**Calculate Severity**

</td><td>

Calculate the severity of a security incident using predefined calculators. The severity is calculated based on the predefined rules in the calculators. The severity of an incident is based on the Risk score, Business Impact, and Priority.

</td></tr><tr><td>

**Run EDR Profile**

</td><td>

Select and run the EDR Profile for the required integration. **Note:** This option is available only when any integrations are installed.

</td></tr><tr><td>

**Link to Major Security Incident**

</td><td>

Link a security incident to a major security incident.

</td></tr><tr><td>

**Report risk event**

</td><td>

Report this security incident as a risk event to the Risk Management team. The Risk Management team analyzes the event and ensure that such events and the associated losses don’t reoccur.**Note:** This option is available only when Risk Management is installed.

</td></tr><tr><td>

**Unlink from Major Security Incident**

</td><td>

Unlink from major security incident.

</td></tr><tr><td>

**Propose as Major Security Incident**

</td><td>

Propose a security incident as a major security incident.

</td></tr><tr><td>

**Promote to Major Security Incident**

</td><td>

Promote a security incident as a major security incident.

</td></tr><tr><td>

**Run Additional Action\(s\) on Endpoint**

</td><td>

Run additional actions on the endpoint.**Note:** This option is available only when Endpoint integrations are installed. For example: FireEye HX

</td></tr><tr><td>

**Create a new Event in MISP**

</td><td>

Create and modify events in MISP automatically or manually.**Note:** This option is available only when MISP integration is installed.

</td></tr><tr><td>

**Associate MITRE ATT&amp;K Technique**

</td><td>

Associate MITRE ATT&amp;K Techniques to the security incident.**Note:** This option is available when MITRE ATT&amp;K is installed.

</td></tr><tr><td>

**Show MITRE ATT&amp;K info**

</td><td>

Shows the MITRE ATT&amp;K information associated with the security incident.**Note:** This option is available when MITRE ATT&amp;K is installed.

</td></tr><tr><td>

**Add to Security Case**

</td><td>

Add the security incident to an existing or new security case.**Note:** This option is available when Threat Intel is installed.

</td></tr><tr><td>

**Switch to Classic UI**

</td><td>

Enable the analyst to switch between classic and new UI so that the analyst can also work on the existing functionalities that aren’t available on the new workspace yet.

</td></tr><tr><td>

**Cancel**

</td><td>

Cancel a security incident. After you select **Cancel** all the related records such as response tasks, child security incidents will also get canceled.

</td></tr><tr><td>

**Delete**

</td><td>

Delete a security incident record.

</td></tr></tbody>
</table>4.  Select a security incident number to view the security incident record. You can see the UI actions on the top of the page.

\[Omitted image "form-ui-actions.png"\] Alt text: Form UI actions

**Parent Topic:**[Using SIR Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/using-sir-workspace.md)

**Related topics**  


[Working with Security Incident Records]()

[Security Incident Playbook]()

[Prerequisites for the Playbooks]()

[Rebuilding existing playbooks in Workflow Studio]()

[Activity Definitions]()

[Sample Playbooks for SIR Workspace]()

[Working with MSI Records]()

[Security Incident Closure workflow]()

[Handle security incidents using Advanced Work Assignment]()

