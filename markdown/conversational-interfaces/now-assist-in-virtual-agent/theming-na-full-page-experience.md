---
title: Theming for Now Assist in Virtual Agent enhanced chat
description: You can customize the look and feel of the Now Assist in Virtual Agent enhanced chat experience in your ServiceNow portal by updating the relevant Cascading Style Sheet \(CSS\) variables.
locale: en-US
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Theming for Now Assist in Virtual Agent enhanced chat

You can customize the look and feel of the Now Assist in Virtual Agent enhanced chat experience in your ServiceNow portal by updating the relevant Cascading Style Sheet \(CSS\) variables.

As a Virtual Agent admin or admin, you can customize the default enhanced chat theming variables. Information on how to customize theming can be found in [Create a portal theme](https://www.servicenow.com/docs/access?context=c_CustomCSS&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US). Edit these variables in the following table within the CSS variables field \(sp\_theme\) record. You can also configure these variables with a CSS Include associated with a portal's theme.

**Note:**

The chat header logo is shared between standard and enhanced chat, and it’s determined by the selected standard chat branding profile. You can’t configure a separate chat header logo for each experience. Updating the chat header logo in one experience updates it for the other. To view the branding profile, navigate to **Assistant Designer** &gt; **Assistants** &gt; **Branding**.

For the variables, `nass` refers to enhanced chat.

For more information about enhanced chat, see [Enhanced chat](../concept/nava-enhanced-chat.md).

<table id="table_ok3_wwm_bdc"><thead><tr><th>

Variable

</th><th>

Description

</th><th>

Default Values

</th></tr></thead><tbody><tr><td>

$now-sp-nass-agent-bubble-font-color

</td><td>

Agent text message font color.

</td><td>

$text-color

</td></tr><tr><td>

$now-sp-nass-chat-user-message-bubble-bg-color

</td><td>

User text message bubble background color.

</td><td>

$brand-primary-lightest

</td></tr><tr><td>

$now-sp-nass-user-bubble-font-color

</td><td>

User text message font color.

</td><td>

$text-color

</td></tr><tr><td>

$now-sp-nass-timestamp-color

</td><td>

Timestamp text color.

</td><td>

$text-muted

</td></tr><tr><td>

$now-sp-nass-secondary-text-color

</td><td>

Secondary text color for example for Active.

</td><td>

$gray-dark

</td></tr><tr><td>

$now-sp-nass-system-msg-text-color

</td><td>

System message text color.

</td><td>

$text-muted

</td></tr><tr><td>

$now-sp-nass-base-input-field-placeholder-and-highlight-text-color

</td><td>

Input text color and with .45 opacity for placeholder.

</td><td>

$text-color

</td></tr><tr><td>

$now-sp-nass-base-link-color

</td><td>

Link color.

</td><td>

$brand-primary

</td></tr><tr><td>

$now-sp-nass-color-secondary\_2

</td><td>

Now Design System secondary-2 color.

</td><td>

$brand-primary-darker

</td></tr><tr><td>

$now-sp-nass-modeless-dialog-header-bg-color

</td><td>

Background color for primary Now Assist header bar.

</td><td>

\#ffffff

</td></tr><tr><td>

$now-sp-nass-modeless-dialog-header-text-color

</td><td>

Text color for primary Now Assist header.

</td><td>

$text-color

</td></tr><tr><td>

$now-sp-nass-base-toolbar-labels-and-icons-color

</td><td>

Left-panel tool bar icons.

</td><td>

$gray-light

</td></tr><tr><td>

$now-sp-nass-toolbar-icons-color--hover

</td><td>

Left-panel tool bar icons in hover state.

</td><td>

$gray-dark

</td></tr><tr><td>

$now-sp-nass-toolbar-icons-color--active

</td><td>

Left-panel tool bar icons in active state.

</td><td>

$text-color

</td></tr><tr><td>

$now-sp-nass-toolbar-icons-fullscreen-mode-color

</td><td>

Left-panel tool bar icons in full-screen mode.

</td><td>

darken \($brand-primary-darker, 15%\)

</td></tr><tr><td>

$now-sp-nass-toolbar-icons-fullscreen-mode-color--active

</td><td>

Left-panel tool bar icons in full-screen mode for active state.

</td><td>

$brand-primary-darker

</td></tr><tr><td>

$now-sp-nass-window-control-icons-color

</td><td>

Window controls icons.

</td><td>

$text-muted

</td></tr><tr><td>

$now-sp-nass-window-control-icons-color--hover

</td><td>

Window controls icons in hover state.

</td><td>

$text-color

</td></tr><tr><td>

$now-sp-nass-window-control-icons-color--active

</td><td>

Window controls icons in active state.

</td><td>

$text-color

</td></tr><tr><td>

$now-sp-nass-feedback-and-search-result-panel-color

</td><td>

Feedback panel and search result icon.

</td><td>

$text-muted

</td></tr><tr><td>

$now-sp-nass-feedback-and-search-result-panel-selected-color

</td><td>

Selected icon in feedback panel.

</td><td>

$text-muted

</td></tr><tr><td>

$now-sp-nass-action-and-kb-citation-color

</td><td>

Action and Knowledge Base link color

</td><td>

$link-color

</td></tr><tr><td>

$now-sp-nass-color-primary-0

</td><td>

Primary-0 for pills/primary buttons.

</td><td>

$brand-primary-lightest

</td></tr><tr><td>

$now-sp-nass-color-primary-2

</td><td>

Primary-2 for pills/primary buttons in active state.

</td><td>

$brand-primary-darker

</td></tr><tr><td>

$now-sp-nass-button-primary-bg-color

</td><td>

Submit button in choice picker control.

</td><td>

$btn-primary-bg

</td></tr><tr><td>

$now-sp-nass-button-primary-bg-active-color

</td><td>

Button primary active background color.

</td><td>

$btn-primary-bg

</td></tr><tr><td>

$now-sp-nass-button-selection-text-color

</td><td>

Now Design System secondary-1 color

</td><td>

$brand-primary

</td></tr><tr><td>

$now-sp-nass-tooltip-bg-color

</td><td>

Tooltip background color for input field icons.

</td><td>

$tooltip-bg

</td></tr><tr><td>

$now-sp-nass-tooltip-text-color

</td><td>

Tooltip text color for input field icons.

</td><td>

$tooltip-color

</td></tr><tr><td>

$now-sp-nass-alert-critical-color

</td><td>

Unread indicator color.

</td><td>

$brand-danger

</td></tr><tr><td>

$now-sp-nass-input-field-icon-color

</td><td>

Icon and attachment icon in the input field

</td><td>

$text-muted

</td></tr><tr><td>

$now-sp-nass-color-alert-moderate-3

</td><td>

Animated loading icon color.

</td><td>

\#4345a6

</td></tr><tr><td>

$now-sp-nass-body-bg

</td><td>

Body primary background color.

</td><td>

\#ffffff

</td></tr><tr><td>

$now-sp-nass-base-highlight-color

</td><td>

Background-color of matched text when searching emojis.

</td><td>

lighten \($warning, 35%\)

</td></tr><tr><td>

$now-sp-nass-color-primary-3

</td><td>

Bare buttons color in active state.

</td><td>

darken \($brand-primary-darker, 15%\)

</td></tr><tr><td>

$now-sp-nass-color-background-primary

</td><td>

Content background color.

</td><td>

\#ffffff

</td></tr><tr><td>

$now-sp-nass-header-panel-bg-color

</td><td>

Header panel background color.

</td><td>

\#ffffff

</td></tr><tr><td>

$now-sp-nass-button-bg-action-color

</td><td>

Image picker select button background color.

</td><td>

$brand-primary

</td></tr><tr><td>

$now-sp-nass-primary-button-action-text-color

</td><td>

Image picker select button color.

</td><td>

$sp-btn-text-color

</td></tr><tr><td>

$now-sp-nass-base-separator-color

</td><td>

Separator.

</td><td>

$border-tertiary

</td></tr><tr><td>

$now-sp-nass-chat-agent-message-bubble-bg-color

</td><td>

Agent message bubble background color.

</td><td>

$gray-light

</td></tr><tr><td>

$now-sp-nass-citation-badge-color

</td><td>

Citation badge color.

</td><td>

$gray-lighter

</td></tr><tr><td>

$now-sp-nass-divider-and-border-tertiary-color

</td><td>

Divider and border color of mid-topic switch in search results.

</td><td>

$border-tertiary

</td></tr><tr><td>

$now-sp-nass-highlight-value-tertiary-info-bg-color

</td><td>

Highlighted info value in the mid-topic card.

</td><td>

$state-info-bg

</td></tr><tr><td>

$now-sp-nass-FAB-icon

</td><td>

Icon imagery that appears on the floating action button.

</td><td>

ai-sparkle-icon

</td></tr><tr><td>

$now-sp-nass-FAB-gradient-color-1

</td><td>

First color of background gradient for chat floating action button icon.

</td><td>

$brand-primary-lighter

</td></tr><tr><td>

$now-sp-nass-FAB-gradient-color-2

</td><td>

Second color of background gradient for chat floating action button icon.

</td><td>

$brand-info

</td></tr><tr><td>

$now-sp-nass-FAB-gradient-hover-color-1

</td><td>

First color of background gradient for chat floating action button icon in hover state.

</td><td>

$brand-primary-darker

</td></tr><tr><td>

$now-sp-nass-FAB-gradient-hover-color-2

</td><td>

Second color of background gradient for chat floating action button icon in hover state.

</td><td>

darken \($brand-info, 10%\)

</td></tr><tr><td>

$now-sp-nass-FAB-gradient-active-color-1

</td><td>

First color of background gradient for chat floating action button icon in active state.

</td><td>

$brand-primary

</td></tr><tr><td>

$now-sp-nass-FAB-gradient-active-color-2

</td><td>

Second color of background gradient for chat floating action button icon in active state.

</td><td>

$brand-info

</td></tr><tr><td>

$now-sp-nass-FAB-icon-size-factor

</td><td>

Handles size of Image within the chat icon.

</td><td>

1

</td></tr></tbody>
</table>