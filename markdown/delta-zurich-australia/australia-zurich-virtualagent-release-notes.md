---
title: Combined Virtual Agent release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Virtual Agent from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-virtualagent-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Virtual Agent release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Virtual Agent from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Virtual Agent release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Virtual Agent to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Virtual Agent.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&family=zurich&ft:locale=en-US)**

Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience. Assistant Designer is comprised of three main areas: Assistants, Asset library \(previously Virtual Agent Designer\), and Analytics.

-   **[Conversational settings](https://www.servicenow.com/docs/access?context=asset-lib-conv-settings&family=zurich&ft:locale=en-US)Conversational settings**

Manage the settings for an asset directly from the Asset library page.


</td></tr><tr><td>

Australia

</td><td>

-   **[Assign search sources](https://www.servicenow.com/docs/access?context=add-info-sources-assistant&family=australia&ft:locale=en-US)**

For premium chat, catalog items have improved fluidity; however, some of them are no longer conversational. They’ll open in a catalog form instead. This applies to Now Assist in Virtual Agent assistants and Now Assist panel – Platform assistant.

-   **[Select a display experience](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&family=australia&ft:locale=en-US)**
    -   If your instance is eligible, you can opt into the premium chat experience. ServiceNow performs a set of readiness checks to see if your instance is eligible for premium chat. Premium chat is a contextual chat experience that appears throughout the platform, adapting its behavior and interface based on where users are and what they're doing.
    -   An alert is shown when the instance is eligible for premium chat or when there is a possible delay for premium chat to appear as an option on your instance.
    -   When editing the display experience of an existing portal or mobile widget, chat experience options depend on the existing configuration.
    -   For channels, select channels from the **Add channels** drop-down list that integrate with the assistant.
    -   For Microsoft Teams, edit the channel to toggle between standard and premium chat.
-   **[Display assistant on Platform or ServiceNow Studio](https://www.servicenow.com/docs/access?context=display-nap-assistant&family=australia&ft:locale=en-US)**

An alert is shown when the instance is eligible for premium chat or when there is a possible delay for premium chat to appear as an option on your instance.

-   **[Brand and personalize an assistant](https://www.servicenow.com/docs/access?context=brand-assistant&family=australia&ft:locale=en-US)**

Customize an assistant’s tone, response length, and persona in the **Personalization** section when branding your assistant. By default, personalization is hidden.To enable personalization, set the appropriate values in the **sn\_nowassist\_va.assistant\_personalization** system property. For more information, see [ServiceNow Otto for Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&family=australia&ft:locale=en-US).

-   **[Enable additional chat features](https://www.servicenow.com/docs/access?context=additional-chat-features&family=australia&ft:locale=en-US)**

For Now Assist in Virtual Agent assistants, voice input is available for premium chat.For Now Assist panel – Platform assistant, voice input is available for standard, enhanced, and premium chat.

-   **[Manage chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&family=australia&ft:locale=en-US)**

For premium chat, you can select a topic for fallback options.For premium messages, select the default greeting message, static greeting message, or select a custom topic. The static greeting message allows you to customize message.For premium chat, your premium messages and premium fallbacks are pre-filled with your legacy messages and legacy fallbacks.

-   **[Edit a chat assistant](https://www.servicenow.com/docs/access?context=edit-assistant&family=australia&ft:locale=en-US)**

View **All assets** to see the assets that are assigned to an assistant.There is no limit to the number of assets that can be promoted.If an active asset is promoted, and later is set to inactive, the asset is not shown in the **Discoverable**, **Visible**, and **Promoted** lists.

-   **[ServiceNow Otto for Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&family=australia&ft:locale=en-US)**

Use the **sn\_nowassist\_va.assistant\_personalization** system property to show or hide chat personalization when branding an assistant. Personalization determines the tone of the assistant, response length, and persona.

-   **[Post-chat surveys](https://www.servicenow.com/docs/access?context=nava-integrated-chat&family=australia&ft:locale=en-US)**

Collect user feedback in premium chats through post-chat surveys that trigger on agent task completion instead of waiting for a chat-end event. When an agent completes a task in an agentic flow, the survey can surface based on a configured probability, enabling you to gather insights that were previously unavailable.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Virtual Agent features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Preferences](https://www.servicenow.com/docs/access?context=set-up-preferences-next-experience&family=zurich&ft:locale=en-US)**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Assistant Designer Asset library](https://www.servicenow.com/docs/access?context=vad-topics-page&family=zurich&ft:locale=en-US)**
    -   Tabs have replaced pills in the Virtual Agent Designer list view.
    -   Hover over the tooltip icon \(\[Omitted image "image.i-tooltip"\] Alt text:\) to see information about the assistant you have selected from the drop-down menu.
    -   Use the new **AI agents** and **Agentic workflows** tabs to select from the types of topics on the home page, along with **Topics**, **Subflows**, **Actions**, and **Custom skills**.
-   **Virtual Agent Designer [Table bot response control](https://www.servicenow.com/docs/access?context=table-bot-response&family=zurich&ft:locale=en-US)**

Slide the new Show links for each record toggle switch to activate links for each record in the output in your Virtual Agent conversation.


 -   **[Test assistant options](https://www.servicenow.com/docs/access?context=test-llm-topics&family=zurich&ft:locale=en-US)**

The **Test** button in the Virtual Agent Designer canvas directly opens up the chat widget.


</td></tr><tr><td>

Australia

</td><td>

-   **[Updated Otto processing animation](https://www.servicenow.com/docs/access?context=nava-integrated-chat&family=australia&ft:locale=en-US)**

View an updated Otto processing animation.

-   **[Assign Model Context Protocol \(MCP\) servers to an assistant](https://www.servicenow.com/docs/access?context=assign-mcp-servers&family=australia&ft:locale=en-US)**

Role-based configuration is no longer stored or managed within Assistant Designer.


 -   **[Upload files improvements](https://www.servicenow.com/docs/access?context=upload-documents-na-va&family=australia&ft:locale=en-US)**

Upload up to 10 files or 50 MB for the following file types: PDF native, PDF OCR, Word, PPTX, Excel, CSV, TXT, JPEG, PNG for premium chat in ServiceNow Otto for Virtual Agent and Otto panel.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Virtual Agent features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Virtual Agent features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Starting with the Zurich release, [Sensitive Data Handler](https://www.servicenow.com/docs/access?context=ac-sensitive-data-overview&family=zurich&ft:locale=en-US) and Sensitive Data Masking capability are being prepared for future deprecation. They will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Install the Data Privacy application as a replacement. For more information, see [Data Privacy](https://www.servicenow.com/docs/access?context=data-privacy-landing&family=zurich&ft:locale=en-US).

-   Starting with the Zurich release, Microsoft LUIS is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.


</td></tr><tr><td>

Australia

</td><td>

-   Starting with the September 2026 release, Now LLM Service is being prepared for future deprecation. The Now LLM Service is no longer the default model provider for new or inactive AI assets, and it is no longer selected by default in AI Control Tower. A third-party LLM is now selected by default for AI assets, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Virtual Agent.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Activation information**

Virtual Agent is a ServiceNow AI Platform feature that is active by default.


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Virtual Agent is a ServiceNow AI Platform feature that is active by default.


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Virtual Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Virtual Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Virtual Agent, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Virtual Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Virtual Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

[Zurich Patch 12](https://www.servicenow.com/docs/access?context=zurich-patch-12&family=zurich&ft:locale=en-US)

-   ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Virtual Agent and ServiceNow Otto panel. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

 [Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience.
-   [Assistant Designer Asset library](https://www.servicenow.com/docs/access?context=vad-topics-page&family=zurich&ft:locale=en-US):
    -   View an updated UI for Virtual Agent Designer topics in the new Assistant Designer Asset library page.
    -   Navigate between Assistants, Asset library, and Analytics tabs in the Assistant Designer UI.
    -   Disconnect an LLM Assistant from a given asset with the Actions on Row icon \[Omitted image "image.kebab-menu"\] Alt text:in the Asset library.
    -   See descriptions of each LLM asset type when selecting **Create asset** in the Asset library.
    -   Read a tooltip that appears when you edit an LLM assistant under the Assistans tab and try to promote more than 6 topics associated with an LLM assistant.

 [Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Google Workspace chat now works with the ServiceNow® conversational interface features, including Virtual Agent, Natural Language Understanding \(NLU\), Notifications, and live agents.
-   Start the create flow for all supported conversational assets directly from Virtual Agent Designer.

 See [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 6](https://www.servicenow.com/docs/access?context=australia-patch-6&family=australia&ft:locale=en-US)

-   Embed the enhanced chat widget on third-party websites.

 [Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)

-   ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Virtual Agent and ServiceNow Otto panel. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

 [Australia Patch 4](https://www.servicenow.com/docs/access?context=australia-patch-4&family=australia&ft:locale=en-US)

-   Prompts help users ask better questions and get more accurate answers. Admins can turn prompt library on or off and further configure the default recommended prompts for users.

 See [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

