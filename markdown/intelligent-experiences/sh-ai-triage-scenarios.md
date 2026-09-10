---
title: Shadow AI triage examples
description: Worked examples show how an AI steward moves from a detected AI service to a decision about it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sh-ai-triage-scenarios.html
release: australia
topic_type: concept
last_updated: "2026-08-21"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Detecting shadow AI, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Shadow AI triage examples

Worked examples show how an AI steward moves from a detected AI service to a decision about it.

The following scenarios walk through how an AI steward reviews a detected AI service and decides what to do about it. Each scenario shows what Shadow AI detected, what the AI steward finds on the record, and what those signals support. For the signals each detection method reports, see [How Shadow AI detects unsanctioned AI use](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-how-detection-works.md).

## Scenario 1: Acting on AI use detected across your network

An AI steward reviews the **Detected AI traffic** list and finds a code assistant domain with 340 events from 22 users over the last 30 days, one of the heaviest detections in the organization.

**What Shadow AI detected**

Armis identified the traffic at the network layer. Several of the devices involved are contractor laptops that aren't enrolled in the organization's endpoint management, so this usage reached the AI steward through network observation rather than through any agent on those machines.

**What the AI steward finds**

The **Overview** tab shows 22 unique users across 4 departments and the total volume sent. The **Details** tab breaks that down by device, by user, and by department, and the **Events** view shows the daily pattern: steady weekday use concentrated in one engineering department, climbing over three weeks. **First detected** is 26 days earlier than **Last activity**, confirming a sustained pattern rather than a one-time spike.

**What the signals support**

The AI steward has what a reportable finding needs: a named service, a sustained usage trend, the departments involved, and the volume of data leaving the organization. An unreviewed code assistant in daily use across a contractor population is the finding that needs action.

## Scenario 2: Responding to an action item about concentrated use

An AI steward opens the Shadow AI overview. The **Top action items** widget reports that a single user accounts for most of the use of a document summarization service.

**What Shadow AI detected**

Agent Client Collector \(ACC\) detected the service on managed devices, so the record includes request content alongside its usage signals.

**What the AI steward finds**

The record shows 6 unique users against 210 events, and the **Users** view attributes roughly 180 of those events to one person in Finance. The **Attachments** card shows spreadsheets and PDFs sent to the service. On the **Conversations** tab, the AI steward expands several conversations from that user and reads prompts covering quarterly close figures and compensation bands.

**What the signals support**

The recommendation identified a usage pattern. The prompts uncover that financial and compensation data is going to a service nobody reviewed. Six users at 210 events would not warrant urgent action on volume alone.

The AI steward blocks the service for that user rather than for everyone, because the service itself is a reasonable tool and the rest of the usage looks routine. The block moves the service's policy status to **Partially blocked**, and the reason the AI steward enters is recorded in the activity history for whoever reviews this later.

This type of pattern points to an unmet need. One person summarizing financial documents by hand is a candidate for a governed alternative, and the AI steward passes that along to the team that owns the organization's approved AI tools.

## Scenario 3: Clearing a detection that isn't an AI service

An AI steward reviews a newly detected domain and recognizes it as a subdomain of the organization's own internal documentation host, matched to the AI services registry because of a pattern in its URL.

**What Shadow AI detected**

The domain matched a registry entry, so Shadow AI began reporting its traffic as a detected AI service. The record shows 40 events, all from the platform engineering department.

**What the AI steward finds**

The **Events** view shows a small, steady volume consistent with people reading internal documentation. The **AI category** and **Provider** values assigned from the registry don't match what the AI steward knows the host actually is.

**What the signals support**

All three ways of clearing a detection would remove it from the AI steward's active queue, and they differ in what happens next.

-   **Snooze for 7 days** suits a detection the AI steward expects to confirm shortly, such as waiting on a reply from the team that owns the host. The record returns in 7 days.
-   **Dismiss** suits a benign pattern the AI steward expects to see again and doesn't want to keep deciding about. The record is muted until new traffic arrives.
-   **This is not Shadow AI** suits this case, because the finding is a registry match on something that isn't an AI service at all. Shadow AI continues collecting traffic for 30 days, then stops reporting the domain.

The AI steward selects **This is not Shadow AI**. Because the service status and the registry entry are linked, the domain is also marked **Not Shadow AI** in the registry, which stops future detections rather than just hiding this one. If the decision needs reversing later, the AI steward marks the domain active again in the registry. See [Manage the AI services registry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-manage-registry.md).

Choosing **Dismiss** here instead would have left the registry entry active, so the same domain would resurface as a new detection every time the documentation host saw traffic.

