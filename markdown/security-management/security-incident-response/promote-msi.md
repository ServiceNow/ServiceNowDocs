---
title: Promote to a Major Security Incident
description: Promote a security incident to a major security incident or reject promoted proposals through the Major Security Incident Management \(MSIM\) Workspace.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Propose, promote, and link incident records, Use, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Promote to a Major Security Incident

Promote a security incident to a major security incident or reject promoted proposals through the Major Security Incident Management \(MSIM\) Workspace.

## Before you begin

Role required: sn\_msi.workspace\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace** &gt; **Security Incidents** &gt; **Lists**.

2.  Select the security incident in the related category that you want to promote as major security incident.

    Review the details of the security incident in the Details section or view extended details in the incident record in a separate tab by clicking **View more details**.

3.  Select the **More Actions** icon and select **Promote to Major Security Incident**.

4.  In the Promote Major Security Incident dialog box, fill in the fields.

    1.  **Detection Date**: Date when the major security incident was first created or proposed.

    2.  **Estimated resolution date**: The estimated resolution date by when the major security incident is estimated to be resolved.

    3.  **Code name**: Select the code name for the major security incident.

        For example, Blue Tiger.

    4.  **Category**: Select the category for the major security incident.

        For example, Misconfiguration.

    5.  **Justification**: Provide the justification for proposing the incident.

    6.  **Potential impact**: Indicate the impact of the incident.

5.  Select **Propose**.

6.  Either promote the security incident or reject the promotion proposal.

    -   To promote the incident, click **Promote to Major Security Incident**.
    -   To reject the promotion proposal, click **Reject as Major Security Incident**.
7.  Select **Save**.


## Result

-   If you rejected the promotion proposal, the incident is not promoted and the incident entry moves to the Rejected tab.
-   If you promoted the incident, the incident entry moves to the Open tab and the security record displays a tag indicating that it is a major security incident.
-   The decision is listed in the Activity section of the MSIM Workspace.

Once an incident is promoted, the default configuration is applied.

-   A folder structure is created based on the folder template configuration.
-   Chat channels are created based on the channels configuration.
-   An email message is sent to the designated users. The default notification contains a link to the major security incident and details of the incident. The designated users also now have access to the collaboration resources, so the notification also includes the Microsoft Team name and a link to Microsoft SharePoint folders related to the incident.

**Parent Topic:**[Propose, promote, and link incident records](../../security-incident-response/concept/promoting-sir-to-msim.md)

**Related topics**  


[Propose as a Major Security Incident](propose-as-msi.md)

[Link to Major Security Incident](link-si-msi.md)

