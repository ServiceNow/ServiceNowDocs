---
title: Global search for mobile
description: Give your users the ability to search for information within the defined search sources from a mobile app.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/mobile/mobile-platform/mobile-search-config.html
release: zurich
product: Mobile Platform
classification: mobile-platform
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Global search for mobile

Give your users the ability to search for information within the defined search sources from a mobile app.

## Global search bar

<table id="table_tkw_nln_rhb"><tbody><tr><td>

\[Omitted image "launcher-global-search.png"\] Alt text: Global search bar

</td><td>

You can include a global search bar on your launcher screen. Use search to give your users the ability to quickly find information within the defined search sources. Examples include people, catalog items, and knowledge base articles in your instance.

 There are two search engines available to activate within launcher screens.

-   **Zing** - The default search engine used to search ServiceNow AI Platform® record data. For more information, see Zing text indexing and search engine.
-   **AI Search** - AI search engine available for Now Mobile, which offers visually intelligent query features to help users quickly find the answers they need. For more information see, AI Search.

</td></tr></tbody>
</table>## Search criteria

Create search criteria for your launcher screen to help your users find related information quickly. You can configure which sources the search uses, as well as options like search result limits. For details on configuring custom search criteria:

-   For Zing search engine, see [Configure search criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-platform/sg-create-custom-search.md).
-   For AI Search search engine, see the Now Mobile documentation AI Search in mobile.

**Note:** AI Search utilizes the data sources of catalog items, KB articles and users. Use AI Search, wherever possible, when using these data sources. Use Zing in the launcher screen if you utilize other data sources not associated with AI Search, for example user tasks or requests.

## Voice search

Voice search enables your users to use global search using the speech recognition feature of their mobile device. Users access voice search by tapping the microphone icon \(\[Omitted image "mic-icon.png"\] Alt text: Microphone icon\) that appears on the right side of a search bar. For more information on configuring voice search, see [Enable voice search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-platform/turn-on-voice-search.md).

## Photo search

Photo search enables users to use global search by taking a picture. The Google Vision API identifies the picture and uses that identification as search query. Users access photo search by tapping photo icon \(\[Omitted image "sg-icon-image-search.png"\] Alt text: Photo search icon\) that appears in your launcher screen search bar. For more information on photo search, see [Mobile photo search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-platform/sg-mobile-image-search.md).

