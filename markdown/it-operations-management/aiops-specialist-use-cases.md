---
title: AIOps AI Specialist use cases
description: Three scenarios show how teams typically use the AIOps AI Specialist to reduce noise, speed up investigations, and turn runbooks into fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/aiops-specialist-use-cases.html
release: australia
topic_type: concept
last_updated: "2026-11-01"
reading_time_minutes: 4
keywords: [AIOps AI Specialist, use cases, noise reduction, root cause analysis, remediation suggestions]
breadcrumb: [AIOps AI Specialist, ITOM AIOps specialists, AI in ITOM AIOps, ITOM AIOps, IT Operations Management]
---

# AIOps AI Specialist use cases

Three scenarios show how teams typically use the AIOps AI Specialist to reduce noise, speed up investigations, and turn runbooks into fixes.

These three scenarios show how teams typically put the AI Specialist to work. Each scenario follows the same pattern: the challenge, the solution, and the outcome you can measure. Some examples are provided for illustration only.

## Protect the queue from noise

Many network operations centers \(NOCs\) spend the first hour of each shift on alerts that they have seen many times. The AI Specialist closes the repetitive alerts, so operators start with the alerts that need judgment.

-   **The challenge**

    A retail company runs a NOC across three shifts. Nightly batch jobs push CPU and queue alerts over their thresholds, and the same alerts return every evening. This caused the following problems:

    -   Operators opened and closed known alerts before they reached real problems.

    -   Real alerts waited behind the noise.

    -   Alerts that belong to no assignment group went unseen.


-   **The solution**

    The team scoped the AI Specialist to the infrastructure alerts that repeat most. It turned on noise reduction and covered unowned alerts.

    |Solution|Description|Outcome|
    |--------|-----------|-------|
    |Scoped triage|Conditions limit the AI Specialist to the monitoring source and severity levels behind the repeat alerts.|The AI Specialist works the alert types that it handles best.|
    |Noise reduction|The AI Specialist closes alerts that history shows resolve without action, and logs each closure.|Repeat alerts leave the queue before an operator opens them.|
    |Unassigned coverage|Handle unassigned alerts gives ownerless alerts an owner.|No alert sits unseen.|
    |Supervised review|Supervisors review closed alerts each morning and reopen any mistakes.|Deflection stays reliable and improves over time.|

    Modules used: Scoping on, Noise reduction on, Investigation on, Remediation off. Measure it with: the Auto-closed tile, and workload status for unassigned alerts.


-   **Result measurement**

    Measure the results with the number of auto-closed alerts and the workload status for unassigned alerts.


## Resolve a critical alert faster

When a critical alert fires on a customer-facing service, the slowest step is often working out what changed and who is affected. The AI Specialist completes that work before the operator starts the investigation.

-   **The challenge**

    A bank's payments database raises a critical alert about exhausted connections. The on-call operator must find which services depend on the database, whether a recent change caused the problem, what the monitoring tools show, and which runbook applies. Without the AI Specialist, this work involves the following:

    -   Switching between monitoring tools, change records, the CMDB, and knowledge articles.

    -   Waiting for colleagues to provide context.

    -   A longer time to resolve, while the service is degraded.


-   **The solution**

    The team turned on investigation with observability agents connected. It selected the operations runbooks as knowledge sources.

    |Solution|Description|Outcome|
    |--------|-----------|-------|
    |Root cause analysis|The AI Specialist links related alerts and a recent change to the database, and names a probable cause with evidence.|The operator starts from a hypothesis.|
    |Impact analysis|The AI Specialist lists the affected service instances, service offerings, and technical business services.|Priority reflects actual service impact.|
    |Observability analysis|The AI Specialist retrieves telemetry and topology from the connected monitoring tool for the alert source.|Findings include data that the operator did not have to collect.|
    |Knowledge lookup|The AI Specialist reads the selected runbooks and cites them.|Recommended steps match your own procedures.|
    |Insight summary|The overview, probable cause, impact, and next steps appear on the Insights tab.|The operator decides within minutes.|

    Modules used: Investigation on with all settings, Noise reduction off, Remediation off.


-   **Result measurement**

    Measure the results by comparing Alert MTTR using AI with Alert MTTR without AI.


## Turn runbooks into one-click fixes

Most teams already have runbooks and some automation. The AI Specialist connects them to the alert, so the right fix is available with one action. An operator still makes the decision.

-   **The challenge**

    A logistics provider has knowledge articles for its most common incidents, such as clearing a full disk or restarting a stuck service. Several of these articles have automation behind them. Without the AI Specialist, operators must do the following:

    -   Search for the right article each time.

    -   Run the steps differently on different shifts.

    -   Hesitate to run automation that they cannot inspect first.


-   **The solution**

    The team linked its automation to knowledge articles as alert management rules. It enabled suggested remediation after the investigation phase proved reliable.

    |Solution|Description|Outcome|
    |--------|-----------|-------|
    |Knowledge-linked automation|Articles with automation enabled as alert management rules become candidate fixes.|Existing runbooks are reused, not rebuilt.|
    |Ranked suggestions|The AI Specialist searches the articles and recommends the best action for the alert. It learns which actions worked on similar alerts.|The right fix appears on the alert.|
    |Human activation|An operator reviews the action and activates it. The AI Specialist never runs it.|Operators keep control, and every change is attributable.|
    |Phased rollout|Remediation is enabled last, after investigation and noise reduction are proven reliable.|Autonomy grows as confidence grows.|

    Modules used: Investigation on, Remediation on, and Noise reduction on once validated.


-   **Result measurement**

    Measure the results with the time saved by automation and the hours recovered.


**Parent Topic:**[AIOps AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/ai-specialist-aiops-overview.md)

