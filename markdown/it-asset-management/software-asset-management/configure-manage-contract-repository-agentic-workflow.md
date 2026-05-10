---
title: Configure the manage contract repository agentic workflow for Software Asset Management
description: Install the Now Assist in Contract Management plugin \(sn\_cm\_gen\_ai\) and activate the generative AI skills to use the manage contract repository agentic workflow.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use manage contract repository agentic workflow, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Configure the manage contract repository agentic workflow for Software Asset Management

Install the Now Assist in Contract Management plugin \(sn\_cm\_gen\_ai\) and activate the generative AI skills to use the manage contract repository agentic workflow.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_admin

## Procedure

1.  Install the Now Assist in Contract Management plugin \(sn\_cm\_gen\_ai\).

    For information about the plugin installation process, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

3.  Access the **Now Assist Skills** tab of the Now Assist Admin console.

4.  Navigate to **Employee** &gt; **CM Pro**.

5.  Select the **Activate skill** on the skill that you want to activate.

    ![Now Assist skills available for Contract Management Pro](../image/sam-cmpro-now-assist-skills-activate.png "Now Assist skills for Contract Management Pro")

6.  In the skill guided setup, configure the use cases and other mappings for the Contract obligation extraction and Contract metadata extraction skills.

    For more information on configuring contract metadata extraction skill, see [Configuring contract metadata extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-conf-metadata-extraction.md).

    **Note:** For the Contract metadata extraction skill, complete the [creation of use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-na-usecase-me.md), [mapping use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-na-usecase-mappings-me.md), and [enable notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-config-notf-na-metadata.md) setup.

    For more information on configuring Contract obligation extraction skill, see [Configuring contract obligation extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-conf-obligation-extraction.md).

    **Note:** On the use case mapping page, the **Contracts created from contract request** check box is visible only if the Contracts core \(sn\_cm\_core\) plugin is installed. If you have the Contracts core \(sn\_cm\_core\) plugin installed, it means you're already availing the contract pre-signature capabilities. You must clear the **Contracts created from contract request** check box.

    If the Contracts core \(sn\_cm\_core\) plugin is not installed, this check box will not be displayed.

7.  In the Define access page, select **Save and continue**.

8.  In the Review and activate page, select **Activate**.


## Result

When a software contract record is created, the **Initiate contract extraction** button is displayed on the contract form.

## What to do next

[Initiate metadata and obligation extraction from a signed contract in the Software Asset Workspace](extract-metadata-from-uploaded-contract-document.md)

**Parent Topic:**[Use manage contract repository agentic workflow in the Software Asset Workspace](../concept/manage-contract-repository-workflow.md)

