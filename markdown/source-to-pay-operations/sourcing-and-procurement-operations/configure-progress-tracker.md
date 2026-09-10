---
title: Configure the Progress Tracker
description: Procurement administrators can control whether the Progress Tracker displays on purchase requisition \(PR\) and purchase order \(PO\) records systemwide. You can customize which states appear in the stepper and control the order in which states are displayed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/configure-progress-tracker.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-08-19"
reading_time_minutes: 3
breadcrumb: [Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure the Progress Tracker

Procurement administrators can control whether the Progress Tracker displays on purchase requisition \(PR\) and purchase order \(PO\) records systemwide. You can customize which states appear in the stepper and control the order in which states are displayed.

## Prerequisites

You must have the sn\_shop.procurement\_administrator role to read or modify both the Progress Tracker configuration records and the system properties that control visibility.

## Control levels

By default, the Progress Tracker is enabled and displays all available states on every purchase requisition and purchase order. As a procurement administrator, you have two levels of control.

-   **Systemwide visibility**

    Enable or disable whether the Progress Tracker appears on all PR or PO records using system properties. This is useful when you are performing maintenance or need to hide the tracker temporarily.

-   **State-level customization**

    Customize which states appear in the stepper and their display order using the Progress Tracker configuration records. You can hide states your organization does not use and arrange states in a sequence that matches your workflow.


## Required role

You must have the sn\_shop.procurement\_administrator role to set up and maintain the Progress Tracker to align with your organization's PR and PO workflows.

## Related tasks

For more information, see the following topics.

-   [Configure PR and PO Progress Tracker states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/configure-pr-po-states.md)
-   [Configure Progress Tracker visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/configure-tracker-visibility.md)

-   **[Configure PR and PO Progress Tracker states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/configure-pr-po-states.md)**  
Configure which states appear in the Progress Tracker, and how they flow, by editing the PR Stage Display Config and PO Stage Display Config records—no code deployment required.
-   **[Configure Progress Tracker visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/configure-tracker-visibility.md)**  
Enable or disable whether the Progress Tracker displays on purchase requisition and purchase order records system-wide.

**Parent Topic:**[Using Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/using-spo.md)

**Related topics**  


[Using Shopping Hub]()

[Using Shopping Hub Mobile]()

[Using Procurement Case Management]()

[Working with SPO playbooks in the Source-to-Pay Workspace]()

[Using Spend and Savings Management]()

[Using Sourcing Pipeline Management]()

[Create a Universal Request]()

[Purchase requisition and purchase order progress tracking]()

