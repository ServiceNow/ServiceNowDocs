---
title: Task Mining agent
description: The Task Mining agent is a service installed on a user's workstation that captures workstation logs for active windows only. Task Mining agent user-initiated recording supports mouse actions, hotkeys, and authentication integrations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/now-intelligence/task-mining/task-mining-agent-features-and-workarounds.html
release: yokohama
product: Task Mining
classification: task-mining
topic_type: reference
last_updated: "2026-06-18"
reading_time_minutes: 1
breadcrumb: [Reference, Task Mining, Platform Analytics]
---

# Task Mining agent

The Task Mining agent is a service installed on a user's workstation that captures workstation logs for active windows only. Task Mining agent user-initiated recording supports mouse actions, hotkeys, and authentication integrations.

Certain user interactions aren't captured automatically.

**For workstation users:** Use mouse clicks and keyboard shortcuts instead of drag-and-drop or trackpad scrolling so that all interactions are accurately recorded.

**For Task Mining analysts:** Expect agent UI events in your Task Mining data. Plan for manual filtering or post-processing steps to exclude them. You can also use workarounds to capture equivalent data for processes affected by these limitations.

## Unsupported features and workarounds

This table describes these limitations and provides practical workarounds.

|Limitation|Workaround|
|----------|----------|
|Drag-and-drop interactions aren't captured|Document the sequence of individual clicks and keyboard modifiers that achieve the same result|
|Tab navigation accuracy is limited on some browser-based applications|Document navigation using mouse clicks instead of keyboard tab sequences|
|Task Mining agent UI events can't be automatically excluded from recordings|Filter agent events manually during analysis or apply filters during post-processing|
|Duplicate actions aren't automatically removed|Review recordings and filter duplicate actions manually|
|Trackpad gesture-based scrolling is not detected|Use a traditional scroll wheel or keyboard navigation instead|

**Parent Topic:**[Task Mining Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/task-mining/reference-task-mining.md)

**Related topics**  


[Install the Task Mining agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/task-mining/install-agent.md)

[Define user actions for task logging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/task-mining/mine-data.md)

[Identify task improvement actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/task-mining/identify-improvement-opportunities.md)

