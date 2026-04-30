---
title: Verify Application Restricted Caller Access \(RCA\) Privileges
description: Verify that there are no duplicate entries in the Restricted Caller Access \(RCA\) records before uploading an RCA data set to fix the configuration issues.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-02-01"
reading_time_minutes: 1
breadcrumb: [Install HR Service Delivery, Plan your installation, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Verify Application Restricted Caller Access \(RCA\) Privileges

Verify that there are no duplicate entries in the Restricted Caller Access \(RCA\) records before uploading an RCA data set to fix the configuration issues.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Application Restricted Caller Access Privileges**.

2.  In the **Source Scope** search, enter: `ServiceNow for Microsoft Teams`.

3.  Right-click on **Source Scope** column header, and select **Group By Source Scope**.

4.  Expand **ServiceNow for Microsoft Teams**, and **Collaboration Services** source scopes.

5.  Delete all the entries under **ServiceNow for Microsoft Teams**, and **Collaboration Services** source scopes.


**Parent Topic:**[Install HR Service Delivery integration with Microsoft Teams application](install-hr-ms-teams-plugin.md)

