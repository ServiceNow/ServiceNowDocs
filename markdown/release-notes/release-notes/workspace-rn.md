---
title: Workspace release notes
description: The ServiceNow Workspace application provides agents, case manager, help desk professionals, and managers with tools to answer customer questions and resolve customer problems. Workspace was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
---

# Workspace release notes

The ServiceNow® Workspace application provides agents, case manager, help desk professionals, and managers with tools to answer customer questions and resolve customer problems. Workspace was enhanced and updated in the Xanadu release.

## Workspace highlights for the Xanadu release

-   Add email addresses to recipient fields with more flexibility, including the ability to use international characters, edit email recipient pills, and view concise error messages for invalid or blocked addresses.
-   Categorize and filter records in the Activity Stream.
-   Help users access relevant reference search results by applying pre-filtered and removable query parameters to reference lists.

See [Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for more information.

## New in the Xanadu release

-   **International characters supported in email addresses**

    Enter international characters for email addresses without running into errors.

    Enable international characters for your users according to RFC6530 standards or disable them by changing a system property and performing additional configurations.

-   **[Email client plugin system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Ensure your agents leverage the latest functionality in the email client by using updated plugin \(**glide.ui.email.composer.enabled\_plugins**\) and toolbar \(**glide.ui.email.composer.toolbar**\) system properties offered by default for Tiny MCE v6.

-   **[Tags for Activity Stream records](https://www.servicenow.com/docs/access?context=tags-activity-stream-agent&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    Use tags to categorize and filter records shown in the Activity Stream.

    As admins, you can enable, add, customize, and edit tags for your users' Activity Stream records.

-   **Reference searches with queries**

    Help users access relevant reference search results by applying pre-filtered and removable query parameters to reference lists. These query parameters act as an addition to fixed queries that cannot be removed by end users.

-   **Client scripts for field decorators**

    Add field decorators to field types using client scripts.

-   **Pre-filter records on the multi-record associator**

    Pre-filter records with typeahead on the multi-record associator using scripts.

-   **[Use a keyboard shortcut to insert response templates](https://www.servicenow.com/docs/access?context=add-response-templates-shortcut&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    Enter the keyboard shortcut `/r` and a keyword to insert a response template directly into an email body.

-   **[Configure response templates for email composer](https://www.servicenow.com/docs/access?context=configure-response-templates&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    You can enable or disable response templates for agents with a system property.


## UI changes

-   **[Show and hide the email header](https://www.servicenow.com/docs/access?context=compose-email&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    Collapse and expand all recipient fields in the email header by selecting the chevron icon \(![Chevron icon](../../administer/workspace/image/x-chevron-icon.png)\).

-   **[Edit email addresses](https://www.servicenow.com/docs/access?context=drag-and-drop-recipients-in-to-cc-and-bcc-email-fields&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    Edit an email address directly from the email address' pill instead of removing the email address and reentering it.

-   **[Invalid email address alerts](https://www.servicenow.com/docs/access?context=drag-and-drop-recipients-in-to-cc-and-bcc-email-fields&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    When you enter an invalid email address, an exclamation icon \(![Invalid email icon](../image/icon-invalid-email.png)\) appears within the email address' pill and the **Send email** button is inactive.

    When you enter a blocked email address, a blocked icon \(![Blocked email icon](../image/icon-blocked-email.png)\) appears within the email address' pill and the **Send email** button is inactive.

    Once you enter more than one invalid email address, you receive a single alert as a list of invalid and blocked email addresses.

-   **[Manage email drafts from the full email composer](https://www.servicenow.com/docs/access?context=review-draft-emails&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    Use the **Manage drafts** button in the full email composer to view, edit, and delete drafts.

-   **[Manage email drafts from the mini email composer](https://www.servicenow.com/docs/access?context=review-email-drafts-from-the-mini-email-composer&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    Manage email drafts from the mini email composer by selecting the **View drafts** icon \(![Drafts icon](../../administer/workspace/image/x-mini-drafts-icon.png)\) in the email footer and an action from the menu that opens.

-   **[Add email templates, response templates, and quick messages from the mini email composer](https://www.servicenow.com/docs/access?context=compose-emails-with-email-templates&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    Add email templates, response templates, and quick messages from the mini email composer with the **Apply templates** icon \(![Apply templates icon](../image/x-apply-templates-icon.png)\) in the email footer.

-   **Date and time selection**

    The calendar for selecting a month and year appears as a list with a text box for entering a time.

-   **Back to Group button for list experiences**

    The **Back to Group** button navigates you back to the previous grouped list.


## Activation information

Workspace is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[ServiceNow AI Platform user interface release notes](now-platform-ui-rn-landing.md)

