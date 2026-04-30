---
title: Create path segment records and supported URL records for universal linking
description: Create path segment records and supported URLs records for universal linking to display a mobile banner. Users see this banner when they land on specific platform web pages. Within each supported URL, you define the page where the banner appears, the mobile app and the screen type the user views, and the data displayed within the screen.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Mobile universal linking for supported URLs, Universal linking for mobile, Mobile URLs, Configuring the Mobile Platform, Mobile Platform]
---

# Create path segment records and supported URL records for universal linking

Create path segment records and supported URLs records for universal linking to display a mobile banner. Users see this banner when they land on specific platform web pages. Within each supported URL, you define the page where the banner appears, the mobile app and the screen type the user views, and the data displayed within the screen.

## Before you begin

Role required: admin

## Procedure

1.  Create a path segment record.

    1.  In the web-based UI, navigate to **System Mobile** &gt; **Mobile Universal Linking** &gt; **Path Segments**.

    2.  Select **New** to create a universal link path segment.

    3.  On the form, fill in the fields.

<table id="table_uy4_1xw_spb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Title for the universal link path segment.

</td></tr><tr><td>

Path segment regex

</td><td>

Regular expression of the string that defines the category path of the URL.The system evaluates the regular expression string and then performs the matching process on the supported URLs.

</td></tr></tbody>
</table>    4.  Select **Submit**.

2.  Create a universal link supported URL.

    1.  In the web-based UI, navigate to **System Mobile** &gt; **Mobile Universal Liking** &gt; **Supported URLs**.

    2.  Select **New** to create a universal link supported URL.

    3.  On the form, fill in the fields.

<table id="table_ywm_k1n_wpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Title for the universal link supported URL.

</td></tr><tr><td>

Mobile app

</td><td>

ServiceNow mobile app the link opens in. Options are `Agent`, `Onboarding`, or `Request` \(Now Mobile\).

**Note:** The selection here overrides the selection made in the **Mobile app** field listed in the topic [Mapping specific mobile screens for universal linking](universal-linking-screen-mapping.md).

</td></tr><tr><td>

Active

</td><td>

Option for enabling the activation of this record.

</td></tr><tr><td>

Order

</td><td>

Option to determine in which order the instance matches a record. The lower the number, the higher the priority for matching the URL.**Note:** The system matches each record one by one. When a record matches a supported URL the instance generates a banner. The order is a way to put the more general supported URLs lower down on the list to prevent the usurping of specific links you want to match.

</td></tr><tr><td>

Path segment

</td><td>

Use the reference lookup icon to select the path segment you created earlier. The system begins to search for matches by first checking the referenced path segment. If there is no match, the instance does not display a banner.

</td></tr><tr><td>

Has query keys

</td><td>

Comma-separated string field for query keys. Each query key added into this string field must exist in the URL for there to be a match. An example entry is `id,table,sys_id`

</td></tr><tr><td>

Has query values

</td><td>

Option to add a name a value for each query key you added. An example is **Name** = `id` and **Value** = `ticket`

</td></tr><tr><td>

Mobile screen builder

</td><td>

Use the mobile screen builder script block to define the screen type to build and the data the screen uses. Using one of the provided methods in the script block it creates a list screen, record screen, or browser screen. Each method has its own parameter requirements. You can find specific parameters in the script block comments. For more information, see [GlideRecord](https://developer.servicenow.com/dev.do#!/reference/api/orlando/server/no-namespace/c_GlideRecordScopedAPI) in the [ServiceNow® Developer Site](https://developer.servicenow.com/).

</td></tr></tbody>
</table>    4.  Select **Submit**.


## What to do next

After defining when banners appear and the screen and content the user views, consider enhancing the experience by associating the screen to a preconfigured table. See, [Mapping specific mobile screens for universal linking](universal-linking-screen-mapping.md).

**Parent Topic:**[Mobile universal linking for supported URLs](../concept/universal-linking-support-urls.md)

