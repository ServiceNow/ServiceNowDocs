---
title: Help resolve health and safety cases agentic workflow
description: Use the Help resolve health and safety cases agentic workflow to enable faster resolution of cases. It enhances the management of Health and Safety cases by improving the time to response for safety teams.
locale: en-US
release: australia
product: Now Assist for Health and Safety
classification: now-assist-for-health-and-safety
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use agentic workflows, Now Assist for Health and Safety, Health and Safety, Employee Service Management]
---

# Help resolve health and safety cases agentic workflow

Use the **Help resolve health and safety cases** agentic workflow to enable faster resolution of cases. It enhances the management of Health and Safety cases by improving the time to response for safety teams.

The **Help resolve health and safety cases** is a case analyzer agentic workflow designed to support safety teams in resolving cases more quickly and effectively. It reviews related historical cases, analyzes actions taken, and reviews available knowledge base articles to generate suitable action plans. You can select one or more preferred actions from the suggestions to apply to the current case. This process helps safety teams benefit from previous resolutions, reducing the time and effort required to close new cases.

To access the agentic workflow:

1.  Navigate to All&gt;AI Agent Studio&gt;Overview.
2.  Select **Help resolve Health and Safety cases**.

    The Help resolve health and safety cases **Describe and connect** workflow opens.

3.  Select **Continue** or select **Define trigger** to review the trigger factor for this agentic workflow.

    **Note:** Confirm that the application scope is selected as **AI agents for Health and Safety** to enable the **Save** option when you change the trigger status to Active. For more information on changing the application scope, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=australia&pubname=australia-application-development&ft:locale=en-US).

4.  Enable the Now Assist panel from the **Select display** option.

## AI agents used in the Help resolve health and safety cases agentic workflow

The **Connect AI agents** section in the **Describe and connect** workflow displays the AI Agents that are working on the **Help resolve Health and Safety cases** workflow.

The following agent is used to help resolve Health and Safety cases workflow:

|AI agent name|Description|
|-------------|-----------|
|Health and safety case analyzer AI agent|AI agent recommends actions from similar health and safety cases and AIA RAG Retrieval of Knowledge Base articles are suggested to the user.|

|Name|Type|Execution Mode|
|----|----|--------------|
|Display message of no recommended actions|Scripts|Autonomous|
|Get similar actions for Health and Safety case|Scripts|Autonomous|
|Notify user of recommended actions|Scripts|Autonomous|
|Get details of health and safety case|Flow Actions|Autonomous|
|Add selected actions to health and safety case|Scripts|Autonomous|
|Get relevant knowledge articles|Search retrievals|Autonomous|

