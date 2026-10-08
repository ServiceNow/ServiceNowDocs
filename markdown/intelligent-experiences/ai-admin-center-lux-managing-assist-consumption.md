---
title: Managing assist consumption \(Lux UI\)
description: The Assist consumption page provides features that enable you to view the assists consumed on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-admin-center-lux-managing-assist-consumption.html
release: australia
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 1
keywords: [AI Admin Center, Now Assist Center, AI, AI setup, assist consumption]
breadcrumb: [Setting up AI capabilities and configurations, AI Admin Center, Enable AI experiences]
---

# Managing assist consumption \(Lux UI\)

The Assist consumption page provides features that enable you to view the assists consumed on your instance.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

**Note:** This topic describes the AI Admin Center feature based on the Lux user experience \(UI\). There is no Next Experience UI version of this topic.

An assist is the unit of measurement for AI usage on the ServiceNow AI Platform. Assists are used to measure usage of generative AI skills through performed skill actions. Users consume assists when they execute skill actions.

Different skill actions consume different numbers of assists based on complexity. An assist is not a 1:1 ration with a user action. Each skill carries an assist ratio reflecting its relative cost, and total assists are calculated by multiplying the number of actions by the assist ratio. A simple summarization and a multi-step agentic execution consume very different amounts.

Three asset types consume assists: skills, conversational assistants, and AI agents and agentic workflows.

