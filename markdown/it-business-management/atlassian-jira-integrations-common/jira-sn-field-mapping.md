---
title: Default mapping configuration between Agile Development 2.0 and Jira
description: Understand the default field mapping configuration for work items of a project between Jira and Agile Development 2.0.
locale: en-US
release: xanadu
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: reference
last_updated: "2024-09-06"
reading_time_minutes: 1
breadcrumb: [Discover and import Jira projects and boards, Setting up the integration between Jira and Agile Development 2.0, Atlassian Jira Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Default mapping configuration between Agile Development 2.0 and Jira

Understand the default field mapping configuration for work items of a project between Jira and Agile Development 2.0.

Mapping configuration is used to map records in Jira to Agile Development 2.0 for a project. If the table map does not exist for an issue type in your Jira project, the issue cannot be imported and exported between Jira and Agile Development 2.0.

By looking at the default mapping configuration, you can understand how issue types in Jira are mapped to task types in Agile Development 2.0. You can also see how fields are mapped between the two applications. When you import the available issues and sprints of a Jira project, this data is stored in tables as defined in the project's map configuration.

From version 1.1.1 onwards, mapping configuration is generated per project and not at the instance level. You must update any custom maps that you previously configured to ensure that the import and export of work items is not impacted.

Here's how you can view the default map configuration tables of your Jira project.

1.  Navigate to **Agile Jira Integration** &gt; **Jira Instances**.
2.  Open your Jira instance record.
3.  From the Jira Projects related list, open a Jira project.
4.  From the Table Maps related list, open the record for Story or Epic.

The following table lists the default field map configuration for a Story and Epic.

|Field in Jira|Field in Agile Development|
|-------------|--------------------------|
|Epic Name|Short Description|
|Priority|Priority|
|Summary|Description|
|Status|State|

|Field in Jira|Field in Agile Development 2.0|
|-------------|------------------------------|
|Status|State|
|Sprint|Sprint|
|Description|Description|
|Priority|Priority|
|Epic Link|Epic|
|Summary|Short Description|
|Assignee|Assigned to|

You can add or update the configuration for field, table, and choice maps of your projects between Jira and Agile Development 2.0 according to your organizational preferences. For details, see [Customizing map configuration for your Jira projects](custom-map-configuration.md).

