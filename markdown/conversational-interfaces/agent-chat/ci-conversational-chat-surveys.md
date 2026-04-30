---
title: Chat surveys
description: Display conversational questionnaires to your end users to gather important information from them, before and after they chat with a live or virtual agent.
locale: en-US
release: xanadu
product: Agent Chat
classification: agent-chat
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Explore, Agent Chat, Conversational Interfaces]
---

# Chat surveys

Display conversational questionnaires to your end users to gather important information from them, before and after they chat with a live or virtual agent.

## How chat surveys work

Instead of using forms to collect information from your requesters, you can create different questionnaires that run in the chat client to capture preliminary user information or post-chat feedback. The questions in the following pre-chat survey example ask users to identify their service issue and to provide additional details.

![Web chat client with pre-chat surveys highlighted.](../image/pre-chat-survey-example.png "Example pre-chat survey conversation")

Survey administrators and administrators use [Survey Designer](https://www.servicenow.com/docs/access?context=c_SurveyDesigner&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) to:

-   Build survey content: Survey Designer provides various controls for defining survey questions. The example above shows the choice list control, which displays a list of items that your users can choose from. Each survey question has corresponding properties that you can set to manage survey behavior. For instance, you can make a survey response mandatory. If you make a survey response optional, users can skip the question in the survey. You can also configure your survey so that an introductory note starts the survey and an end note displays after users finish the survey.
-   \(Optional\) Save certain survey responses as chat context: When defining your survey, you can map a particular survey question to a chat context variable so that survey responses are stored in the context variable. You can then use these variables to route chats to live agents in certain queues, by specifying the chat context variables in routing conditions or to the virtual agent.

After creating the surveys, administrators configure the surveys to run as conversations in the chat client. The chat client renders the chat survey as a live chat conversation.

## What to do next

Setting up chat surveys involves these main steps:

![Infographic describing steps for setting up pre-chat and post-chat conversational surveys.](../image/survey-implementation-steps.png)

-   **[1. \(Optional\) Define chat context.](../task/ac-configure-context-variables.md)**

    Configure the chat context variables for storing survey responses using **Context Variables** in Chat Settings.

-   **[2. Create chat surveys](../task/create-chat-surveys.md)**

    In Survey Designer, build your conversational questionnaires for gathering pre-chat information and post-chat feedback from your requesters. If you defined chat context variables to store certain survey responses, you can map the appropriate survey question to the corresponding chat context variable.

-   **[3. Define pre-chat survey configurations.](../task/ac-configure-pre-chat-surveys.md)**

    Determine the pre-chat questionnaire to be presented to your requesters based on conditions that you apply.

-   **[4. Define post-chat survey configurations.](../task/define-post-chat-survey-config.md)**

    Control the post-chat questionnaire displayed to your requesters to gather feedback on their experience with live agents.

-   **[5. If using Virtual Agent, define context topic intent configurations.](../task/ac-configure-context-topic-intent.md)**

    Use pre-chat survey information to determine the appropriate Virtual Agent conversation topic automatically displayed to your requesters, rather than prompting them to choose from a list of conversation topics.


The Interaction Related Records list stores the post-survey chat results and creates a related record that links the assessment to the live agent \(fulfiller\).

