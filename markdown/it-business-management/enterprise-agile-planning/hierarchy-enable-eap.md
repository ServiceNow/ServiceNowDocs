---
title: Enable Hierarchy tab in EAP
description: Run a fix script to enable the Hierarchy tab in the Enterprise Agile Planning \(EAP\) workspace.
locale: en-US
release: zurich
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-02-26"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Enable Hierarchy tab in EAP

Run a fix script to enable the Hierarchy tab in the Enterprise Agile Planning \(EAP\) workspace.

## Before you begin

Ensure that **Application Scope** of your ServiceNow instance is set to **Strategic Planning**.

Role required: sn\_apw\_advanced.eap\_admin

## About this task

By default, the Hierarchy tab is not enabled for use in the EAP workspace.

Running the fix script **Populate parent level data for work item** creates a system property**sn\_apw\_advanced.enable\_hierarchy\_view** the value of the property is set to **true**. This action activates the Hierarchy tab and makes it available to all team members alongside the Backlog and Planning board tabs in the workspace.

## Procedure

1.  Navigate to **System Definition** &gt; **Fix Scripts**.

2.  Search for **Populate parent level data for work item** and open the record.

3.  Select **Run Fix Script**.

4.  From the Run Fix Script window, select **Proceed**.

    The fix script creates the sn\_apw\_advanced.enable\_hierarchy\_view if it's not already present in your instance and sets its value to **true**.


## What to do next

Verify that the value of the **sn\_apw\_advanced.enable\_hierarchy\_view** property is set to true.

1.  Navigate to **sys\_properties.list**
2.  Search for **sn\_apw\_advanced.enable\_hierarchy\_view** and open the record.
3.  Verify if the Value field is set to **true**.

**Related topics**  


[Work item hierarchy for EAP teams](../concept/eap-hierarchy-tab.md)

[Modify display limit in Hierarchy tab of EAP](hierarchy-display-limit-eap.md)

