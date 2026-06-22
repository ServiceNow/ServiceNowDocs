---
title: Configure Next Experience accessibility preferences
description: Set up Next Experience accessibility preferences to achieve a UI that's most accessible to you.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/configure-user-experiences/next-experience-accessibility-preferences.html
release: zurich
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [accessibility preferences, next experience accessibility]
breadcrumb: [Preferences, Working in Next Experience, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Configure Next Experience accessibility preferences

Set up Next Experience accessibility preferences to achieve a UI that's most accessible to you.

## Before you begin

Role required: none

## Procedure

1.  Navigate to **User Menu** &gt; **Preferences** &gt; **Accessibility**.

2.  Select the toggle next to each option to turn the preference on or off.

<table id="table_y5b_j2f_jqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[Omitted image "pol-pref-date-time.png"\] Alt text: Show date and time formats.

</td><td>

Displays the date and time format \(yyyy-MM-dd-HH:mm:ss\) next to the form fields ensuring the format remains visible even when the field is in focus. For more information, see [Show date and time formats on forms preference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/show-date-time-formats-forms.md).

</td></tr><tr><td>

\[Omitted image "pol-pref-colors.png"\] Alt text: Replace colors with patterns in charts and graphs.

</td><td>

Adjusts charts and graphs to display with a pattern such as stripes or dashed lines instead of just a color. For more information, see [Replace colors with patterns in charts and graphs preference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/replace-colors-with-patterns.md).

</td></tr><tr><td>

\[Omitted image "pol-pref-shortcuts.png"\] Alt text: Enable special keyboard shortcuts.

</td><td>

Use keyboard shortcuts to quickly perform common actions in the user interface. The keyboard shortcuts that display in the modal are specific to the screen you are viewing. For more information, see [Enable keyboard shortcuts preference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/enable-keyboard-shortcuts-pref.md) and [Next Experience keyboard shortcuts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/next-experience-keyboard-shortcuts.md). **Note:** If you’re working in the Classic Environment, see [Core UI keyboard shortcuts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/r_KeyboardShortcuts.md).

</td></tr><tr><td>

\[Omitted image "pol-pref-no-hover.png"\] Alt text: Show all buttons without the need to hover

</td><td>

Displays all hidden fields, buttons or other UI elements, eliminating the need to hover over them. For more information, see [Show all buttons without the need to hover preference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/show-all-buttons-pref.md).

</td></tr><tr><td>

\[Omitted image "pol-pref-data.png"\] Alt text: Enable data table for charts and graphs.

</td><td>

Shows a table with chart and graph data for easier screen reader access. For more information, see [Enable data table for charts and graphs preference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/enable-data-table-pref.md).

</td></tr><tr><td>

\[Omitted image "pol-pref-reduce-motion.png"\] Alt text: Reduce motion.

</td><td>

Reduces the speed of the animations when switching between screens. This reduction pertains mainly to login animations. For more information, see [Reduce motion preference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/reduce-motion-pref.md).

</td></tr><tr><td>

\[Omitted image "pol-pref-classic-accessibility.png"\] Alt text: Enable accessibility in classic.

</td><td>

Extends keyboard navigation and enables more tab stops in the classic environment so you can tab to icons and buttons in lists, form fields, and cards. This option also presents additional info on forms. For more information, see [Enable accessibility in Classic preference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/enable-accessibility-in-classic-pref.md).**Note:** The classic environment refers to working in lists of records and on record forms directly. You can work in the classic environment with Next Experience active, or with it inactive, which is referred to as Core UI.

</td></tr><tr><td>

\[Omitted image "pol-pref-truncated-text.png"\] Alt text: Enable keyboard focus on truncated text.

</td><td>

Allows keyboard-only users to access truncated text. Truncated text is text that doesn't fit on the screen and is indicated by an ellipsis \[Omitted image "ellipsis-h-fill.png"\] Alt text: Ellipses icon.. When this preference is enabled, keyboard-only users can access the truncated text as they Tab through the focus order, revealing the full text of each tooltip as they navigate the screen. For more information, see [Enable keyboard focus on text that displays tooltip](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/enable-keyboard-focus-pref.md).

</td></tr><tr><td>

\[Omitted image "pol-pref-voice-input.png"\] Alt text: Enable voice input for the Now Assist panel.

</td><td>

Voice input is automatically activated when the Now Assist panel is activated. As of the Zurich Patch 4 release, voice input is configured in [Additional chat features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/now-assist-in-virtual-agent/additional-chat-features.md) and not with this option.

Activates voice-to-text in the Now Assist panel. With this feature, use your voice to access Now Assist skills in the  in any supported language. For more information on this preference, see [Enable voice input for the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/enable-voice-input-pref.md).**Note:** This preference appears only if your system administrator has enabled Now Assist voice input for your instance. For more information, see .

</td></tr><tr><td>

\[Omitted image "pol-pref-auto-dismiss.png"\] Alt text: Do not auto-dismiss page alerts.

</td><td>

Keeps page alerts visible until you acknowledge them. When this preference is turned off, page alerts may disappear after a certain amount of time depending on how the specific page alert is configured. For more information, see [Do not auto-dismiss page alerts preference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/do-not-auto-dismiss-pref.md).**Note:** Critical and warning alerts do not disappear. If focus is applied to the alert, the auto-dismiss feature will not apply.

</td></tr></tbody>
</table>    **Note:** If users have configured operating system-specific settings, such as forced colors or contrast in Windows, those settings are not overridden by Next Experience user preferences or themes. If those OS-specific settings are inactive, color and theme behaviors will revert to those behaviors defined in the Next Experience UI.


