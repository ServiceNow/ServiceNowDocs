---
title: Analyze your hardware assets by using Now Assist for HAM
description: View consolidated asset data and identify key action items with the comprehensive AI-generated analysis summary.
locale: en-US
release: zurich
product: Now Assist for Hardware Asset Management
classification: now-assist-for-hardware-asset-management
topic_type: task
last_updated: "2026-02-03"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use generative AI skills, Now Assist for Hardware Asset Management \(HAM\), Hardware Asset Management, IT Asset Management]
---

# Analyze your hardware assets by using Now Assist for HAM

View consolidated asset data and identify key action items with the comprehensive AI-generated analysis summary.

## Before you begin

Summaries are available only for assets within the Hardware and Asset classes and that are licensed and associated with an opted-in resource category.

**Important:** This feature doesn't support pallets, consumables, bundles, and assets that are opted out of HAM workflows.

Role required: asset

## About this task

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

The Generate hardware asset insights generative AI skill generates comprehensive asset analysis summaries by aggregating data from related records. These summaries provide insights into the asset lifecycle, chain of custody, audit status, and financial metrics to support key asset management activities. The level of detail in the summary depends on the amount of data available for that specific asset. The summary dynamically updates based on asset state and includes context from any active incidents, change requests, or tasks. To maintain data integrity and streamline workflows, the skill highlights missing information and lists specific action items.

**Note:** You can view incident and change request details in the summary only if the asset role is provisioned with read access to the Incident \[incident\] and Change Request \[change\_request\] tables.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace**.

2.  Select the **Hardware assets** tab.

3.  Select the asset record that you want to analyze.

4.  Select **Summarize**.

    An asset analysis summary card with a consolidated overview of critical asset data and potential actions is displayed.

    ![Asset analysis summary with comprehensive asset information and list of action items](../image/now-assist-ham-asset-summary.png "Asset analysis summary")


