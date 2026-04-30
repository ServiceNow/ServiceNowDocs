---
title: Search feature configuration
description: Understand the configuration of the Search feature in Engagement Messenger to configure the field values.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Engagement Messenger reference, Customer Service Management reference, Customer Service Management]
---

# Search feature configuration

Understand the configuration of the Search feature in Engagement Messenger to configure the field values.

<table id="table_opq_wb1_g4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search message

</td><td>

Text that is used for the search feature widget in the messenger.

</td></tr><tr><td>

Placeholder text

</td><td>

Placeholder text that appears in the search box.

</td></tr><tr><td>

Enabled for unauthenticated users

</td><td>

Option for enabling this feature for guest users who visit the website that hosts the messenger.**Note:**

-   You also must configure EC AI Homepage Search widget, Typeahead Search widget, and AI Search Assist widget for public access to enable AI search for unauthenticated users. For more information, see [Enable AI Search in Engagement Messenger for unauthenticated users](../task/enable-ai-guest-user.md).
-   Starting with the Vancouver release, the chat client was enabled by default only for authenticated users. To enable the chat client for unauthenticated users to be able to access Virtual Agent chat and Live Agent chat, you must enable the **$sn-va-web-client-app** and **sn\_va\_web\_client\_app\_embed** pages for public access. For more information, see [Make UI pages public or private](https://www.servicenow.com/docs/access?context=t_MakeAPagePublic&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Enabled for authenticated users

</td><td>

Option for enabling this feature for users who sign in to the website that hosts the messenger.

</td></tr><tr><td>

Search application

</td><td>

Application that is used to power the search functionality in Engagement Messenger. This field is automatically set to **Engagement Messenger AI Search Config**.To configure the new search application, navigate to **Engagement Messenger** &gt; **Modules** &gt; **Administration** &gt; **Search Applications**.

</td></tr></tbody>
</table>![Search feature widget screen with a search message and placeholder text in the search bar.](../image/em-search-feature-widget.png "Search feature widget")

In addition to configuring these fields for Engagement Messenger, you must configure AI Search in your ServiceNow instance and then enable Typeahead Search and AI Search Assist widgets so that the unauthenticated users can use the AI search feature from Engagement Messenger.

For more information on enabling Typeahead Search and AI Search Assist widgets for Engagement Messenger, see [Enabling AI search in the Customer and Consumer Service Portals for unauthenticated users](../task/configure_search_csp_guestuser.md).

For more information of AI Search configuration, see [Configuring AI Search](https://www.servicenow.com/docs/access?context=configuring-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

For more information on the availability of AI Search in your instance, see the [AI Search Availability \[KB0867751\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867751) article.

**Note:**

-   In the Firefox browser, AI Search results aren’t displayed on the Engagement Messenger home page.
-   If AI Search isn’t enabled:
    -   The search feature won’t be available for users if the messenger module is created on or after version 5.6.
    -   Zing search is used for messenger modules created before version 5.6.

