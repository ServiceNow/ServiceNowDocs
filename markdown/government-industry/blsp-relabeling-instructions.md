---
title: Relabel Business Location Services portal \(BLSP\) items after upgrade
description: Using Guided Setup, you can optionally modify the "Business Location Details" page in the Business Location Services Portal to be relabeled "Agency Location Details" using Public Sector Digital Services terms during configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/government-industry/blsp-relabeling-instructions.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CSM Configurable Workspace, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Relabel Business Location Services portal \(BLSP\) items after upgrade

Using Guided Setup, you can optionally modify the "Business Location Details" page in the Business Location Services Portal to be relabeled "Agency Location Details" using Public Sector Digital Services terms during configuration.

## Before you begin

Role required: admin

## About this task

This script will relabel the "Business Location Details" page within the Business Location Services Portal to "Agency Details". References to "Business Locations" will be changed to "Agencies." The "Install Base" section of the page will be changed to "Items Received." The "Products" section will be removed; there is no equivalent use case of this in Public Sector Digital Services.

## Procedure

1.  Navigate to **All** &gt; **Constituent Service** &gt; **Administration** &gt; **Guided Setup**.

2.  Select **Get Started** to begin configuration.

    \[Omitted image "ps-gs-second-page.png"\] Alt text: Guided Setup page view to set up Government Service Portal, configure workspace, services offered, case types, foundation data, and workflow categories for Public Sector Digital Services.

    The setup page displays the different categories of configuration tasks to be completed.

3.  Select **Get Started** under the Government Service Portal category.

4.  Select **Customize the Business Location Services Portal**.

5.  Follow the steps to complete the Guided Setup task.


**Parent Topic:**[Set up the CSM Configurable Workspace for Public Sector Digital Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/setting-up-csm-fsm.md)

