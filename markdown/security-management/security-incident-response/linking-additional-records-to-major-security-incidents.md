---
title: Link additional records to Major Security Incident
description: In the workspace, use the linking records functionality to link any related Security Incident records and its child security incidents, Remediation Tasks from Vulnerability Response, and Security Cases from Threat Intelligence to a Major Security Incident \(MSI\) record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/linking-additional-records-to-major-security-incidents.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Link additional records to Major Security Incident

In the workspace, use the linking records functionality to link any related Security Incident records and its child security incidents, Remediation Tasks from Vulnerability Response, and Security Cases from Threat Intelligence to a Major Security Incident \(MSI\) record.

## Before you begin

Role required: sn\_msi.workspace\_manager and sn\_msi.workspace\_responder

## Procedure

1.  Navigate to **Major Security Incident Response** &gt; **MSIM Workspace**.

2.  Navigate to the **Lists** view, which is displayed in the left pane of the workspace.

3.  Click **Accepted** to select the promoted major security incident records.

4.  Select the incident record that is required to be linked which is not in the Closed state from the list of promoted records.

5.  Click **Linked Records** tab.

    A drop-down list is provided to select other linked record tables.

    The Linked Records section displays the linked records and its related records, which were linked to the Major Security Incident.

6.  Select the desired table view such as Security Incidents, Remediation Tasks \(vulnerable items\), or Security Case from the list.

    Based on your selection type records table view, the linked records that linked to the major security incident records are displayed.

7.  Link a record that is not linked to any MSI record and is in the **Open** state by selecting the record and clicking **Link Record** in the top right of the page.

    **Note:** You can't link an incident record to an MSI record if it's in the **Closed** state.

8.  Select the record to be linked and click **Link**.

    A confirmation message displays that the record is linked successfully and the rollup of related records will be processed in the background.

    **Note:** After a record is linked, the list view is refreshed automatically and lists the updated list of incident records.


**Parent Topic:**[Using Major Security Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/major-security-incident-setup.md)

**Related topics**  


[Propose, promote, and link incident records]()

[Using MSI List view in the MSIM workspace]()

[View Major Security Incident impact metrics]()

[View Major Security Incident trend charts]()

[Update Major Security Incident details]()

[Unlink records from Major Security Incident]()

[Manage tasks in a Major Security Incident]()

[Track collaboration activity via MSIM workspace]()

[Create and distribute MSIM Status Reports]()

[Unlink records from Major Security Incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/unlinking-msi-records.md)

