---
title: Security Incident Details section
description: This section displays the security incident form fields that are rendered from the security incident classic UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/security-incident-details.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Details section

This section displays the security incident form fields that are rendered from the security incident classic UI.

The Classic UI has a view called **SIRW** View created. This view is mapped to the **Details** tab in the workspace. Any customizations that are required need to be implemented in this view.

The form fields are grouped into the following sections and displayed on the Details tab form view. Select any of the section or jump to the respective section within the form:

-   Security Incident
-   Priority
-   Source
-   Parent
-   Assignment
-   Access Controls
-   Affected Items
-   Restriction
-   Resolution

The **Details** tab contains the **Activity** stream section within the details form itself for a quick access to the security analysts to add any comments and post it. Additionally, you can also use the **Email** option, to send email about this security incident to the necessary stakeholders.

\[Omitted image "details-tab.png"\] Alt text: Malicious code activity view: Details tab.

**View the SIR Analyst Workspace view:**

1.  Navigate to **All** &gt; **Security Incident** &gt; **Show Open incidents**.
2.  Select any security incident record.
3.  Select the context menu and select **View** &gt; **sirw**.

    **Note:** You can customize using **sirw** workspace view in the classic UI form.

    \[Omitted image "sir-classic-view.png"\] Alt text: Classic UI security incident

4.  The security incident workspace view is rendered as shown below.

    \[Omitted image "classic-view-sirw.png"\] Alt text: Security incident in SIR workspace view

5.  On the Security Incident record, right click and go to **Configure** &gt; **Form Layout**.
6.  Drill down to the **Form view and section** and select **New** from **Section** to create a new section.
7.  Provide the new section name and select **OK**.

    For example, Incident form.

8.  The new section is created and added to the **Section**.
9.  Select your new section and add the required section fields to the slush bucket and select **Save**.
10. The newly added section is displayed along with the existing section layout within the security incident form.
11. Select **Switch to SIR workspace** to jump to the security incident form and the customized section within the **Details** tab of the workspace.

-   **[Security incident Details tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/security-incident-details-form.md)**  
This section describes all the fields of the **Details** tab of a security incident.

**Parent Topic:**[Working with Security Incident Records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/using-analyst-workspace.md)

**Related topics**  


[Security Incident Overview section]()

[SIR Workspace Orchestration]()

[Security Incident Response Tasks]()

[Security Incident Response Other Records]()

[Security Incident Response Post Incident Review]()

[Update information in security incident related records]()

[TISC integration within SIR Workspace]()

[Reports in Security Incident Response]()

[Collaborate using conference call or chat in Security Incident Response]()

[Viewing incident details with a relationship graph]()

[MITRE attack and defend technique graph]()

[View and filter the incident timeline]()

