---
title: Configure Azure DevOps story integration
description: Perform the following procedure to configure your Azure DevOps integration options.Script variables, field paths, and leading practices for writing field mapping scripts in the Azure DevOps story integration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/configure-azure-devops-integration-options.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [User story integration, Scan Engine integrations, Configure the Impact Store Application, Configuring Impact, Impact]
---

# Configure Azure DevOps story integration

Perform the following procedure to configure your Azure DevOps integration options.

## Before you begin

-   Before you begin, gather the following from your Azure DevOps environment:

    -   Organization name
    -   Project name
    -   Work item type

Role required: Scan Engine admin \(sn\_se.scan\_engine\_admin\).

## Procedure

1.  Generate an Azure DevOps API token
2.  In Azure DevOps, select **Personal access tokens** from the user settings menu.

3.  Select **New Token** and follow the Azure DevOps documentation to configure and generate the token.

4.  Configure the integration
5.  Navigate to `sys_auth_profile_basic.list` and select **New**.

    Create one basic auth record per user who will create Azure DevOps work items. Set **Username** to the user's email address and paste the API token in **Password**.

6.  Navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties** and select the **User Story Integration** properties tab.

7.  Set **Integration Type** to `Azure DevOps` and populate the following fields: **Organization name**, **Project name**, **Work item type**.

8.  Select **Update**.


## What to do next

See [Azure DevOps integration script leading practices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-azure-devops-integration-options.md) for available script variables, common field paths, and guidance on writing field mapping scripts for Azure DevOps.

**Parent Topic:**[User story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/user-story-integration-properties.md)

## Azure DevOps integration script leading practices

Script variables, field paths, and leading practices for writing field mapping scripts in the Azure DevOps story integration.

### Script variables

The Azure DevOps field mapping script runs on the ServiceNow instance at the time a work item is created. Set field values on the `payload` object using the Azure DevOps field path format: `payload['/fields/System.Title'] = value`.

|Variable|Description|
|--------|-----------|
|`payload`|The field mapping object sent to your Azure DevOps project. Set field path keys on this object to populate work item fields.|
|`grFinding`|GlideRecord of the finding. Use this to read finding data for field mapping.|
|`workItemType`|The work item type selected for this integration.|

### Common Azure DevOps field paths

|Field path|Maps to|
|----------|-------|
|`/fields/System.Title`|Work item title|
|`/fields/System.Description`|Work item description|
|`/fields/Microsoft.VSTS.Common.Risk`|Risk level|
|`/fields/Microsoft.VSTS.Scheduling.StoryPoints`|Story points|

### Leading practices

-   **Use field path syntax for all payload assignments**

    Azure DevOps requires field values to be set using the JSON Patch path format. Always use bracket notation: `payload['/fields/System.Title'] = grFinding.getValue('short_description')`. Do not use dot notation or plain property names.

-   **Verify field paths against your process template**

    The available field paths depend on your Azure DevOps process template \(Agile, Scrum, or CMMI\). Confirm that the field paths you use exist in your project's work item type before deploying your mapping script.

-   **Use grFinding to pull finding context**

    Access finding details using standard GlideRecord methods on `grFinding`. For example, `grFinding.getValue('short_description')` maps cleanly to `/fields/System.Title`.

-   **Enable ES12 mode for modern JavaScript**

    To use modern JavaScript syntax, enable **ECMAScript 2021 \(ES12\) mode** in Scan Engine Properties before writing your mapping script.


