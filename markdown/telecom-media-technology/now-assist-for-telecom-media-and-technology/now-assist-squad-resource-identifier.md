---
title: Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection Squad resource identifier agentic workflow
description: Use a squad resource identifier agentic workflow to identify and recommend internal experts based on record under consideration, skill set, region, and real-time availability.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customer Success Management, Use agentic workflows, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection Squad resource identifier agentic workflow

Use a squad resource identifier agentic workflow to identify and recommend internal experts based on record under consideration, skill set, region, and real-time availability.

## Squad resource identifier agentic workflow overview

The agentic workflow assists the customer success teams to quickly identify and connect with the right individuals to support success plays, initiatives, or critical escalations, ensuring faster and more effective collaboration across engagements.

The Squad resource identifier agentic workflow supports these tables:

-   Touchpoint \(sn\_acct\_lc\_touchpoint\)
-   Account Onboarding Case \(sn\_acct\_lc\_onb\_case\)
-   Success Task \(sn\_acct\_lc\_success\_task\)
-   Engagement \(sn\_acct\_lc\_engagement\)
-   Implementation Record \(sn\_acct\_lc\_implementation\_record\)
-   Customer Play \(sn\_acct\_lc\_success\_case\)
-   Success Initiative \(sn\_acct\_lc\_success\_initiative\)
-   Internal Play \(sn\_acct\_lc\_internal\_play\)
-   Internal Play Task \(sn\_acct\_lc\_internal\_play\_task\)
-   Risk Signal and Issue \(sn\_acct\_lc\_risk\_signal\_issue\)
-   Onboarding Task \(sn\_ti\_core\_task\)
-   Data Import Task \(sn\_ti\_core\_imp\_task\)

Role required: sn\_acct\_lc.customer\_success\_agent and sn\_acct\_lc.agent

To configure the Squad resource identifier agentic workflow, see [Squad Resource Identifier AI Workflow: Setup and Configuration Guide](https://support.servicenow.com/kb?sys_kb_id=99f441a747d6365077748d01426d433a&id=kb_article_view).

To modify the Squad resource identifier agentic workflow, Duplicate an agentic workflow, and adjust the settings according to your requirements.

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously.

## Assign customer success role

The squad members assigned through the squad resource identifier workflow aren’t automatically granted customer success roles. An administrator must manually assign the appropriate role to enable record access.

To assign customer success roles to users using the ServiceNow AI Platform user administration feature, see Assign a role to a user.

## Squad resource identifier agentic workflow

To access the use case:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Squad Resource Identifier**.

To create a use case, see Create an agentic workflow.

## Testing the agentic workflow

To access the use case testing page:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
2.  On the Overview page, select **Test use cases**.

To test the use case, see Manually test the execution of an agentic workflow.

## AI agent used in the Squad resource identifier agentic workflow

The following AI agent is used to execute the instructions for the agentic workflow.

|AI agent|AI agent role|
|--------|-------------|
|User resource recommender AI agent|Analyzes user data to identify the most relevant candidates, ranks them by priority, and automatically populates the input record with top-performing users.|

To create an AI agent, see Create an AI agent.

