---
title: Update sets and Build Agent
description: When you work with Build Agent, your changes are automatically tracked in update sets so you can review, revert, and deploy them without leaving ServiceNow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/ba-update-sets.html
release: zurich
topic_type: concept
last_updated: "2026-05-29"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Update sets and Build Agent

When you work with Build Agent, your changes are automatically tracked in update sets so you can review, revert, and deploy them without leaving ServiceNow Studio.

Build Agent tracks every change it makes to your application in update sets. Changes from each checkpoint in a conversation are captured together in a single update set. You can access, review, and open those update sets directly from the Build Agent chat panel and the Current Changes List \(CCL\) page in ServiceNow Studio, without navigating to the platform.

**Note:** Your instance must be on Zurich Patch 10 or higher to work with update sets in Build Agent.

For general information about update sets on the ServiceNow AI Platform, see [System update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/system-update-sets/system-update-sets.md).

## How Build Agent tracks changes

Build Agent automatically captures changes to the app and metadata that you're working on update set as you work.

A checkpoint is created automatically after you approve each task plan. When Build Agent reaches a checkpoint, the changes associated with that checkpoint are captured in the update set. You can view and open the relevant update set directly from each checkpoint in the chat panel. For more information on checkpoints, see [Build Agent conversation change log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ba-conversational-change-log.md).

## Access update sets from Build Agent

You can access update sets created during a Build Agent session from two locations in ServiceNow Studio.

-   **Chat panel**

    Each checkpoint in the chat panel includes a **Review** button that opens the relevant update set in a new ServiceNow Studio tab. The update set button in the summary card opens all update sets associated with the changes shown in that card.

    \[Omitted image "ba-summary-card-update.png"\] Alt text: Summary card showing a batch update set with files, each listed with its type and New status, and the Review button highlighted.

-   **Current Changes List page**

    The Current Changes List \(CCL\) page in ServiceNow Studio shows Build Agent edits. Each checkpoint on the CCL page includes a button that opens the relevant update set in a new tab.


## Revert changes using checkpoints

You can revert your application to any previous checkpoint during a Build Agent session. For more information about checkpoints and how to restore a previous state, see [Build Agent conversation change log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ba-conversational-change-log.md).

## Deploy update sets

After your changes are ready, you can find the update sets from your Build Agent session on the **Deployment** tab on the ServiceNow Studio home page. For more information about deploying your changes, see [Deploying what you built with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-deployment.md).

**Parent Topic:**[Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/use-build-agent.md)

