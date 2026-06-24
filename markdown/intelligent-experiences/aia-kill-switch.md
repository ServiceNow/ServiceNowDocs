---
title: Kill Switch in Now Assist AI Agents
description: The kill switch feature detects and stops runaway AI agent triggers that execute repeatedly against the same records, preventing unnecessary consumption of Now Assist interactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aia-kill-switch.html
release: zurich
topic_type: concept
last_updated: "2026-06-04"
reading_time_minutes: 3
keywords: [Kill Switch]
breadcrumb: [Add a trigger, Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Kill Switch in Now Assist AI Agents

The kill switch feature detects and stops runaway AI agent triggers that execute repeatedly against the same records, preventing unnecessary consumption of Now Assist interactions.

## Kill Switch Overview

An AI agent trigger can match the same record multiple times within a short period during executions. When left unchecked, a misconfiguration trigger condition can process the same incident five or more times per day, across dozens of records, for several consecutive days. Each trigger activation spawns a conversation and consumes assists, resulting in charges for activity that provides no customer value.

The kill switch feature detects when the same record is triggering the same agent objective beyond a threshold in a single day and automatically disables the agent. It monitors trigger activity, issues tiered alert notifications to trigger and agent owners, and optionally disables the trigger automatically after a configurable breach threshold is reached.

## Default detection thresholds

The kill switch evaluates trigger activity against the following default thresholds. All thresholds are configurable by users through system properties:

-   Fires per record per 24-hour window: 5
-   Distinct records breaching the threshold: 25
-   Consecutive days of breach before action: 3

Five tunable system properties control these thresholds and the feature's operating mode:

-   **kill\_switch.mode**: Default value: **warn\_only**. For the different operating modes the property contains, see [Operating modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aia-kill-switch.md).
-   **kill\_switch.max\_fires\_per\_window**: Fires per record that mark it as breaching. Default value: **5**.
-   **kill\_switch.min\_distinct\_records**: Breaching records needed for the window to count as runaway. Default value: **25**.
-   **kill\_switch.window\_size**: Length of one observation window. Default value: **1440 min / 24h**.
-   **kill\_switch.consecutive\_windows\_duration**: The total look back span. Default value: **4320 min / 3 days**.

## Architecture

The kill switch uses two fully decoupled execution paths.

-   **Trigger activation path**

    Runs on every conversation start. When a trigger matches a record and fires, an audit row is written to the audit table before the conversation begins. Audit writes never interrupt or fail the user's conversation.

-   **Evaluator path**

    A scheduled job runs once daily. It reads the audit table, computes a `cycleStart` date, and assigns each active trigger a stage value \(`K`\) from 0 to 3 based on the number of consecutive days the trigger has breached the threshold. If `K` is 1 or higher, the evaluator sends a warning email. If `K` reaches 3 and enforce mode is active, the evaluator also disables the trigger.


**Note:**

-   Warning emails are sent to the trigger creator and to the creators of any agents or workflows associated with the trigger. Alerts follow the same notification mechanism used for all existing Now Assist alert purposes.
-   Re-enabling an inactive trigger resets the cycle, so the next evaluator run treats the trigger as a fresh Day 1.

## Operating modes

The `kill_switch.mode` system property controls how the feature responds to a detected breach.

-   **`off`**

    Audit rows are still written, but the evaluator performs no detection, sends no warnings, and never disables triggers.

-   **`warn_only`**

    The evaluator sends a daily warning email for each day the breach pattern is present. Triggers are never inactive. This is the shipped default.

-   **`enforce`**

    The evaluator sends the same tiered warnings on Days 1 and 2. On Day 3, it sends a final warning and deactivates the trigger configuration, including associated many-to-many and override rows.


## Escalation sequence

In `warn_only` or `enforce` mode, the evaluator sends progressively stronger email notifications as the breach continues.

-   **Day 1 — Early warning:** \[1 of 3\] Action Recommended — Trigger Firing at Unusual Rate
-   **Day 2 — Stronger warning:** \[2 of 3\] Action Required — Trigger Has Been Firing at High Volume for 2 Consecutive Days
-   **Day 3 — Final warning \(enforce mode also disables\):** \[3 of 3\] Trigger inactive — High Volume Detected for 3 Consecutive Days

Each email includes the agent name, trigger name, affected record count, and a direct link to the trigger configuration.

