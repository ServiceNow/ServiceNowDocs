---
title: RCA approvals in Agent Workspace for HR Case Management
description: After you install or upgrade to the latest Agent Workspace for HR Case Management from ServiceNow Store, you might encounter Restricted Caller Access \(RCA\) approval messages in the HR Agent Workspace.
locale: en-US
release: zurich
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# RCA approvals in Agent Workspace for HR Case Management

After you install or upgrade to the latest Agent Workspace for HR Case Management from ServiceNow Store, you might encounter Restricted Caller Access \(RCA\) approval messages in the HR Agent Workspace.

## Before you begin

Role required: admin

Install the Agent Workspace for HR Case Management application. The RCAs that are generated after the installation are in the Requested state and you must manually mark the RCAs as allowed, which can be time-consuming.

To automate the RCA approvals for any record, you can run the HR Agent WS bulk RCAs approval script where the source scope is the Agent Workspace for HR Case Management application. Download the HR Agent WS bulk RCAs approval file from ServiceNow Store.

Perform the following steps:

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Right-click the header and choose **Import XML**.

3.  Click **Choose file** and select the XML file that you downloaded.

4.  Search and find the HR Agent WS bulk RCAs approval script record.

5.  Click **Run Script** to approve all the requested RCAs.

    **Note:** RCA fix script can approve the RCAs which exist at the time of execution. After running the RCA script \(if you install the Document Templates from ServiceNow Store, Human Resources Scoped App: Lifecycle Events, and Human Resources Scoped App: Employee Relations plugins\), re-run the RCA script to approve the new RCAs.


