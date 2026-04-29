---
title: Breakdown Management
description: Breakdown Analysis helps industrial teams investigate and resolve serious equipment failures and process stops. You can either escalate an unresolved deviation or create a breakdown record directly, depending on how the issue is identified. This structured workflow helps timely issue resolution and long-term reliability improvements.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Industrial Workflows, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Breakdown Management

Breakdown Analysis helps industrial teams investigate and resolve serious equipment failures and process stops. You can either escalate an unresolved deviation or create a breakdown record directly, depending on how the issue is identified. This structured workflow helps timely issue resolution and long-term reliability improvements.

## Breakdown and Breakdown Analysis overview

Breakdowns are events that are more serious than regular deviations. They cause longer downtime, higher costs, and a greater impact on production.

Every breakdown is a deviation, but not every deviation is a breakdown.

Factors that help determine the severity include:

-   Value of replacement parts
-   Effort required to fix the issue
-   Lost production time or opportunity

Breakdowns Analysis is a structured process used to investigate:

-   Breakdowns: Machine stops that require major repairs or part replacements
-   Process failures: Machine stops that last longer than a set time, where the default is 15 minutes

## Methods for logging breakdown events

Escalating a deviation

When a deviation remains unresolved or its impact increases, you can escalate it to Breakdown Analysis. This method keeps all original data, such as timestamp, asset ID, and operator notes. It avoids duplicate data entry, links to deviation and breakdown records for traceability, and optionally closes the deviation when the breakdown is resolved.

Creating a breakdown record directly

Sometimes breakdowns are identified outside the deviation workflow, for example through alerts, manual observation, or scheduled reviews. In such cases, you can create a Breakdown Analysis record directly to log the event immediately. Capture details such as duration, symptoms, and impact, classify the issue and assess its cost, as well as trigger deeper analysis if needed.

## Users

Breakdown analysis is used mostly by:

<table id="table_lwf_5gv_bhc"><thead><tr><th>

Users

</th><th>

Responsibilities

</th></tr></thead><tbody><tr><td>

Line operator

</td><td>

-   Logs deviations or breakdowns
-   Minimizes downtime
-   Provides context for escalation

</td></tr><tr><td>

Shift lead

</td><td>

-   Monitors issues
-   Escalates deviations or logs breakdowns
-   Coordinates investigations

</td></tr><tr><td>

Maintenance engineer

</td><td>

-   Investigate root causes
-   Records fixes and preventive actions
-   Close Breakdown analysis records after resolution

</td></tr><tr><td>

Equipment owner

</td><td>

-   Oversees equipment performance
-   Makes sure that breakdowns are logged and analyzed

</td></tr></tbody>
</table>## Example scenario

A machine stops during production. The operator logs a deviation. After two hours, the shift lead escalates it to Breakdown Analysis. The system creates a linked record with all relevant data. The maintenance engineer investigates, replaces a faulty part, and closes the breakdown. The deviation is also marked as resolved. In another situation, a breakdown is identified directly through a system alert. The operator logs it manually, records the impact, and assigns it for investigation. The team performs a breakdown analysis and updates the record with corrective actions.

-   **[Create a breakdown](../task/create-breakdown.md)**  
Create a breakdown record in the Digital Factory Workspace to document a significant equipment failure or process stop. Use this task to capture key details such as duration, impact, and cause, and begin structured investigation and resolution.
-   **[Escalate a deviation to a breakdown](../task/escalate-deviation-to-breakdown.md)**  
Convert a deviation into a breakdown when it no longer fits the deviation criteria and requires structured analysis.
-   **[Initiate a breakdown analysis](../task/initiate-breakdown-analysis.md)**  
Start a breakdown analysis to investigate the root cause of a recurring or complex issue.

**Parent Topic:**[Industrial Workflows](industrial-workflows.md)

