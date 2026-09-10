---
title: Configure the Manage contract repository agentic workflow for HAM
description: Install the ServiceNow Otto for Contract Management Pro plugin \(sn\_cm\_gen\_ai\) and activate the generative AI skills to use the Manage contract repository agentic workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/configure-contract-repo-agentic-workflow-ham.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 1
breadcrumb: [Configure, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Configure the Manage contract repository agentic workflow for HAM

Install the ServiceNow Otto for Contract Management Pro plugin \(sn\_cm\_gen\_ai\) and activate the generative AI skills to use the Manage contract repository agentic workflow.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_admin

## About this task

**Important:** Obligation Management in the Hardware Asset Workspace is available only with Hardware Asset Management Prime SKU, starting from Hardware Asset Management version 16.0.0 and Australia patch 6.

## Procedure

1.  Install the ServiceNow Otto for Contract Management Pro plugin \(sn\_cm\_gen\_ai\).

    For information about the plugin installation process, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

2.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills**.

3.  Access the **AI Skills** tab of the AI Admin Hub console.

4.  Navigate to **Employee** &gt; **CM Pro**.

5.  Select the **Activate skill** tab on the skill that you want to activate.

6.  In the skill guided setup, configure the use cases and other mappings for the Contract obligation extraction and Contract metadata extraction skills.

    -   For more information on configuring the Contract metadata extraction skill, see [Configuring contract metadata extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-conf-metadata-extraction.md). Complete the [creation of use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cmpro-na-usecase-me.md), [mapping use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cmpro-na-usecase-mappings-me.md), and [enable notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-config-notf-na-metadata.md) setup.
    -   For more information on configuring the Contract obligation extraction skill, see [Configuring contract obligation extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-conf-obligation-extraction.md).
    **Important:** When adding a new use case mapping record for these skills, clear the **Contracts created from contract request** check box.

7.  In the Define access page, select **Save and continue**.

8.  In the Review and activate page, select **Activate**.


## Result

When a warranty, maintenance, lease, or purchase contract record is created, the **Initiate contract extraction** button is displayed on the contract form.

**Related topics**  


[Hardware Asset Management integration with Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/ham-cm-pro-integration.md)

[Manage contract repository agentic workflow in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/manage-contract-repo-agent-flow-ham.md)

