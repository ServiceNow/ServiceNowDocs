---
title: Use decision tables
description: Decision tables built in Workflow Studio are executed in flows with flow logic or in scripts with API calls.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/workflow-studio/use-decision-tables.html
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using decision tables, Use, Workflow Studio, Build workflows]
---

# Use decision tables

Decision tables built in Workflow Studio are executed in flows with flow logic or in scripts with API calls.

Although decision tables are built in Workflow Studio, the actual execution of the decision takes place in other applications. Keeping decision actions separate from these applications allows the decisions to be reused and called when needed.

## Decision tables in flows

In Workflow Studio, decisions are executed as part of the **Make a decision** flow logic. For more information, see [Make a decision flow logic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/flow-logic-make-decision.md).

## Decision tables in APIs

In scripts, decision tables are executed using API calls to the decision table with the GetDecision\(\) or GetDecisions\(\) methods from the DecisionTableAPI. For more information, see [DecisionTableAPI - Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/DecisionTableAPI.md).

**Parent Topic:**[Using decision tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/using-decision-builder.md)

