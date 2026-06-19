---
title: Configure Jira user story integration
description: Configure the Jira user story integration to create work items in a Jira project directly from Scan Engine finding records.The following leading practices are guidelines for creating Jira integration scripts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/configure-jira-integration-options.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-05-05"
reading_time_minutes: 2
breadcrumb: [User story integration, Scan Engine integrations, Configure the Impact Store Application, Configuring Impact, Impact]
---

# Configure Jira user story integration

Configure the Jira user story integration to create work items in a Jira project directly from Scan Engine finding records.

## Before you begin

Gather the following from your Jira environment:

-   Jira Project Key
-   Work item type
-   Domain name: the subdomain of your Jira URL \(for example, `companyname` from `companyname.atlassian.net/jira`\)

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\)

## Procedure

1.  Generate a Jira API token
2.  Navigate to [https://id.atlassian.com/manage-profile/security/api-tokens](https://id.atlassian.com/manage-profile/security/api-tokens).

3.  Select **Create API Token**, enter a name, and copy the token.

4.  Configure the integration
5.  Navigate to `sys_auth_profile_basic.list` and select **New**.

    Create one basic auth record per user who will create Jira work items. Set **Username** to the user's Jira email address and paste the API token in **Password**.

6.  Navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties** and select the **User Story Integration** properties tab.

7.  Set **Integration Type** to `Jira` and populate the following fields: **Project key**, **Domain name**, **Work item type**.

8.  Select **Update**.


**Parent Topic:**[User story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/user-story-integration-properties.md)

## Jira integration script leading practices

The following leading practices are guidelines for creating Jira integration scripts.

### Script variables

The Jira field mapping script runs on the ServiceNow instance at the time a work item is created. Use the following variables to populate Jira fields from finding data.

|Variable|Description|
|--------|-----------|
|`payload`|The field mapping object sent to your Jira project. Set properties on this object to populate Jira fields.|
|`grFinding`|GlideRecord of the finding. Use this to read finding data for field mapping.|
|`workItemType`|The work item type selected for this integration.|
|`Key`|The Jira project key configured for this integration.|

### Leading practices

-   **Map finding fields to Jira fields via payload**

    Set properties on the `payload` object that correspond to your Jira project's field structure. Consult your Jira project configuration or the Jira REST API documentation to confirm the exact field keys expected by your project.

-   **Use grFinding to pull finding context**

    Access finding details using standard GlideRecord methods on `grFinding`. For example, use `grFinding.getValue('short_description')` to read the finding's short description and map it to a Jira summary field.

-   **Use Key and workItemType for dynamic routing**

    If your Jira environment has multiple projects or issue types, use `Key` and `workItemType` to conditionally route work items to the correct destination rather than hard-coding project keys in your script.

-   **Enable ES12 mode for modern JavaScript**

    To use modern JavaScript syntax, enable **ECMAScript 2021 \(ES12\) mode** in Scan Engine Properties before writing your mapping script.


