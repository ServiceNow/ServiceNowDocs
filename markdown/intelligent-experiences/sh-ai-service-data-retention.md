---
title: Detected AI service data retention
description: Know how long each kind of data on a detected AI service's record is retained.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sh-ai-service-data-retention.html
release: australia
topic_type: reference
last_updated: "2026-08-24"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Investigate a detected AI service, Detecting shadow AI, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Detected AI service data retention

Know how long each kind of data on a detected AI service's record is retained.

## Retention periods

Alongside per-event views on the **Details** and **Conversations** tabs, Shadow AI keeps running aggregates of usage by user and by device. These aggregates let a service retain a usage summary after its individual events are removed on the 30-day cycle.

|Retained for 30 days|Retained indefinitely|
|--------------------|---------------------|
|Individual usage events, prompts, and attachments|Aggregate counts: unique users, unique devices, and event counts, by service|
|Conversations and the events grouped inside them|The service record itself, including its status and policy history|

A service in **Limited details** status still shows which users and devices used it and how often, but no longer shows the conversations or prompts behind those counts. The service record itself, including its status and policy history, persists regardless.

**Parent Topic:**[Investigating a detected AI service in Shadow AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-investigating-detected-services.md)

