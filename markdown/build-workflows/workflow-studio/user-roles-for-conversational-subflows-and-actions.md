---
title: User roles for conversational subflows and actions
description: Provide personnel with one or more user roles to grant them access to conversational subflows and actions.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# User roles for conversational subflows and actions

Provide personnel with one or more user roles to grant them access to conversational subflows and actions.

|Role|Description|Contains roles|Groups with this role|Special considerations|
|----|-----------|--------------|---------------------|----------------------|
|Virtual Agent administrator \[virtual\_agent\_admin\]|Provides read and write access to all Virtual Agent tables, conversational experiences, and Now Assist admin operations|action\_designer,flow\_designer|None|Avoid granting an admin role when more specialized roles are available.|
|Workflow Conversational Admin \[sn\_conv\_fa.conv\_fa\_admin\]|Provides read access to flows, subflows, and actions. Provides read and write access to conversational experience settings.|sn\_conv\_fa.conv\_fa\_designer, fd\_read\_actions, fd\_read\_flows|None|Avoid granting an admin role when more specialized roles are available.|
|Flow/Action Designer Conversational Workflow \[sn\_conv\_fa.conv\_fa\_designer\]|Provides read and write access to conversational experience settings.|None|None|This is a specialized role with limited access.|
|Action Designer \[action\_designer\]|Provides read and write access to Workflow Studio actions.|sn\_conv\_fa.conv\_fa\_designer|None|This is a specialized role with limited access.|
|Flow Designer \[flow\_designer\]|Provides read and write access to Workflow Studio flows and subflows.|sn\_conv\_fa.conv\_fa\_designer|None|This is a specialized role with limited access.|
|Email Write \[sn\_conv\_fa.csa\_email\_write\]|Provides write access to the sys\_email table to conversational subflows and actions.|None|None|This is a specialized role with limited access.|

**Parent Topic:**[Flows, subflows, and actions reference](flow-designer-reference.md)

