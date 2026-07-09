---
title: Combined Workspace release notes for upgrades from Washington DC to Yokohama
description: Consolidated page of all release notes for Workspace from Washington DC to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-washingtondc-yokohama/yokohama-washingtondc-workspace-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Workspace release notes for upgrades from Washington DC to Yokohama

Consolidated page of all release notes for Workspace from Washington DC to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Workspace release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Workspace to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Workspace.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Maximum file size allowed for attachments](https://developer.servicenow.com/dev.do#!/reference/next-experience/washingtondc/now-components/now-record-common-attachments-connected/uib-setup)**

Setting the maximum file size provides storage space for attachments and documents in the workspace.


</td></tr><tr><td>

Xanadu

</td><td>

-   **International characters supported in email addresses**

Enter international characters for email addresses without running into errors.

Enable international characters for your users according to RFC6530 standards or disable them by changing a system property and performing additional configurations.

-   **[Email client plugin system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&family=xanadu&ft:locale=en-US)**

Ensure your agents leverage the latest functionality in the email client by using updated plugin \(**glide.ui.email.composer.enabled\_plugins**\) and toolbar \(**glide.ui.email.composer.toolbar**\) system properties offered by default for Tiny MCE v6.

-   **[Tags for Activity Stream records](https://www.servicenow.com/docs/access?context=tags-activity-stream-agent&family=xanadu&ft:locale=en-US)**

Use tags to categorize and filter records shown in the Activity Stream.

As admins, you can enable, add, customize, and edit tags for your users' Activity Stream records.

-   **Reference searches with queries**

Help users access relevant reference search results by applying pre-filtered and removable query parameters to reference lists. These query parameters act as an addition to fixed queries that cannot be removed by end users.

-   **Client scripts for field decorators**

Add field decorators to field types using client scripts.

-   **Pre-filter records on the multi-record associator**

Pre-filter records with typeahead on the multi-record associator using scripts.

-   **[Use a keyboard shortcut to insert response templates](https://www.servicenow.com/docs/access?context=add-response-templates-shortcut&family=xanadu&ft:locale=en-US)**

Enter the keyboard shortcut `/r` and a keyword to insert a response template directly into an email body.

-   **[Configure response templates for email composer](https://www.servicenow.com/docs/access?context=configure-response-templates&family=xanadu&ft:locale=en-US)**

You can enable or disable response templates for agents with a system property.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Configure keyboard shortcut for response templates](https://www.servicenow.com/docs/access?context=configure-response-templates&family=yokohama&ft:locale=en-US)**

Use a keyboard shortcut to add response templates to journal fields within a form.

-   **[Create collapsible content for email templates](https://www.servicenow.com/docs/access?context=configure-collapsible-email-templates&family=yokohama&ft:locale=en-US)**

Hide email content behind an ellipsis in email templates.

-   **[Configure the email composer in Core UI](https://www.servicenow.com/docs/access?context=enable-next-experience-email-client-core-ui&family=yokohama&ft:locale=en-US)**

Access the latest Workspace features for email composer in the Core UI.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Workspace features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **Record preview in Configurable Workspace**

Select the information icon \(\[Omitted image "image.icon-view-event-rpa"\] Alt text: information icon\) within a field to preview a record before opening it.

Record preview available by using the Form bundle component within the Form component or using the standard record page template.

-   **Encrypt attachments added to a form**

Select module encryption when adding attachments within a form to maintain which roles have access to view the attachments.

-   **[Save email drafts](https://www.servicenow.com/docs/access?context=review-draft-emails&family=washingtondc&ft:locale=en-US)**

The manual **Save** button is no longer available on the email client.

Email drafts save automatically after a number of seconds.

Create a new email draft and view email drafts while saving the current email draft automatically.

System admins disable auto-save or change the time between auto-save refreshes with property **glide.email\_client.auto\_save\_enable**.

-   **[Add email addresses into recipient fields](https://www.servicenow.com/docs/access?context=drag-and-drop-recipients-in-to-cc-and-bcc-email-fields&family=washingtondc&ft:locale=en-US)**

Copy and paste email addresses into the recipient fields in the email client.

-   **[Insert link to knowledge article in email](https://www.servicenow.com/docs/access?context=add-article-agent-assist&family=washingtondc&ft:locale=en-US)**

Use Agent Assist to add a link to a knowledge article in an email to requesters.

-   **[Pop-up dialog for Compose panel](https://developer.servicenow.com/dev.do#!/reference/next-experience/washingtondc/now-components/now-activity-stream-compose-connected/uib-setup)**

Interact with the Compose panel from a pop-up dialog to work with other areas of your workspace form simultaneously.

-   **[Email composer in UIB](https://developer.servicenow.com/dev.do#!/reference/next-experience/washingtondc/now-components/now-email-client-composer-connected/uib-setup)**

Properties added in UIB for Email Composer to configure the **Send Email** button, insert links in emails, control the **Create New Email**, **Discard**, and **View drafts** buttons, and adjust the column layout.

Event added in UIB for Email Composer to maintain the email subject after it's changed.

-   **Supported field types for forms**

Workspace supports the following field types in forms: Integer\_date, XML, Script, Script\_plain, Condition\_string, Slushbucket.

-   **[Declarative actions configuration improvements](https://www.servicenow.com/docs/access?context=declarative-actions-landing&family=washingtondc&ft:locale=en-US)**

Collection of improvements to address declarative actions configuration experience including automatic creation of UXF Form Action and UX Form Action Layout Item records to reduce the number of manual disparate steps required to set up declarative actions, updates to navigation access to declarative actions, and support for icons and more button colors.

-   **[Translations via payload for UXF Client Actions](https://www.servicenow.com/docs/access?context=create-a-new-uxf-client-action-for-forms&family=washingtondc&ft:locale=en-US)**

Translate text defined in your declarative actions payload by wrapping the value in a translate\(\) call with single or double quotes.

-   **Unify actions in form layout**

Any existing layout displays an alert message with a button to unify actions which consolidates form actions into a single list for simplified display adjustments. New layouts are consolidated automatically.


</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Context-based suggestions with @mentions](https://www.servicenow.com/docs/access?context=set-up-at-mentions&family=yokohama&ft:locale=en-US)**

Receive suggestions for users with access to the record when using @ mentions.

-   **[Expand all tiles in the Activity stream](https://www.servicenow.com/docs/access?context=activity-stream-expand-tiles&family=yokohama&ft:locale=en-US)**

Set a user preference to keep all tiles in the Activity stream expanded across cases and user sessions.

-   **Access control security model for the Activity stream**

Data filters and access rules provide role-based access control for viewing and editing tables in the Activity stream.

-   **[Multiple records added from the multi-record associator load in the background](https://www.servicenow.com/docs/access?context=set-up-asynchronous-record-addition&family=yokohama&ft:locale=en-US)**

Work on a record while the multiple records that were selected from the multi-record associator are added in the background.

-   **Attach display text to knowledge base links in the email composer**

Manage your email's appearance by attaching display text to knowledge base links.

-   **Infinite scroll for lists**

Use the Record List bundle to scroll through lists infinitely without pagination.

-   **Live updates for lists**

Use the Record List bundle to view live updates on lists without refreshing the page.

-   **Temporary lists available in the list menu**

Temporarily access personalized lists that are sent to you as links within the My Lists menu.

-   **Filter for hierarchy in condition builder**

The **is within hierarchy** field in the condition builder enables you to filter your list within a hierarchy instead of only direct reports.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Workspace features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Workspace features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Workspace.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Workspace is a ServiceNow AI Platform® feature that is active by default.

</td></tr><tr><td>

Xanadu

</td><td>

Workspace is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Yokohama

</td><td>

Workspace is a ServiceNow AI Platform feature that is active by default.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Workspace we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Workspace we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

Workspace doesn’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge-Chromium or one of the other supported browsers that are listed in [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Workspace, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Keyboard shortcuts](https://www.servicenow.com/docs/access?context=next-experience-keyboard-shortcuts&family=washingtondc&ft:locale=en-US)**

Forty keyboard shortcuts are now available to help you navigate across configurable workspace pages faster and more effectively without a mouse device.

Shortcuts are contextual to the page that you're on and to the operating system that you're using. View the keyboard shortcuts that are available to you on a particular page through the keyboard shortcut modal. You can open the modal by selecting **Keyboard shortcuts** from the Next Experience User Preferences menu, or by using a keyboard shortcut \(**Control + /** for Windows or **Command + /** for macOS\).

This enhancement helps non-mouse and keyboard-only users or users with mobility issues and cognitive impairments to reduce the time required to complete various tasks.

Previously, a limited number of keyboard shortcuts were available when the **Enable special keyboard shortcuts** Next Experience user preference was turned on. Those shortcuts are included in the new keyboard shortcut framework and are accessible via the new modal. See [Configure Next Experience accessibility preferences](https://www.servicenow.com/docs/access?context=next-experience-accessibility-preferences&family=washingtondc&ft:locale=en-US) for additional information.


</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Workspace we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Workspace we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Manage file sizing for documents and attachments.
-   Organize access to attachments by role with module encryption.
-   Streamline workspace navigation with consolidated actions in the navigator, collapsed Activity stream entries with tiles, and updated navigation messages.
-   Get more versatility while working in your workspace with more supported field types, unified actions, and auto-save functionality for emails.

 See [Configurable Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Add email addresses to recipient fields with more flexibility, including the ability to use international characters, edit email recipient pills, and view concise error messages for invalid or blocked addresses.
-   Categorize and filter records in the Activity Stream.
-   Help users access relevant reference search results by applying pre-filtered and removable query parameters to reference lists.

 See [Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Navigate form templates with larger cards, sorting preferences, and favorites.
-   Add collapsible content to email templates and attach a display to knowledge base links.
-   Leverage the latest workspace features for email composer in the Core UI.
-   Use lists that have additional condition builder fields, infinite scroll, live updates, and saved temporary lists.
-   Provide role-based access control for viewing and editing tables in the Activity stream.

 See [Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-washingtondc-yokohama/rn-combined-intro.md)

