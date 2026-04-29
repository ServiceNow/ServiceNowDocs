---
title: Golden image structure and modularity
description: The following table outlines the structure and modularity of the golden image mode for cloning agents, based on the operating system \(OS\) in use.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-29"
reading_time_minutes: 1
breadcrumb: [ACC-F reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# Golden image structure and modularity

The following table outlines the structure and modularity of the golden image mode for cloning agents, based on the operating system \(OS\) in use.

| |Linux|macOS|Windows|
|---|-----|-----|-------|
|**Trigger type**|marker file|plist key|msi property|
|**Fresh install handling**|supported, no action required|supported|supported|
|**Service control**|stop and disable|skip load|stop and disable|
|**Identity handling**|cache wipe|skip restore|skip restore|
|**Certificate handling**|cert wip|skip restore|cert wipe|
|**Runtime state**|Cache and database wipe|skip restore|Cache and database wipe|

**Parent Topic:**[Agent Client Collector Framework reference](agent-client-collector-reference.md)

