---
title: Activate the CI ownership agentic workflow
description: Activate the CI ownership agentic workflow from the Feature Preview Program to start automated CI ownership matching.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/activate-na-cmdb-awf-ci-ownership.html
release: brazil
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-09-28"
reading_time_minutes: 1
keywords: [activate AI Agent, CI ownership recommender, Feature Preview Program, Now Assist, CMDB, Otto]
breadcrumb: [CI ownership agentic workflow, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Activate the CI ownership agentic workflow

Activate the CI ownership agentic workflow from the Feature Preview Program to start automated CI ownership matching.

## Before you begin

The CI ownership agentic workflow must be activated from the Feature Preview Program. For more information, see [Feature Preview Program](https://www.servicenow.com/docs/r/platform-administration/feature-preview-program.html).

Role required: admin

## About this task

The CI ownership agentic workflow is inactive by default. After activation, the workflow is available for an admin or the CI ownership recommender to start. It doesn't run in the background until its scheduled jobs are also started. You can deactivate the feature at any time.

**Note:** If ServiceNow Otto for CMDB isn't installed, the **CI ownership recommender** card doesn't appear on the Feature Preview Program page.

## Procedure

1.  Navigate to **All** &gt; **Feature Preview Program**.

2.  On the Feature Preview Program page, locate the **CI ownership recommender** card.

3.  On the card, select **Activate**.

    The button changes to **Deactivate** and an **Active** badge appears on the card.


## What to do next

To start the two scheduled jobs, ask the CI ownership recommender to activate them or activate **CMDBCIOwnershipBuildGroupProfile** and **CMDBCIOwnershipInference** directly.

To deactivate the feature, select **Deactivate** on the card. The button returns to **Activate**.

**Related topics**  


[CI ownership agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-c.md)

[Determine the owner of a CI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-use.md)

