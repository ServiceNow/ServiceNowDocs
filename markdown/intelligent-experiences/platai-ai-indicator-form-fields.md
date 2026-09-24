---
title: AI indicator on form fields
description: The AI indicator is a badge that identifies form fields containing content generated or updated by an AI agent in Core UI and configurable workspaces.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/platai-ai-indicator-form-fields.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Creating AI user experiences, Enable AI Experiences]
---

# AI indicator on form fields

The AI indicator is a badge that identifies form fields containing content generated or updated by an AI agent in Core UI and configurable workspaces.

AI indicators help distinguish AI-generated updates from human edits on a record. When an AI agent updates a field, an AI indicator appears next to the field label. Selecting the indicator opens a popover that displays a brief message. When a record contains one or more AI-updated fields, a record-level alert is displayed as a reminder to review AI-generated content before using or acting on it.

**Note:** The popover and alert messages aren't configurable.

\[Omitted image "ai-form-indicators.png"\] Alt text: AI indicators on a form in a configurable workspace.

AI indicators appear:

-   When you open a record that contains one or more fields updated by an AI agent.
-   When an AI workflow updates a field while the record is open, a live update notification appears.

AI indicators clear:

-   When you manually modify the AI-generated value. Actions such as hovering over the indicator, selecting it, moving focus to the field, or saving the form do not clear the indicator.
-   When a client script overwrites the AI-generated value.

AI indicators reappear when the field value is restored to the AI-generated value.

## Configuration and AI activity tracking

AI indicators are included in the AI Field Activity \(com.glide.ai\_field\_activity\) plugin, which is installed with the Generative AI Controller \(sn.generative.ai\) plugin. No additional configuration is required.

-   Information about AI-generated activity is stored in the sys\_ai\_record\_activity table.
-   This tracking data distinguishes AI-generated updates from manual edits, enables the display of AI indicators on form fields, and supports auditing, compliance, and AI governance.
-   AI indicator activity records are retained for 365 days by default unless the associated AI indicator is cleared when the field value is manually modified.
-   Admins can modify this retention period by configuring sys\_auto\_flush for the sys\_ai\_record\_activity table.

AI tracking is enabled for all tables except the following:

-   Tables with the prefixes:
    -   sys\_
    -   v\_
    -   sysevent
    -   syslog
    -   sysrule
    -   sysauto
    -   sn\_
    -   one\_
    -   var\_
-   Infrastructure-related tables with the prefixes:
    -   wf\_
    -   jrobin
    -   ecc\_
    -   hermes
    -   pa\_
    -   sa\_
    -   ua\_
    -   report\_stats
-   High-volume telemetry, log, and queue tables, including:
    -   report\_executions
    -   metric\_instance
    -   service\_mapping\_status
    -   sp\_log
    -   sla\_async\_queue
    -   attachment\_scan\_history
    -   itam\_asset\_usage
    -   itam\_ci\_usage
    -   ts\_query\_kb
    -   ts\_search\_summary
    -   label\_entry
    -   label\_history
    -   qc\_node\_metric
    -   qc\_candidate\_query
-   To enable AI activity tracking for a specific table, add the dictionary attribute **no\_ai\_record\_activity** and set it to **false**. To disable tracking, set the dictionary attribute to **true**.

**Note:** To disable AI indicators on form fields, create a system property named **glide.ai.field\_indicators.enabled**, and set it to **false**. By default, this property is set to **true**.

**Parent Topic:**[Creating AI user experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platai-creating-ai-user-experiences.md)

