---
title: Unlink records from Major Security Incident
description: Using the Major Security Incident Management workspace, unlink the major security incident records from the Linked Records section.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/unlinking-msi-records.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Unlink records from Major Security Incident

Using the Major Security Incident Management workspace, unlink the major security incident records from the Linked Records section.

## Before you begin

Role required: sn\_msi.workspace\_manager and sn\_msi.workspace\_responder

**Note:** You can only unlink a single record at a time. After you unlink a record, the related rolled up information will be removed from the Incident Impact and Threat Intelligence sections on the workspace and the action can't be undone.

For more information on roll up records, see [Rollup Framework for MSIM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/roll-up-framework-for-major-security-incident-management.md).

## Procedure

1.  Navigate to **Major Security Incident Response** &gt; **MSIM Workspace**.

2.  Navigate to **Lists** view, which is displayed in the left pane of the workspace.

3.  Select **Accepted** to select the promoted major security incident records.

4.  Select the **Linked Records** tab.

    This section displays the linked records and its related records, which are linked to the Major Security Incident.

5.  Select the desired table view such as Security Incidents, Remediation Tasks \(vulnerable items\), or Security Case.

6.  Select the record to unlink from the list view of records.

7.  Select **Unlink Record**.

    \[Omitted image "unlink-record.png"\] Alt text: Unlink Record remediation task.

8.  A warning message is displayed asking if you want to unlink the selected record from MSI.

    \[Omitted image "unlink-record-msg.png"\] Alt text: Unlink Record warning message.

9.  Select **Unlink Record**.

    The record is unlinked and once unlinked, the changes can't be reverted. The list view of Linked Records will be refreshed after unlinking.


**Parent Topic:**[Using Major Security Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/major-security-incident-setup.md)

**Related topics**  


[Propose, promote, and link incident records]()

[Using MSI List view in the MSIM workspace]()

[View Major Security Incident impact metrics]()

[View Major Security Incident trend charts]()

[Update Major Security Incident details]()

[Link additional records to Major Security Incident]()

[Manage tasks in a Major Security Incident]()

[Track collaboration activity via MSIM workspace]()

[Create and distribute MSIM Status Reports]()

[Configure Linked Records in Major Security Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/configuring-linked-records-in-major-security-incident-management.md)

[Configure Rollup Records in Major Security Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/roll-up-record-configuration-in-major-security-incident-management.md)

