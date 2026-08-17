---
title: Query Generation skills
description: Query Generation skills enable users to ask questions in ServiceNow Otto for Platform Analytics applications and receive answers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/enable-query-generation.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Query Generation, ServiceNow Otto for Platform Analytics, Platform Analytics]
---

# Query Generation skills

Query Generation skills enable users to ask questions in ServiceNow Otto for Platform Analytics applications and receive answers.

## Before you begin

Query Generation is included in Generative AI Controller, which is included with ServiceNow Otto applications from the ServiceNow® Store.

Role required: sn\_query\_gen.admin or higher

## About this task

Query Generation skills are not used directly. Instead, they enable other applications that call Query Generation, such as AI Data Explorer

**Important:** These generative AI skills are turned on by default. The skills will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **All** &gt; **Application Manager** and verify that the Generative AI Controller plugin is activated.

    It is likely to already be active, especially if you installed and activated a ServiceNow Otto application and plugin that has Now Assist for Platform as a dependency.

2.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills**.

3.  In the product area pane, select **Data and analytics** &gt; **Analytics**.

4.  Browse for the analytics query generation skill.

    \[Omitted image "querygen-activate-qg-skill-new.png"\] Alt text: Analytics query generation skill tile.

5.  To deactivate a skill, select **Deactivate skill**.

6.  To change the roles that can access a skill, open it for editing.

    \[Omitted image "open-skill-edit.png"\] Alt text: Opening a skill card to edit the settings.

    **Warning:** Be careful when selecting the roles that can access a skill. The default role is sn\_query\_gen.user, which the default roles for other ServiceNow Otto for Platform Analytics skills contain. Users of these other skills must be able to access Query Generation skills.


**Parent Topic:**[Configuring Query Generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/configuring-query-generation.md)

