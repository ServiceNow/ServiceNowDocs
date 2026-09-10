---
title: ServiceNow Otto for FSM release notes
description: The ServiceNow ServiceNow Otto for FSM application brings generative AI to Field Service Management. ServiceNow Otto for FSM was enhanced and updated in the Zurich release.The ServiceNow ServiceNow Otto for FSM application brings generative AI to Field Service Management. ServiceNow Otto for FSM was enhanced and updated in the Zurich release.The ServiceNow ServiceNow Otto for FSM application brings generative AI to Field Service Management. ServiceNow Otto for FSM was enhanced and updated in the Zurich release.The ServiceNow ServiceNow Otto for FSM application brings generative AI to Field Service Management. ServiceNow Otto for FSM was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# ServiceNow Otto for FSM release notes

The ServiceNow® ServiceNow Otto for FSM application brings generative AI to Field Service Management. ServiceNow Otto for FSM was enhanced and updated in the Zurich release.

## About ServiceNow Otto for FSM

-   Track and validate parts usage during work order task closure with the Parts Manager AI agent.
-   Create work orders from images by uploading photos of equipment issues through the Now Assist panel or ServiceNow Agent mobile app.
-   Access Now Assist Virtual Agent from a primary action button in the mobile app navigation bar.
-   Use voice-to-text input when interacting with Now Assist Virtual Agent in the ServiceNow Agent mobile app.
-   Enhance your productivity with the Create Work Order AI agent, which allows users to initiate work orders using AI to process descriptions from text.

See  for more information.

## Activation and other requirements

**Important:** ServiceNow Otto for FSM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Now Assist features are available with activation of the ServiceNow Otto for FSM plugin. For more information, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

-   **Additional requirements**

    The ServiceNow Otto for FSM application requires Field Service Management.


**Parent Topic:**[Field Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/field-service-management-rn.md)

## March 2026

The ServiceNow® ServiceNow Otto for FSM application brings generative AI to Field Service Management. ServiceNow Otto for FSM was enhanced and updated in the Zurich release.

### What's new

-   **AI agent: Parts Manager**

    Track and validate parts usage when closing work order tasks. The Parts Manager AI agent analyzes activity notes to update parts statuses and automatically adjusts inventory when tasks are closed. The AI agent is available through the Now Assist panel on platform and through the ServiceNow Agent mobile app.

-   **AI agent: Create Work Order from image**

    Create work orders by uploading photos of equipment issues. The AI agent extracts relevant information from the image to populate work order fields.

-   **Primary action button for Now Assist Virtual Agent**

    Access Now Assist Virtual Agent from a primary action button in the ServiceNow Agent mobile app navigation bar. Administrators can configure this button to launch Now Assist Virtual Agent or another global function.

-   **Voice-to-text input in Now Assist Virtual Agent**

    Use voice input when interacting with Now Assist Virtual Agent in the ServiceNow Agent mobile app. Tap the microphone icon to dictate messages instead of typing.


### What's changed

-   **AI visual indicators**

    Consistent gradient styles indicate when AI is assisting or augmenting an experience. Gradients appear across AI-powered features in Workspace, UI16, and mobile interfaces. Gradients subtly animate during AI processing and return to a static state when complete.

-   **Updated icons in Now Assist Virtual Agent**

    The Now Assist Virtual Agent interface includes updated icons for web search, photo upload, and microphone functions.


-   **Create Work Order AI agent performance improvements**

    The Create Work Order AI agent was optimized to reduce latency and improve response times. Inter-agent communication was streamlined to minimize redundant processing during work order creation.


## December 2025

The ServiceNow® ServiceNow Otto for FSM application brings generative AI to Field Service Management. ServiceNow Otto for FSM was enhanced and updated in the Zurich release.

### What's new

-   **AI agent: Create Work Order**

    You can leverage AI to create work orders from a written description of the issue. The Create Work Order AI agent is available through the Now Assist panel on platform and through the ServiceNow Agent mobile app.


## Zurich

The ServiceNow® ServiceNow Otto for FSM application brings generative AI to Field Service Management. ServiceNow Otto for FSM was enhanced and updated in the Zurich release.

### What's new

-   **[New third-party AI model provider options available for all AI applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Google Gemini and AWS Claude are available for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.

-   **[Custom template and custom prompt support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/field-service-management/customize-a-skill.md)**

    As an admin, you can clone the KB generation skill and customize the input fields. You can also clone the Work order task summarization skill, then access the skill in the Now Assist skill kit, and update the prompts.


### What's changed

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


-   **[Removed prompt headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/field-service-management/cust-now-assist-fsm-wot-summarization-skill.md)**

    The prompt headers have been removed from the work order summarization skill to support third-party large language models. You can now customize prompts via a hyperlink to the Now Assist skill.


