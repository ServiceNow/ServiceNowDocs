---
title: Interaction context and channel metadata
description: Context and channel metadata are document ID fields included as part of interactions. Both types of records store information about the interaction.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/interaction-management/interaction-context-channel-metadata.html
release: zurich
product: Interaction Management
classification: interaction-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Interaction Management, Interaction Management, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Interaction context and channel metadata

Context and channel metadata are document ID fields included as part of interactions. Both types of records store information about the interaction.

## Context

Context for an interaction tracks the information for an interaction, such as the initial question, asset tagging, or device location. Context records are stored on the interaction\_json\_blob table by default, however you can use any table to store a context record.

## Channel metadata

Channel metadata contains the information needed to interact with the channel on which communication is happening on, for example, the chat or phone channels. Channel metadata can be free-form JSON or a reference to another record.

**Parent Topic:**[Configuring Interaction Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/interaction-management/configuring-interaction-management.md)

