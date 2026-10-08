---
title: Mobile language menu unification
description: Learn about the different Language options in the Settings menu for ServiceNow mobile client versions 22.1 and 22.2.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/mobile/language-menu-unification.html
release: australia
topic_type: reference
last_updated: "2026-10-01"
reading_time_minutes: 1
breadcrumb: [Localization, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Mobile language menu unification

Learn about the different Language options in the Settings menu for ServiceNow mobile client versions 22.1 and 22.2.

For new customers using version 22.2, after selecting the Language option in the Settings menu, users are automatically directed to the account’s language page. The account language includes both the preferred and instance language settings. This avoids the need for users to select multiple language options on their mobile device.

For existing customers using version 22.2 and earlier, after selecting the Language option in the settings menu, users are required to select a language setting for both their Preferred language and Account language settings. For more information on Preferred language and Account language, see [Client-side localization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/localization-client.md).

<table id="table_tj3_vtk_tkc"><tbody><tr><td>

Default language options in Settings page \(Existing customers using version 22.2 and earlier\)

</td><td>

Default language options in Settings page \(New customers using version 22.2\)

</td></tr><tr><td>

\[Omitted image "lang-landing-two-options.png"\] Alt text: Language landing page with two options

</td><td>

\[Omitted image "language-landing-page.png"\] Alt text: Language landing page with instant language selection

</td></tr></tbody>
</table>The change in the menu display is due to the inclusion of the system property glide.sg.unify\_language\_settings.

For new customers from version 22.2 and above, the default option of the settings property is set to true. This means that users view the account's language options after selecting the Language menu option. The property can be added manually for existing customers on client version 22.2 and earlier. For more information, see [Configure the Language menu to be a single option](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/language-unification-config.md).

-   **[Configure the Language menu to be a single option](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/language-unification-config.md)**  
Configure the mobile property glide.sg.unify\_language\_settings to unify the Language option in the Settings screen. Use this setting to prevent the need for users to select multiple language options on their mobile device.

**Parent Topic:**[Localization on mobile devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/localization-mobile-device.md)

