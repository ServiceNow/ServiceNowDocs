---
title: Now Assist for Field Service Management \(FSM\) release notes
description: The ServiceNow Now Assist for FSM application brings generative AI to Field Service Management. Now Assist for FSM was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-03-19"
reading_time_minutes: 4
---

# Now Assist for Field Service Management \(FSM\) release notes

The ServiceNow® Now Assist for FSM application brings generative AI to Field Service Management. Now Assist for FSM was enhanced and updated in the Yokohama release.

## Now Assist for FSM highlights for the Yokohama release

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Clone and customize skills.
-   Edit prompts using the Now Assist skill kit.

Yokohama Patch 3

-   Enable Field Service technicians to access a virtual assistant from the mobile application with Now Assist in Virtual Agent.

-   Use Now Assist in Virtual Agent for mobile to summarize work order tasks.
-   Explore conversational search in the Now Assist panel with results from Knowledge Base articles.

See Now Assist for Field Service Management \(FSM\) for more information.

**Important:** Now Assist for Field Service Management \(FSM\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[New third-party AI model provider options available for all Now Assist applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Custom template and custom prompt support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/customize-a-skill.md)**

    As an admin, you can clone the KB generation skill and customize the input fields. You can also clone the Work order task summarization skill, then access the skill in the Now Assist skill kit, and update the prompts.


-   **[Create an Assistant for Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/activate-virtual-agent-for-field-service-management.md) to do the following:**
    -   Initiate the Now Assist panel from a work order task record or the **My tasks** tab.
    -   Provide technicians with a consistent and intuitive interface for quick and effortless interaction.
    -   Display a summary of work order tasks.
-   **[Use conversational search for technician support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/use-conversational-search-for-technician-support.md) to do the following:**
    -   Enable technicians to ask questions in natural language for quick and clear answers.
    -   Enable technicians to receive accurate and reliable responses sourced exclusively from the Knowledge Base.
    -   Provide technicians with context-aware follow-ups, including related parts or steps, for better support.

## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/aia-security-implementation.md)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[Removed prompt headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/cust-now-assist-fsm-wot-summarization-skill.md)**

    The prompt headers have been removed from the work order summarization skill to support third-party Large Language Models \(LLMs\). You can now customize prompts via a hyperlink to the Now Assist skill.


## Activation information

Now Assist features are available with activation of the Now Assist for FSM plugin. For more information, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

## Additional requirements

The Now Assist for FSM application requires Field Service Management.

## Related ServiceNow applications and features

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/configuring-now-assist.md)**

    Use the Now Assist Admin console to provide you with quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills.md)**

    Use the Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including work order task summarization and Knowledge Base article generation.


**Parent Topic:**[Field Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/field-service-management-rn.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-rn-landing.md)

