---
title: General guidelines for creating and mapping an intent
description: By following some general guidelines for creating email intents and mapping actions to intents, you can create clear and effective instructions that help maximize the efficiency and effectiveness.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Email agentic workflow, Use agentic workflows in emails, Now Assist in Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# General guidelines for creating and mapping an intent

By following some general guidelines for creating email intents and mapping actions to intents, you can create clear and effective instructions that help maximize the efficiency and effectiveness.

## Overview of creating and mapping an intent

AI agents and agentic workflows rely on LLMs, so the language that you use for their instructions is important. There are many steps that you can take to help improve the quality and consistency of your agentic AI solutions.

## Intent Guidelines

The discussion highlights several crucial guidelines for defining and configuring intents to ensure accuracy, help prevent misinterpretation, and optimize the performance of the LLM-driven system:

-   Be clear, specific, and avoid vagueness

    -   Use instructions that are concise, clear, and precise. Simple language can help remove ambiguous situations that could stall or disrupt an agent's progress.
    -   Intents should be highly specific and not overlap with other intents.
    -   Avoid using just keywords or topic names instead, describe the user's full intention.
    -   Vague intents can confuse the LLM and lead to incorrect matches.
    -   Clarify boundaries and limitations.
    |Example|Weak intent|Specific and strong intent|Notes|
    |-------|-----------|--------------------------|-----|
    |Subscription Cancellation|User requesting to cancel subscription|User requesting to cancel music subscription|If your system handles various types of subscriptions for example, music and video streaming, software licenses, a vague intent like cancel subscription could lead to the LLM incorrectly identifying which service the user wants to cancel. A specific intent like cancel music subscription ensures the LLM understands the exact service, allowing the correct workflow to be triggered.|
    |Leave Approval|Leave approval|User requesting for a leave approval|Leave approval is a topic, not an action or a user's intent. The LLM needs to understand the user's intention. By stating User requesting for a leave approval, you clearly communicate that the user is initiating a request, not just mentioning a topic.|
    |Leave Approval including recipient|User requesting for a leave approval|User requesting for a leave approval for their colleague|While the system might default to assuming the request is from the email sender, explicitly stating for their colleague provides crucial context. This prevents scenarios where a request made on behalf of someone else is incorrectly processed for the sender, highlighting the need for intelligence in understanding the subject of the request.|

-   Context and coherence:

    -   The intent should clearly articulate what the user is asking for or requesting.
    -   Distinguish between a user merely mentioning something and explicitly requesting an action.
    -   Design instructions that serve the overall objective. All of your tools and AI agents work together to solve problems.
    |User email|Incorrect Intent match|Notes|
    |----------|----------------------|-----|
    |I just bought a car, my father was insisting me on getting a car insurance quotation|Requesting for a car insurance quotation|In this scenario, the user is talking about getting a quotation because their father insisted, but they haven't explicitly requested one from the system. If an intent designed to generate a quotation matches this email, the user would receive an unsolicited quotation, leading to a poor and potentially confusing experience. The system should only act when the user's intent is a direct request for that action.|
    |Marketing email, maybe I should just unsubscribe already|Requesting to unsubscribe from emails|Marketing emails, just unsubscribe. This statement is sarcastic or a casual expression of frustration, not a direct request to unsubscribe. If the intent is configured too broadly like just "unsubscribe email", it might incorrectly trigger an unsubscribe action. The intent should be precise enough to differentiate between a casual remark and a clear, actionable request.|

-   Include critical details:

    -   Ensure the intent description contains all critical details that differentiate it from any similar requests.
    -   Use consistent formatting. Similar instructions should use similar language patterns.
    -   Missing critical details can lead to false positives or false negatives.
    -   If a detail can change the meaning or appropriate action, it must be included in the intent.
    -   Use consistent terminology throughout.
    |Weak intent|Strong Intent|Notes|
    |-----------|-------------|-----|
    |Requesting for an insurance quotation|Requesting for a car insurance quotation|If a company offers multiple insurances, and the associated workflow is specifically designed for car insurance, the intent must include car. Without this critical detail, an email requesting a different kind of insurance might incorrectly match the insurance quotation intent, leading to a failed or inappropriate workflow.|
    |User requesting for money for house|User requesting for a home loan|Requesting for money is extremely broad. An email like "I gave you money last week, give me my money back" \(a request for repayment\) could incorrectly match this vague intent, even though it's not a home loan request. Including home loan as a critical detail clarifies the specific financial transaction.|

-   Differentiate between action requests and informational queries:

    -   Clearly define whether an intent is for executing an action or for providing information.
    -   This helps prevent the system from taking an action when only information is sought, or vice versa.
    |User email|Intent type|Note|
    |----------|-----------|----|
    |"My team needs writing software installed on our new machines. Please arrange this.|Action request intent|This email clearly asks for an action to be performed \(software installation\). An intent configured as "User requesting installation of Adobe Creative Suite" would correctly match, triggering a workflow to provision and install the software.|
    |I need to install writing software on my personal device for a project. Can you tell me how to do it?|Informational query intent|The user is not asking for the system to perform the installation, but rather for guidance or instructions. If only the action request intent existed, it might incorrectly trigger an installation workflow, or fail to provide the user with the requested information. A separate intent for user asking for instructions on how to install writing software would correctly match and provide a link to a knowledge base article or a step by step guide.|

-   Help the LLM – Don't Make It Guess:
    -   The overarching principle is to make intents as clear and unambiguous as possible to guide the LLM effectively.
    -   The system is a framework; its effectiveness depends on how wisely intents are configured.

For more general guidelines, see [General guidelines for creating AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=gg-creating-aia&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Important Considerations

It’s recommended not to configure workflows to produce final artifacts directly. Instead, workflows should create drafts or intermediate artifacts that require human review and confirmation.

-   Target Record for drafting and email: If using the email drafting capability, a target record must be attached to the email by the time the agent workflow triggers. Without a target record, generated email drafts can't be access.
-   Order of Execution: When enabling the agentic workflow either via Inbound Action or Inbound Email Trigger, consider its order relative to existing inbound actions. The default order 999 places it last to avoid interfering with other processes, but this can be adjusted.
-   Human Oversight: The system aims to remove bottlenecks and increase efficiency, but it doesn’t eliminate the need for human involvement. It's designed to augment, not fully replace, human agents.

