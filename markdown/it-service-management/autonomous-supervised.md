---
title: Autonomous and supervised execution modes
description: Learn about the differences between autonomous and supervised execution modes for AI specialists to help determine which should be used for your use cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/autonomous-supervised.html
release: zurich
topic_type: concept
last_updated: "2026-05-05"
reading_time_minutes: 2
breadcrumb: [Explore, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Autonomous and supervised execution modes

Learn about the differences between autonomous and supervised execution modes for AI specialists to help determine which should be used for your use cases.

AI specialists can help handle incidents from beginning to end. They can classify and triage incoming user requests, then investigate related incidents and other knowledge sources for resolutions. If they need clarification, they can send updates to the requester through the activity feed. If a resolution is found, the AI specialist can propose the solution to the requester. If it can't locate a solution or lacks confidence in the solution it found, it can reroute the incident to a human fulfiller to continue the work.

The **execution mode** of the AI specialist determines its autonomy when performing tasks on incidents. The two types of execution modes are **Autonomous** and **Supervised**. Each instance of an AI specialist can have its execution mode set in the **Investigate and resolve** task configuration.

## Autonomous execution mode

In **Autonomous** mode, the AI specialist performs tasks on incidents without pausing to ask for permission before acting. This is the default configuration.

The general flow of autonomous execution is as follows:

1.  A incident is assigned to the AI specialist.
2.  It triages the incident after reviewing the description, attachments, and relevant context.
3.  It searches knowledge bases, past incidents, known errors, and catalog items to identify a solution. It can also ask the requester follow-up questions to get additional information.
4.  If a solution is found, it posts a solution to the requester and moves the incident to Solution Proposed, which proceeds to Resolved. No requester confirmation is required.
5.  If it needs additional information from the requester, but the requester doesn't respond after the configured number of actions, the incident is rerouted to a human fulfiller. Default number of actions is 3.

## Supervised execution mode

In **Supervised** mode, the AI specialist reasons and researches on its own, but it does not take any action without explicit permission by a human fulfiller.

The general flow of supervised execution is as follows. The first three steps of the flow are the same as in **Autonomous** mode.

1.  A incident is assigned to the AI specialist.
2.  It triages the incident after reviewing the description, attachments, and relevant context.
3.  It searches knowledge bases, past incidents, known errors, and catalog items to identify a solution. It can also ask the requester follow-up questions to get additional information.
4.  If a solution is found, it presents the proposed solution and asks for confirmation by a human fulfiller.
5.  The human fulfiller reviews the solution.
6.  If the human fulfiller accepts the solution, the AI specialist posts the solution, and the incident moves to Solution Proposed.
7.  If the human fulfiller doesn't accept the solution, the AI specialist goes back to the investigation phase to find an alternate solution.

The same communication and rerouting rules from **Autonomous** mode apply to **Supervised** mode.

## Communication with users

The AI specialist uses the incident's activity feed to communicate with the requester. It doesn't send emails on its own. If you have emails configured to notify requesters that their incident has changed states or received comments, those emails are still sent. To change that behavior, you must update the email notification settings. They are unaffected by the execution mode of the AI specialist.

## Configuring execution mode

When configuring or activating any specific AI specialist, you choose which execution mode it uses. There is no global setting that affects the execution mode of all AI specialists. You can also change the execution mode of an AI specialist at any time.

