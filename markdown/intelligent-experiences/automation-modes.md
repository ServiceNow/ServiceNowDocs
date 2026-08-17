---
title: Automation modes
description: Automation modes in the Information Extraction skill determine whether predictions are accepted automatically or routed to a human agent for review before a document task completes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/automation-modes.html
release: australia
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Information Extraction skill, Explore, Content Understanding, Enable AI experiences]
---

# Automation modes

Automation modes in the Information Extraction skill determine whether predictions are accepted automatically or routed to a human agent for review before a document task completes.

The Extract information from documents skill \(Information Extraction skill\) generates predictions for every field, table, and question configured in a use case, regardless of automation mode. The subsequent steps depend on whether the use case is set for full automation.

<table id="automation-mode-comparison"><thead><tr><th>

Automation mode

</th><th>

Description

</th><th>

Suitability

</th></tr></thead><tbody><tr><td>

Full automation

</td><td>

Predictions are accepted directly with no review.

 This mode eliminates the need for manual review by relying entirely on automated predictions.

 The document task is completed immediately and the integrated workflow continues.

</td><td>

Use this mode when prediction accuracy is consistently high and the risk of errors is low.

</td></tr><tr><td>

Agent review

</td><td>

The document task is forwarded to a human agent, who validates or corrects the predicted values.The task is completed, and the integrated workflow continues, only after the agent's review.

</td><td>

Use this mode when errors could lead to significant costs, or when prediction reliability has not yet been established.

</td></tr></tbody>
</table>**Related topics**  


[Predictions in Information Extraction skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictions.md)

[Turn on full automation mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/turn-on-full-automation.md)

