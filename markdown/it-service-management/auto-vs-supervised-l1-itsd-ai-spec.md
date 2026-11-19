---
title: Autonomous and supervised execution modes
description: Autonomous and supervised execution modes control how independently a L1 IT Service Desk AI Specialist acts when handling incidents. Use this information to choose the right mode for your use cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/auto-vs-supervised-l1-itsd-ai-spec.html
release: brazil
topic_type: concept
last_updated: "2026-10-15"
reading_time_minutes: 3
breadcrumb: [Explore, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Autonomous and supervised execution modes

Autonomous and supervised execution modes control how independently a L1 IT Service Desk AI Specialist acts when handling incidents. Use this information to choose the right mode for your use cases.

AI specialists can help handle incidents from beginning to end. They can classify and triage incoming user requests, then investigate related incidents and other knowledge sources for resolutions. If clarifying questions are turned on and the AI specialist needs more information, it can ask the requester through the activity feed. If a resolution is found, the AI specialist can propose the solution to the requester. If it can't identify a solution with sufficient confidence, it can reroute the incident to a human fulfiller to continue the work.

The execution mode of the AI specialist determines its autonomy when performing tasks on incidents. The two types of execution modes are **Autonomous** and **Supervised**. Each instance of an AI specialist can have its execution mode set in the **Investigate and resolve** task configuration.

## Autonomous execution mode

In **Autonomous** mode, the AI specialist performs tasks on incidents without pausing to ask for permission before acting. This is the default configuration.

The general flow of autonomous execution is as follows:

1.  An incident is assigned to the AI specialist.
2.  It triages the incident after analyzing the description, attachments, and relevant context.
3.  It searches knowledge bases, past incidents, known errors, and catalog items to identify a solution. If clarifying questions are turned on, it can also ask the requester for missing information.
4.  If a solution is found, it posts a solution to the requester and moves the incident to Solution Proposed. No requester confirmation is required. The incident stays On Hold. If the requester does not reply within the number of days set in sn\_itsm\_l1\_ais.glide.ui.autoresolve.time \(default 2\), the incident is resolved automatically. A reply before then reopens the conversation.

    **Note:** Set sn\_itsm\_l1\_ais.glide.ui.autoresolve.time to 0 to turn off automatic resolution.

5.  If the requester replies more times than the **Replies before reassigning** setting allows \(default 10\), the incident is reassigned to a human fulfiller.

**Note:** Clarifying questions are off by default. To let the AI specialist ask the requester for missing information and wait for the reply, set the system property sn\_itsm\_l1\_ais.awaiting\_info.enabled to true. When it is false, the incident is reassigned to a human fulfiller. Catalog variable questions are always asked.

## Supervised execution mode

In **Supervised** mode, the AI specialist reasons and researches on its own, but it does not post a solution to the requester without explicit permission by a human fulfiller. In **Supervised** mode the AI specialist still fills the fields selected in **Fields to predict**, and, when **Cross-group reassignment** is **On**, still changes the assignment group.

The general flow of supervised execution is as follows. The first three steps of the flow are the same as in **Autonomous** mode.

1.  An incident is assigned to the AI specialist.
2.  It triages the incident after analyzing the description, attachments, and relevant context.
3.  It searches knowledge bases, past incidents, known errors, and catalog items to identify a solution. If clarifying questions are turned on, it can also ask the requester for missing information.
4.  If a solution is found, it presents the proposed solution and asks for confirmation by a human fulfiller.
5.  The human fulfiller reviews the solution.
6.  If the human fulfiller accepts the solution, the AI specialist posts the solution, and the incident moves to Solution Proposed. The incident stays On Hold and is resolved automatically if the requester does not reply within the number of days set in sn\_itsm\_l1\_ais.glide.ui.autoresolve.time \(default 2\). A reply before then reopens the conversation.
7.  If the human fulfiller doesn't accept the solution, the AI specialist returns to the investigation phase to find an alternate solution.

The same communication and rerouting rules from **Autonomous** mode apply to **Supervised** mode.

## Communication with users

The AI specialist uses the incident's activity feed to communicate with the requester. It doesn't send emails on its own. If you have emails configured to notify requesters that their incident has changed states or received comments, those emails are still sent. To change that behavior, you must update the email notification settings. They are unaffected by the execution mode of the AI specialist.

## Configuring execution mode

When configuring or activating any specific AI specialist, you choose which execution mode it uses. There is no global setting that affects the execution mode of all AI specialists. You can also change the execution mode of an AI specialist at any time.

