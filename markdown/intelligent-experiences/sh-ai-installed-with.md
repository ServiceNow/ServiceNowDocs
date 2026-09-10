---
title: Components installed with Shadow AI
description: Activating Shadow AI installs a plugin and a set of tables that store detected AI usage.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sh-ai-installed-with.html
release: australia
topic_type: reference
last_updated: "2026-08-20"
reading_time_minutes: 2
keywords: [Shadow AI, installed components, plugin, tables]
breadcrumb: [Reference, Detecting shadow AI, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Components installed with Shadow AI

Activating Shadow AI installs a plugin and a set of tables that store detected AI usage.

## Plugin installed

|Plugin|Plugin ID|Description|
|------|---------|-----------|
|Shadow AI|`sn_shadow_ai`|Detects unsanctioned AI usage across your organization through Armis and Agent Client Collector \(ACC\), and gives an AI steward a place to review and act on what's found.|

## Tables installed

Activation installs the following tables to store detected AI usage. Tables that support internal processing only, such as staging and ingestion-run logging, aren't included here.

<table id="table_sh_ai_tables_installed"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Shadow AI Observation

\[sn\_shadow\_ai\_observation\]

</td><td>

The deduplicated record of a detected AI application, MCP tool, or model. Carries the current review status, risk information, and links to any matched, approved asset.

</td></tr><tr><td>

Shadow AI Usage Event

\[sn\_shadow\_ai\_usage\_event\]

</td><td>

One row per detected usage transaction: timestamp, byte counts, and, when ACC can report it, the specific model called. Retained for 30 days.

</td></tr><tr><td>

Shadow AI Conversation

\[sn\_shadow\_ai\_conversation\]

</td><td>

Groups usage events that belong to the same session. Populated only for sources that report session grouping, currently ACC.

</td></tr><tr><td>

Shadow AI Prompt

\[sn\_shadow\_ai\_prompt\_event\]

</td><td>

Captured prompt and response content associated with a usage event. Retained for the same 30 days as the usage event it belongs to.

</td></tr><tr><td>

Shadow AI MCP Tool

\[sn\_shadow\_ai\_tool\_event\]

</td><td>

Captured MCP tool-call information, including tool name and input, reported by ACC.

</td></tr><tr><td>

Shadow AI Detected Usage Rollup

\[sn\_shadow\_ai\_usage\_daily\]

</td><td>

Daily rollup of usage events by service, user, and device. Backs the trend and event-count displays, and the source the AI-generated recommendations evaluate.

</td></tr><tr><td>

Shadow AI Attachment

\[sn\_shadow\_ai\_attachment\_event\]

</td><td>

Captured attachment information for a usage event, including the file type. Backs the **Attachments** card.

</td></tr><tr><td>

Shadow AI Per User Usage

\[sn\_shadow\_ai\_user\_usage\]

</td><td>

Aggregated usage by user, kept so a who-used-what summary survives after the underlying usage events are purged.

</td></tr><tr><td>

Shadow AI Per Device Usage

\[sn\_shadow\_ai\_device\_usage\]

</td><td>

Aggregated usage by device, kept for the same reason as per-user usage.

</td></tr><tr><td>

Shadow AI Registry Domain

\[sn\_shadow\_ai\_registry\_domain\]

</td><td>

The catalog of domain patterns Shadow AI uses to recognize a URL as an AI service. Each entry carries its match type, and its vendor and category classification. Backs the AI services registry.

</td></tr><tr><td>

Shadow AI Registry Vendor

\[sn\_shadow\_ai\_registry\_vendor\]

</td><td>

The AI providers that registry domains are attributed to.

</td></tr><tr><td>

Shadow AI Registry Category

\[sn\_shadow\_ai\_registry\_category\]

</td><td>

The AI categories a registry domain can be classified into.

</td></tr><tr><td>

Shadow AI Registry Ignore Signal

\[sn\_shadow\_ai\_registry\_ignore\_signal\]

</td><td>

Records a registry entry marked **Not Shadow AI**, with the reason given. This is what stops Shadow AI reporting a domain going forward.

</td></tr><tr><td>

Shadow AI Policy

\[sn\_shadow\_ai\_policy\]

</td><td>

One row per block decision, with its scope and the reason given.

</td></tr><tr><td>

Shadow AI Source Connection

\[sn\_shadow\_ai\_source\_connection\]

</td><td>

Tracks each detection source connection you set up from Settings, Integrations, Connectors, currently Armis and ACC.

</td></tr></tbody>
</table>**Parent Topic:**[AI Control Tower Shadow AI reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-reference.md)

