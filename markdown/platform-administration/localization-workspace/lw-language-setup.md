---
title: Language setup in Localization Workspace
description: Language setup enables you to flexibly configure target languages and their third-party translation service providers. When your users create translation requests, they can select the languages and providers you have configured.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/localization-workspace/lw-language-setup.html
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: concept
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Language setup in Localization Workspace

Language setup enables you to flexibly configure target languages and their third-party translation service providers. When your users create translation requests, they can select the languages and providers you have configured.

**Note:** From version 3.0.0, two guided tours are available. One guided tour assists with configuring a language provider, and is accessible to users with the Localization administrator role \(localization\_admin\). The other guided tour assists with configuring language groups, and is accessible to the Localization administrator and the Localization requester role \(localization\_requestor\). Find the guided tours by selecting the Help Center icon \[Omitted image "Banner\_HelpIcon.png"\] on the Localization Workspace [Home](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-workspace/lw-status-synchronization.md) screen.

Navigate to **All** &gt; **Localization Workspace** &gt; **Language setup**. The **Language Provider** tab opens by default, or you can select the **Language Groups** tab.

\[Omitted image "lw-language-setup1.png"\] Alt text: The Language setup tab with the Language Provider list open. Several example Language Providers are listed.

Roles in Language setup:

-   The localization\_admin role is required to create or edit a Language Provider.
-   The sn\_lw.user role can view Language Provider records, but can't create or edit them.
-   The sn\_lw.user role can create Language Groups by selecting from existing Language Providers.

-   **[Configure a language provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-workspace/lw-configure-translation-provider.md)**  
Set up language providers as part of configuring Localization Workspace. For each target language you can configure multiple providers with their pricing.
-   **[Configure language groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-workspace/lw-configure-language-groups.md)**  
After setting up individual language providers, you can define one or more language groups. Configuring language groups is an optional way to streamline the creation of translation requests.

**Parent Topic:**[Configuring Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-workspace/configuring-localization-workspace.md)

