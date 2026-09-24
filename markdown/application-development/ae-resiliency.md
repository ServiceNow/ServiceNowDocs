---
title: Resilience in Autonomous Engineer
description: Autonomous Engineer monitors background agents during execution and automatically detects and retries work items that get stuck or unresponsive.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ae-resiliency.html
release: brazil
topic_type: concept
last_updated: "2026-09-08"
reading_time_minutes: 1
keywords: [Autonomous Engineer, resiliency, stuck agent, automatic retry, background agents, work items, execution]
audience: programmer
breadcrumb: [Overview, Autonomous Engineer, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Resilience in Autonomous Engineer

Autonomous Engineer monitors background agents during execution and automatically detects and retries work items that get stuck or unresponsive.

Autonomous Engineer runs work items in parallel using background agents. During execution, individual agents or jobs can get interrupted or unresponsive due to platform conditions, long-running operations, or transient failures. The resiliency framework monitors for these conditions and takes action automatically so that execution continues without requiring manual intervention in most cases.

## Stuck agent detection

A scheduled job monitors all active work items during execution. When a background agent has not responded within a configurable time threshold, Autonomous Engineer treats that work item as stuck. The resiliency monitor identifies the agent handling the work item and cancels it, then retries the work item automatically.

## Retry behavior

When a work item is retried, Autonomous Engineer generates a new background agent for it and attempts execution again. The plan dashboard reflects the updated state of the work item as the retry progresses.

## Interrupted and long-running jobs

In addition to stuck agents, the resiliency monitor handles jobs that are interrupted by platform events such as instance restarts. Interrupted jobs are detected by the same scheduled monitoring job and are resubmitted automatically when the instance recovers.

Long-running jobs, such as jobs that are making progress but have been active longer than typical, are monitored separately. The resiliency framework does not cancel long-running jobs that show ongoing activity; it cancels only jobs that have stopped responding within the threshold period.

**Parent Topic:**[Exploring Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/exploring-autonomous-engineer.md)

