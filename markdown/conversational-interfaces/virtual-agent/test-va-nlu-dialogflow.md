---
title: Test Virtual Agent with Google Dialogflow ES NLU in Virtual Agent Designer
description: Test topic discovery with Google Dialogflow and Virtual Agent in the Virtual Agent Designer interface.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Google Dialogflow ES as the NLU provider for Virtual Agent, Configure NLU in Virtual Agent, Configure, Virtual Agent, Conversational Interfaces]
---

# Test Virtual Agent with Google Dialogflow ES NLU in Virtual Agent Designer

Test topic discovery with Google Dialogflow and Virtual Agent in the Virtual Agent Designer interface.

## Before you begin

Check the following:

-   Ensure that your Google Dialogflow agent \(model\) is published as a version with the most recent changes.

    For more information, see [Versions and environments](https://cloud.google.com/dialogflow/es/docs/agents-versions) in the Google Dialogflow documentation.

-   Ensure that at least one topic is mapped to an existing Google Dialogflow agent \(model\) and intent.

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  In the Topics page, click **Test Active Topics**.

3.  Type an utterance that should trigger the Google Dialogflow intent that is mapped to the topic.

4.  To test entity slot-filling, do the following:

    1.  On the **Flow** tab, add a Text user input node.

    2.  Select an entity for the **NLU entity** field.

    Ensure that the entity you select is configured in your Google Dialogflow ES agent. When a matching utterance is entered in the Test this topic window, the topic should be triggered, and the entity should slot-fill automatically.


**Parent Topic:**[Configure Google Dialogflow ES as the NLU provider for Virtual Agent](../concept/configure-dialogflow-es-integration.md)

**Previous topic:**[Activate the Google Dialogflow ES service and enable it in your instance](activate-ggl-df-es-service.md)

**Next topic:**[Enhanced natural language handling of user inputs in NLU topic discovery](../concept/natural-language-user-response-handling.md)

