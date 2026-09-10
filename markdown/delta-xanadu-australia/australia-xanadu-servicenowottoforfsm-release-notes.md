---
title: Combined ServiceNow Otto for FSM release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for ServiceNow Otto for FSM from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-servicenowottoforfsm-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Otto for FSM release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for ServiceNow Otto for FSM from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Otto for FSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Otto for FSM to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for ServiceNow Otto for FSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=yokohama&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Custom template and custom prompt support](https://www.servicenow.com/docs/access?context=customize-a-skill&family=yokohama&ft:locale=en-US)**

As an admin, you can clone the KB generation skill and customize the input fields. You can also clone the Work order task summarization skill, then access the skill in the Now Assist skill kit, and update the prompts.


</td></tr><tr><td>

Zurich

</td><td>

-   **[AI agent: Parts Manager](https://www.servicenow.com/docs/access?context=fsm-ai-agent-use-cases&family=zurich&ft:locale=en-US)**

Track and validate parts usage when closing work order tasks. The Parts Manager AI agent analyzes activity notes to update parts statuses and automatically adjusts inventory when tasks are closed. The AI agent is available through the Now Assist panel on platform and through the ServiceNow Agent mobile app.

-   **[AI agent: Create Work Order from image](https://www.servicenow.com/docs/access?context=fsm-ai-agent-use-cases&family=zurich&ft:locale=en-US)**

Create work orders by uploading photos of equipment issues. The AI agent extracts relevant information from the image to populate work order fields.

-   **[Primary action button for Now Assist Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-fsm&family=zurich&ft:locale=en-US)**

Access Now Assist Virtual Agent from a primary action button in the ServiceNow Agent mobile app navigation bar. Administrators can configure this button to launch Now Assist Virtual Agent or another global function.

-   **[Voice-to-text input in Now Assist Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-fsm&family=zurich&ft:locale=en-US)**

Use voice input when interacting with Now Assist Virtual Agent in the ServiceNow Agent mobile app. Tap the microphone icon to dictate messages instead of typing.


</td></tr><tr><td>

Australia

</td><td>

-   **[AI agent: Parts Manager](https://www.servicenow.com/docs/access?context=fsm-ai-agent-parts-manager&family=australia&ft:locale=en-US)**

Track and validate parts usage when closing work order tasks. The Parts Manager AI agent interprets activity notes to update parts statuses and automatically adjusts inventory when tasks are closed. The AI agent is available through the Now Assist panel on platform and through the ServiceNow Agent mobile app.

-   **[AI agent: Create Work Order from image](https://www.servicenow.com/docs/access?context=fsm-ai-agent-create-work-order-image&family=australia&ft:locale=en-US)**

Create work orders by uploading photos of equipment issues. The AI agent extracts relevant information from the image to populate work order fields. A cancel option is available when selecting photos from the camera or photo library.

-   **[Voice-to-text input in Now Assist Virtual Agent](https://www.servicenow.com/docs/access?context=fsm-nava-voice-to-text&family=australia&ft:locale=en-US)**

Use voice input when interacting with Now Assist Virtual Agent in the ServiceNow Agent mobile app. Tap the microphone icon to dictate messages instead of typing.

-   **[New third-party AI model provider options available for all AI applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

Google Gemini and AWS Claude are available for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing ServiceNow Otto for FSM features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&family=yokohama&ft:locale=en-US)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Zurich

</td><td>

-   **[AI visual indicators](https://www.servicenow.com/docs/access?context=now-assist-fsm&family=zurich&ft:locale=en-US)**

Consistent gradient styles indicate when AI is assisting or augmenting an experience. Gradients appear across AI-powered features in Workspace, UI16, and mobile interfaces. Gradients subtly animate during AI processing and return to a static state when complete.

-   **[Updated icons in Now Assist Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-fsm&family=zurich&ft:locale=en-US)**

The Now Assist Virtual Agent interface includes updated icons for web search, photo upload, and microphone functions.


 -   **[Create Work Order AI agent performance improvements](https://www.servicenow.com/docs/access?context=fsm-ai-agent-use-cases&family=zurich&ft:locale=en-US)**

The Create Work Order AI agent was optimized to reduce latency and improve response times. Inter-agent communication was streamlined to minimize redundant processing during work order creation.


</td></tr><tr><td>

Australia

</td><td>

-   **[Primary action button for Now Assist Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-fsm&family=australia&ft:locale=en-US)**

Access Now Assist Virtual Agent from a primary action button in the ServiceNow Agent mobile app navigation bar. Administrators can configure this button to launch Now Assist Virtual Agent or another global function. When configured for Virtual Agent, tapping the button opens Now Assist without additional navigation steps.

-   **[AI visual indicators](https://www.servicenow.com/docs/access?context=now-assist-fsm&family=australia&ft:locale=en-US)**

Consistent gradient styles indicate when AI is assisting or augmenting an experience. Gradients appear across AI-powered features in Workspace, UI16, and mobile interfaces. Gradients subtly animate during AI processing and return to a static state when complete.

-   **[Updated icons in Now Assist Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-fsm&family=australia&ft:locale=en-US)**

The Now Assist Virtual Agent interface includes updated icons for web search, photo upload, and microphone functions.


 -   **[Create Work Order AI agent performance improvements](https://www.servicenow.com/docs/access?context=fsm-ai-agent-create-work-order&family=australia&ft:locale=en-US)**

The Create Work Order AI agent was optimized to reduce latency and improve response times. Inter-agent communication was streamlined to minimize redundant processing during work order creation.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some ServiceNow Otto for FSM features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some ServiceNow Otto for FSM features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate ServiceNow Otto for FSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Now Assist features are available with activation of the ServiceNow Otto for FSM plugin. For more information, see [Install plugins for ServiceNow Otto](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Now Assist features are available with activation of the ServiceNow Otto for FSM plugin. For more information, see [Install plugins for ServiceNow Otto](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow Otto for FSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Additional requirements**

The ServiceNow Otto for FSM application requires Field Service Management.


</td></tr><tr><td>

Australia

</td><td>

-   **Additional requirements**

The ServiceNow Otto for FSM application requires Field Service Management.


</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ServiceNow Otto for FSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for ServiceNow Otto for FSM, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ServiceNow Otto for FSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ServiceNow Otto for FSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   Track and validate parts usage during work order task closure with the Parts Manager AI agent.
-   Create work orders from images by uploading photos of equipment issues through the Now Assist panel or ServiceNow Agent mobile app.
-   Access Now Assist Virtual Agent from a primary action button in the mobile app navigation bar.
-   Use voice-to-text input when interacting with Now Assist Virtual Agent in the ServiceNow Agent mobile app.
-   Enhance your productivity with the Create Work Order AI agent, which allows users to initiate work orders using AI to process descriptions from text.

 See [\[Placeholder link text to key bundle-fsm.now-assist-fsm\]](https://www.servicenow.com/docs/access?context=now-assist-fsm&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Track and validate parts usage during work order task closure with the Parts Manager AI agent.
-   Create work orders from images by uploading photos of equipment issues through the Now Assist panel or ServiceNow Agent mobile app.
-   Access Now Assist Virtual Agent from a primary action button in the mobile app navigation bar.
-   Use voice-to-text input when interacting with Now Assist Virtual Agent in the ServiceNow Agent mobile app.
-   Experience updated visual indicators with consistent AI gradients across platform, workspace, and mobile interfaces.

 See [\[Placeholder link text to key bundle-fsm.now-assist-fsm\]](https://www.servicenow.com/docs/access?context=now-assist-fsm&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

