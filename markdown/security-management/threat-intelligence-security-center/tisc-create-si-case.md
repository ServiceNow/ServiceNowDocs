---
title: Create a security incident from a TISC case
description: Create security incidents and associate observables to the security incidents from a TISC case.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Create a security incident from a TISC case

Create security incidents and associate observables to the security incidents from a TISC case.

## Before you begin

Role required: sn\_si\_basic

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click **Threat Analyst Workbench** icon.

3.  Go to **Case Management** &gt; **All Cases**.

    All the cases are displayed.

4.  Open any case.

5.  Click **Create Security Incident** button.

    **Note:** On the **Case Management Workbench** the **Create Security Incident** button is enabled only for the open case records and disabled for the closed case records.

    The Create Security Incident dialog box is displayed.

6.  Fill the form with appropriate incident details:

    |Field|Description|
    |-----|-----------|
    |Short description|Enter a short description of the security incident.|
    |Description|Enter a description of the security incident.|
    |Category|Defines the classification of the security incident.|
    |Priority|Defines the priority of the security incident.|
    |Subcategory|Defines the sub classification of the security incident based on its category.|
    |Assignment group|Specifies the assignment group to which the security incident should be assigned.|
    |Parent|Indicates the parent security incident, which is a TISC case from which this action is triggered.|

7.  Click **Next** to continue.

    **Note:** You must enter all the mandatory fields, the **Next** button will remain disabled until you enter all the required fields.

8.  Select the observables associated with the TISC case to link them to a security incident, and then click **Next** to proceed

9.  Review the security incident details and observable that will be associated with the newly created security incident then click **Create** to continue and create the security incident.

    **Note:** A confirmation message is displayed indicating that the security incident is created, with a link to the security incident, clicking the link will direct you to the security incident in the Security Incident Response Workspace.

    After the security incident is created, you will be redirected to the TISC **Artifacts** tab of the case.

10. Go to **Security Incidents** section under the TISC **Artifacts** tab to view the incidents.

    **Note:** A work notes is also posted on the TISC case activity stream indicating that the security incident \(security incident number\) is created with the associated with TISC observables. This work notes includes the details such as the observable type and observable value.

    On the Security Incident Response Workspace, security incident form:

    -   A work notes is posted on the activity stream indicating that the security incident was successfully created from TISC case. This work notes also includes a link to the TISC case confirming that the selected observables have been associated with the security incident.
    -   In addition, you can also verify this by accessing the **Related Records** tab of the Security Incident Response Workspace and reviewing the observables entries under **Threat Intel** &gt; **Associated Observables**. From there, you can also view the associated observables under the **TISC Context** section. You may notice that the these observables have been directly associated from TISC.

**Parent Topic:**[Threat Analyst Workbench](../concept/threat-analyst-workbench.md)

**Related topics**  


[Workbench Overview](../concept/workbench-overview.md)

[Creating cases using Threat Analyst Workbench](../concept/create-cases-using-threat-analyst-workbench.md)

[Creating case task using Threat Analyst Workbench](tisc-create-case-task.md)

[Working with Investigation Canvas](../concept/tisc-investigation-canvases.md)

[Add artifacts to case\(s\) or case task\(s\)](add-artifacts-to-a-case-s.md)

[Run Enrichment Actions within a case](run-enrichment-results.md)

[View Case Reports](view-case-reports.md)

[Upload Secure File Attachments](secure-file-attachments.md)

