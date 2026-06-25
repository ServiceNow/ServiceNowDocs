---
title: Analyze hardware assets using the Generate hardware asset insights generative AI skill
description: View consolidated asset data and identify key action items with the comprehensive AI-generated analysis summary.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/generate-asset-analysis-now-assist-ham.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-02-03"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Hardware Asset Management, IT Asset Management]
---

# Analyze hardware assets using the Generate hardware asset insights generative AI skill

View consolidated asset data and identify key action items with the comprehensive AI-generated analysis summary.

## Before you begin

Summaries are available only for assets within the Hardware and Asset classes and that are licensed and associated with an opted-in resource category.

**Important:** This feature doesn't support pallets, consumables, bundles, and assets that are opted out of HAM workflows.

Role required: asset

## About this task

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

The Generate hardware asset insights generative AI skill generates comprehensive asset analysis summaries by aggregating data from related records. These summaries provide insights into the asset lifecycle, chain of custody, audit status, and financial metrics to support key asset management activities. The level of detail in the summary depends on the amount of data available for that specific asset. The summary dynamically updates based on asset state and includes context from any active incidents, change requests, or tasks. To maintain data integrity and streamline workflows, the skill highlights missing information and lists specific action items.

**Note:** You can view incident and change request details in the summary only if the asset role is provisioned with read access to the Incident \[incident\] and Change Request \[change\_request\] tables.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace**.

2.  Select the **Hardware assets** tab.

3.  Select the asset record that you want to analyze.

4.  Select **Summarize**.

    An asset analysis summary card with a consolidated overview of critical asset data and potential actions is displayed.

    \[Omitted image "now-assist-ham-asset-summary.png"\] Alt text: Asset analysis summary with comprehensive asset information and list of action items


**Parent Topic:**[Using Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/using-ham-classic.md)

**Related topics**  


[Work with hardware normalization]()

[Manage asset bundles from your inventory]()

[Manage your inventory through pallet assets]()

[Manage loaner assets]()

[Donate assets to charity organizations]()

[Use Advanced Shipment Notification]()

[Manage RMA requests]()

[Create an inventory stock order request]()

[Create a disposal order]()

[Fulfilling hardware asset requests]()

[Audit hardware asset inventory]()

[Request a Hardware Asset Refresh]()

[Manage your expiring contracts for leased hardware assets]()

[Reclaim hardware assets]()

[View RFID information of assets]()

[Manage the lifecycle of hardware models with calculated lifecycle templates]()

[Create an internal lifecycle in the Hardware Asset Workspace]()

[Receive asset warranty details from Lenovo]()

[Manage stockrooms]()

[Track shipments using the integration framework]()

[Track asset location using indoor maps]()

[Assess performance of Hardware Asset Management]()

[Manage refresh of assets using Zero Touch Refresh]()

[Configure the Total Cost of Ownership of assets]()

[Manage Hardware Asset Management subscriptions]()

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace]()

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows]()

[Manage hardware asset tasks using the Mobile Agent application]()

[Manage asset put away using the Hardware Asset Workspace]()

[Audit your hardware assets by using Asset Attestation]()

[Acknowledge receipt of assets on the Employee Center portal]()

[Update associated Decision tables for HAM flows]()

