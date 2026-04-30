---
title: Configure Azure DevOps story integration
description: Perform the following procedure to configure your Azure DevOps integration options.The following best practices are guidelines for creating Azure DevOps integration scripts.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-04"
reading_time_minutes: 1
breadcrumb: [User story integration, Scan Engine integrations, Scan Engine, Platform Health, Using Impact, Impact]
---

# Configure Azure DevOps story integration

Perform the following procedure to configure your Azure DevOps integration options.

## Before you begin

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\).

-   In the Azure project you want to integrate with the Scan Engine, from the project settings, find and make note of the following information:
    -   Organization name
    -   Project name
    -   Work item type
-   To connect with Azure, you will need to generate an API token:
    1.  Select **Personal access tokens** from the Azure settings menu.
    2.  Select **New Token**.
    3.  Refer to your Azure documentation for complete details.

## Procedure

1.  Navigate to `sys_auth_profile_basic.list`, and then select **New** to create a basic authentication record.

2.  Ensure that the Azure username matches the currently logged-in user’s email address.

    **Note:** Keep the email of the current logged-in user synchronized with the Azure username for seamless integration and authentication. You will also need to create a basic authentication record for each user who can create work items in Azure.

3.  Paste the token you acquired in the **Password** field.

4.  Navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties**, and then select the **User Story Integration** properties tab.

5.  Select **Azure DevOps** as the **Integration Type**.

6.  Populate the following fields with the information you acquired from your Azure DevOps project:

    -   **Organization name**
    -   **Project name**
    -   **Work Item type**
7.  Select **Update** to finalize the connection.


## Azure DevOps integration script best practices

The following best practices are guidelines for creating Azure DevOps integration scripts.

-   Unlike ServiceNow integrations, the Azure integration executes the field mapping script one time per finding. Source and Destination instances do not apply with this integration.
-   The **Organization name** and **Project name** fields determine which Azure project you will send your payload to.
-   When building a script, use data from the finding by extracting fields from the grFinding variable.
-   You can create a description and title to show in your Azure project. These will become core elements in your task. You may use other fields in the Azure project, but you will need an understanding of the Azure API to know the available fields.
-   Some general fields you can use are:

    -   /fields/System.Title
    -   /fields/System.Description
    -   /fields/Microsoft.VSTS.Common.Risk
    -   /fields/Microsoft.VSTS.Scheduling.StoryPoints
    These can be set by using this format:

    -   payload\[‘/fields/System.Title’\] = a value
    -   payload\[‘/fields/Microsoft.VSTS.Scheduling.StoryPoints’\] = a value

The following are predefined variables available for Azure DevOps Integrations:

<table id="table_s2v_nby_2hc"><tbody><tr><td>

payload

</td><td>

The field mapping to populate your Azure project.

</td></tr><tr><td>

grFinding

</td><td>

The glide record of the finding that sends the request.

</td></tr><tr><td>

workItemType

</td><td>

The work item type selected for Azure integration.

</td></tr></tbody>
</table>