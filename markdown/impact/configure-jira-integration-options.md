---
title: Configure Jira user story integration
description: Perform the following procedure to configure your Jira integration options.The following best practices are guidelines for creating Jira integration scripts.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-04"
reading_time_minutes: 2
breadcrumb: [User story integration, Scan Engine integrations, Scan Engine, Platform Health, Using Impact, Impact]
---

# Configure Jira user story integration

Perform the following procedure to configure your Jira integration options.

## Before you begin

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\)

-   To enable the integration, you will need some details from the Jira project you want to integrate with the Scan Engine. From the project settings on your Jira board, find and make note of the following information:
    -   Project Key
    -   Work Item type
    -   Domain Name

        **Note:** You can get the domain name from your Jira URL. For example, if your URL is `companyname.atlassian.net/jira`, then your domain name is `companyname`.

-   To connect with your Jira project, you will also need an API token:
    1.  Navigate to the following URL: [https://id.atlassian.com/manage-profile/security/api-tokens](https://id.atlassian.com/manage-profile/security/api-tokens).
    2.  Select **Create API Token**, enter a name for the token, and then select **Create**.
    3.  Once the token is created, copy and store it.

        You will need it for the ServiceNow connection process.


## Procedure

1.  Navigate to `sys_auth_profile_basic.list`, and then select **New** to create a basic authentication record.

2.  Ensure that the **Name** you define starts with something easily identifiable.

3.  Ensure that the **Username** matches the currently logged-in user’s email address.

    **Note:** Always synchronize the email of the current logged-in user with the JIRA username for seamless integration and authentication. You will also need to create a basic auth record for each user who can create work items in Jira.

4.  Paste the token you acquired previously in the **Password** field.

5.  Navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties**, and then select the **User Story Integration** properties tab

6.  Select **Jira** as the **Integration Type**.

7.  Populate the following fields with the information you acquired from your Jira project:

    -   **Project key**
    -   **Domain name**
    -   **Work item type**
8.  Select **Update** to finalize the connection.


## Jira integration script best practices

The following best practices are guidelines for creating Jira integration scripts.

-   Unlike ServiceNow integrations, the Jira integration executes the field mapping script one time per finding. Source and Destination instances do not apply with this integration.
-   The **Project key** and **Domain name** fields determine which Jira project you will be sending your payload to.
-   When building a script, use data from the finding by extracting fields from the grFinding variable.
-   You can create a description and summary to show in your Jira project. These will become core elements in your work item type. You may use other fields in the Jira project, but you will need an understanding of the Jira API to know the available fields.
-   Some general fields you can use are:

    -   summary
    -   description
    -   project
    -   issuetype
    These can be set by using this format:

    ```
    payload = {
      'fields':{ 
       'summary': text to display in the title, 
       'description': a description of the work item, 
       'project': { 'key': the project key}, 
       'issuetype': { 'name': a work item type: Epic, Story, Bug, Task, Sub-Task} 
      } 
    ```


There are several predefined variables available for Azure DevOps Integrations:

<table id="table_ctq_tcy_2hc"><tbody><tr><td>

payload

</td><td>

The field mapping to populate your Jira project.

</td></tr><tr><td>

grFinding

</td><td>

The glide record of the finding that sends the request.

</td></tr><tr><td>

workItemType

</td><td>

The work item type selected for Jira integration.

</td></tr><tr><td>

Key

</td><td>

The project key created for Jira integration.

</td></tr></tbody>
</table>