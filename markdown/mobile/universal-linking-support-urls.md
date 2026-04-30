---
title: Mobile universal linking for supported URLs
description: Use mobile universal linking to display a web banner on specified platform web pages to encourage users to work within a ServiceNow mobile app. Configure the supported URLs that facilitate this functionality to ensure that the banners are displayed on the correct web pages. These URLs also direct users to a defined location within the appropriate mobile app.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Universal linking, Mobile URLs, Configuring the Mobile Platform, Mobile Platform]
---

# Mobile universal linking for supported URLs

Use mobile universal linking to display a web banner on specified platform web pages to encourage users to work within a ServiceNow mobile app. Configure the supported URLs that facilitate this functionality to ensure that the banners are displayed on the correct web pages. These URLs also direct users to a defined location within the appropriate mobile app.

Each time a user accesses a web page using their mobile web browser, the instance checks the URL against all the records in the path segment table and the supported URLs table. When there’s a match, the instance displays a web banner. After the user taps on the banner, the instance directs the user to the appropriate screen on a designated mobile app. This screen displays the selected data. When configuring a URL record for universal linking, the path, query keys, and query values of the URL must be an exact match of the web page.

## Structural layout of URLs used for mobile universal linking

Supported URLs can comprise of elements like host, path, query keys, and query values. These URLs are created in the universal link path segment table and the universal link supported URL table, as described in [Create path segment records and supported URL records for universal linking](../task/universal-linking-web-banner.md). You can make your URL as general or specific as you require. A more general the URL definition means that the banner is displayed over a larger number of web pages.

**Note:** When creating supported URLs, you must know what path segment, query keys, and query values you want the system to look for.

An example URL structure is `https://<baseURl>/sample_path.do/query_key_01=XYZ/query_key01=value_ABC`. The table describes the parts to create in a path segment record and a supported URL record.

|URL part|Description|
|--------|-----------|
|`sample_path`|Due to its generic nature, the path segment defines the category of the URL and is used to quickly filter out any unmatched records. The path segment record uses regular expressions to match URL texts.|
|`query_key`|Query keys are an extension of the URL that help define specific content.|
|`value`|Values can be added to the query keys, to further streamline the web pages you want to match.|

-   **[Create path segment records and supported URL records for universal linking](../task/universal-linking-web-banner.md)**  
Create path segment records and supported URLs records for universal linking to display a mobile banner. Users see this banner when they land on specific platform web pages. Within each supported URL, you define the page where the banner appears, the mobile app and the screen type the user views, and the data displayed within the screen.
-   **[Mapping specific mobile screens for universal linking](../task/universal-linking-screen-mapping.md)**  
Configure universal links for screen mapping so a user is redirected to a previously styled record screen or list screen. Use this option to provide a customized experience for the user.

**Parent Topic:**[Universal linking for mobile](universal-links-mobile.md)

