---
title: Create actions for safety incidents agentic workflow
description: Use the Create actions for safety incidents agentic workflow to suggest actions automatically for a specific incident and create actions in the Health and Safety workspace.
locale: en-US
release: australia
product: Now Assist for Health and Safety
classification: now-assist-for-health-and-safety
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use agentic workflows, Now Assist for Health and Safety, Health and Safety, Employee Service Management]
---

# Create actions for safety incidents agentic workflow

Use the **Create actions for safety incidents** agentic workflow to suggest actions automatically for a specific incident and create actions in the Health and Safety workspace.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.
2.  Select **Create actions for safety incidents**.

Safety agents and managers with the \[now\_assist\_panel\_user\] role can view the Now Assist panel. This panel can automatically trigger responses and create actions once an incident is opened. Once the actions are suggested by agentic AI, the safety agents and managers can enter the preferred action number or description. Entering the action number automatically creates that specific action record in the health and safety action-related item in an open incident record.

For more information on the Now Assist panel, see Now Assist panel.

The AI agents and tools used for the **Create actions for safety incidents** agentic workflow are as follows:

|AI Agent name|Description|
|-------------|-----------|
|Health and safety incident analysis AI agent|Recommended actions from similar health and safety incidents and AIA RAG Retrieval of Knowledge Base articles are suggested to the user.|
|Health and Safety action planner AI agent|Selected safety actions are added to the safety incident.|

|Name|Type|Execution Mode|
|----|----|--------------|
|Get details of health and safety incident|Flow Actions|Autonomous|
|Notify user of recommended actions|Scripts|Autonomous|
|Get actions from similar health and safety incidents|Scripts|Autonomous|
|Display message of no recommended actions|Scripts|Autonomous|
|Get relevant Knowledge articles|Search retrievals|Autonomous|

|Name|Type|Execution Mode|
|----|----|--------------|
|Add selected safety actions to safety incident|Scripts|Autonomous|

