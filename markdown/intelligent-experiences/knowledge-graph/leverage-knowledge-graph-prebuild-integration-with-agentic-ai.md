---
title: Leverage Knowledge Graph prebuild integration with AI agents
description: The prebuilt integrations of Knowledge Graph, can improve live agent productivity by assisting AI agents in performing tasks and answering user queries.
locale: en-US
release: yokohama
product: Knowledge Graph
classification: knowledge-graph
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Exploring Knowledge Graph, Knowledge Graph, Enable AI experiences]
---

# Leverage Knowledge Graph prebuild integration with AI agents

The prebuilt integrations of Knowledge Graph, can improve live agent productivity by assisting AI agents in performing tasks and answering user queries.

In this release, the available prebuilt integrations with AI agents are:

1.  Integration with Now Assist AI agents for User Context: Helps users with personalized responses.
2.  Integration with AI agents as a tool: Used to perform specific tasks that are assigned to the AI agents.

## Integration with AI agents for User Context

For the users of Now Assist, AI agents integrates the context from the prebuilt User Profile schema to fetch relevant data and provide personalized responses.

By leveraging relationships between users, teams, and content, Now Assist AI agents can fetch relevant, permission-aware user information and provide answers to reduce slot-filing requirement.

Here’s an example use case of how Knowledge Graph is used within AI agents for user context.

-   A user needs assistance in writing their resume, so they use ServiceNow AI agents called Resume builder.
-   The user ads their task: `Build my resume`.
-   AI agents uses Knowledge Graph to fetch the following information from the user profile schema:
    -   First name
    -   Last name
    -   Location
    -   Email ID
    -   Phone number
    -   Occupation
-   AI agents reverts with the available information and request for the missing information to proceed building the resume.
-   Once the agent as all the required information, it provides user with output.

## Integration with AI agents as a tool

Knowledge Graph can now be used as a tool within AI agents. Users can choose Knowledge Graph to perform tasks, while creating an Agent.

You can define the flow action to use Knowledge Graph as a reusable operation in automating the ServiceNow AI Platform features without having to write code.

See [Add a Knowledge Graph to an AI agent](../../now-assist-ai-agents/task/add-knowledge-graph.md) to add Knowledge Graph to an AI agents in AI Agent Studio.

Example use case:

-   A user wants to view and retire all the assets assigned to another user. To execute this task, user will use Asset Manager agent.
-   Asset Manager uses Knowledge Graph to fetch the asset information related to the user.
-   After processing the query, the agent provides the following output:`User has the following assets:1.<asset1> 2.<asset2> 3.<productID>- <asset 3> <purchase date>. The email address for the user is <emailId> and username <username1>.`
-   User then proceeds with the task of retiring the assets: `Proceed with retiring the assets associated with Username1.`
-   The next tool, used execute this task, will take the table name and sysId displayed in Knowledge Graph output and proceed with the task.

## Knowledge Graph API output in AI agents

When a user ask a query `What is my Manager's name?`, AI agents reaches out to Knowledge Graph to fetch this information. Here's an example output of the query:

```json
{ 

    "Manager": [ 

        { 

            "sys_user": { 

                "user_name": { 

                    "value": "abel.tuter", 

                    "displayValue": "abel.tuter" 

                }, 

                "sysId": "62826bf03710200044e0bfc8bcbe5df1", 

                "name": { 

                    "value": "Abel Tuter", 

                    "displayValue": "Abel Tuter" 

                }, 

                "first_name": { 

                    "value": "Abel", 

                    "displayValue": "Abel" 

                }, 

                "last_name": { 

                    "value": "Tuter", 

                    "displayValue": "Tuter" 

                } 

            } 

        } 

    ] 

} 
```

In this example, the table that is called is `sys_user` and column referred is `user_name`. The output also displays SysId , example: `"sysId": "62826bf03710200044e0bfc8bcbe5df1"`.

