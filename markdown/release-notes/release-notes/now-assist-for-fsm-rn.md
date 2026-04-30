---
title: Now Assist for FSM release notes
description: The ServiceNow Now Assist for FSM application brings generative AI to Field Service Management. Now Assist for FSM was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# Now Assist for FSM release notes

The ServiceNow® Now Assist for FSM application brings generative AI to Field Service Management. Now Assist for FSM was enhanced and updated in the Zurich release.

## Now Assist for FSM highlights for the Zurich release

-   Track and validate parts usage during work order task closure with the Parts Manager AI agent.
-   Create work orders from images by uploading photos of equipment issues through the Now Assist panel or ServiceNow Agent mobile app.
-   Access Now Assist Virtual Agent from a primary action button in the mobile app navigation bar.
-   Use voice-to-text input when interacting with Now Assist Virtual Agent in the ServiceNow Agent mobile app.
-   Enhance your productivity with the Create Work Order AI agent, which allows users to initiate work orders using AI to process descriptions from text.

See [Now Assist for Field Service Management \(FSM\)](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US) for more information.

**Important:** Now Assist for FSM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[AI agent: Parts Manager](https://www.servicenow.com/docs/access?context=fsm-ai-agent-use-cases&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    Track and validate parts usage when closing work order tasks. The Parts Manager AI agent analyzes activity notes to update parts statuses and automatically adjusts inventory when tasks are closed. The AI agent is available through the Now Assist panel on platform and through the ServiceNow Agent mobile app.

-   **[AI agent: Create Work Order from image](https://www.servicenow.com/docs/access?context=fsm-ai-agent-use-cases&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    Create work orders by uploading photos of equipment issues. The AI agent extracts relevant information from the image to populate work order fields.

-   **[Primary action button for Now Assist Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    Access Now Assist Virtual Agent from a primary action button in the ServiceNow Agent mobile app navigation bar. Administrators can configure this button to launch Now Assist Virtual Agent or another global function.

-   **[Voice-to-text input in Now Assist Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    Use voice input when interacting with Now Assist Virtual Agent in the ServiceNow Agent mobile app. Tap the microphone icon to dictate messages instead of typing.

-   **[AI agent: Create Work Order](https://www.servicenow.com/docs/access?context=fsm-ai-agent-use-cases&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    You can leverage AI to create work orders from a written description of the issue. The Create Work Order AI agent is available through the Now Assist panel on platform and through the ServiceNow Agent mobile app.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Custom template and custom prompt support](https://www.servicenow.com/docs/access?context=customize-a-skill&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    As an admin, you can clone the KB generation skill and customize the input fields. You can also clone the Work order task summarization skill, then access the skill in the Now Assist skill kit, and update the prompts.


## UI changes

-   **[AI visual indicators](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    Consistent gradient styles indicate when AI is assisting or augmenting an experience. Gradients appear across AI-powered features in Workspace, UI16, and mobile interfaces. Gradients subtly animate during AI processing and return to a static state when complete.

-   **[Updated icons in Now Assist Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    The Now Assist Virtual Agent interface includes updated icons for web search, photo upload, and microphone functions.

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Create Work Order AI agent performance improvements](https://www.servicenow.com/docs/access?context=fsm-ai-agent-use-cases&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    The Create Work Order AI agent was optimized to reduce latency and improve response times. Inter-agent communication was streamlined to minimize redundant processing during work order creation.

-   **[Removed prompt headers](https://www.servicenow.com/docs/access?context=cust-now-assist-fsm-wot-summarization-skill&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    The prompt headers have been removed from the work order summarization skill to support third-party large language models. You can now customize prompts via a hyperlink to the Now Assist skill.


## Activation information

Now Assist features are available with activation of the Now Assist for FSM plugin. For more information, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Additional requirements

The Now Assist for FSM application requires Field Service Management.

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console that provides you with quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including work order task summarization and Knowledge Base article generation.


**Parent Topic:**[Field Service Management release notes](field-service-management-rn.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

