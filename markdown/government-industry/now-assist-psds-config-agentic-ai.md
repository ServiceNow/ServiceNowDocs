---
title: Configure AI Agents for Public Sector Digital Services
description: Configure the Now Assist AI Agents to execute use cases and complete tasks autonomously in Public Sector Digital Services.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Implement Intelligence, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configure AI Agents for Public Sector Digital Services

Configure the Now Assist AI Agents to execute use cases and complete tasks autonomously in Public Sector Digital Services.

## Before you begin

Role required: admin, sn\_aia\_trigger\_configuration

## About this task

To get started with AI Agents, you must have the sn\_gsm\_ai\_agents plugin installed, as well as the Now Assist panel and AI Search enabled on your instance.

## Procedure

1.  Ensure that the Now Assist Panel and AI Search module are both enabled.

    For instructions on how to enable the Now Assist panel and on how to set up AI Search, see [Install and configure Now Assist for Public Sector Digital Services \(PSDS\)](now-assist-psds-configuring.md) and [Enabling and configuring AI Search with Now Assist for PSDS](now-assist-psds-enabling-configuring-ai-search.md).

2.  Navigate to **All** &gt; **AI Search** &gt; **Indexed Sources.**.

3.  Locate the Information Request Table and select the record.

4.  Select **Index All Tables** to start the indexing process.

5.  Select **Indexing History** once it is completed to ensure the Keyword Ingestion State has changed from Indexing to Indexed.

6.  Select **Publish** to publish the search source for the Information Request table.

7.  Create a KB article that will contain the criteria for determining whether a fee waiver request should be approved or rejected.![KB article creation.](../image/create_kb_article_aiagents_psds.png)

    The KB article must have a unique name and number.

8.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and Manage**.

9.  Select **Help manage public information requests**.

10. Select **Define trigger**, and select **Information Request Fee Estimation and Review Trigger**.

11. Set the trigger to **Active**, and select **Save**, then **Continue**.

    **Note:** By default, the trigger is set to active.

12. Set Display to **Active**, then select **Save and Test**.


## Result

The agentic workflow is now active. On this page, you can run a one-time test of the AI agent or agentic workflow to see how it thinks through the given task.

