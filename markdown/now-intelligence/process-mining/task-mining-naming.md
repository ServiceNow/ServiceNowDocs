---
title: Task Mining project naming
description: Every time a Task Mining project is created from Process Mining, the project is named automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/task-mining-naming.html
release: brazil
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Task Mining, Integration, Activate, Process Mining, Platform Analytics]
---

# Task Mining project naming

Every time a Task Mining project is created from Process Mining, the project is named automatically.

You can create a Task Mining project from a graph node, an improvement opportunity, or the side panel. The Task Mining project name automatically includes the Process Mining project name with the name of the node or improvement opportunity you created it from. This makes it easy to identify multiple Task Mining projects apart.

The name follows this format:

`<Process Mining project name> - '<node or improvement opportunity name>'`

For example, a Task Mining project is created from a node called "Work in Progress" within a Process Mining project named "Incident Handling". The Task Mining project is named:

`Incident Handling - 'Work in Progress'`

If the node or improvement opportunity has no name, the Task Mining project uses the Process Mining project's name on its own \(no trailing dash or quotes\).

**Parent Topic:**[Integration with Task Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/integration-taskmining.md)

