---
title: Portal Banner widget instance options form
description: Instance options enable you to configure the Portal Banner widget on a portal page.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configurable Portal widgets instance options, Customer Service Management reference, Customer Service Management]
---

# Portal Banner widget instance options form

Instance options enable you to configure the Portal Banner widget on a portal page.

<table id="table_csm_base_entities"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Heading

</td><td>

Required title of a Portal Banner widget to greet a user who signs in into the website. The default text is `Home Page Banner`.The heading field supports placeholder variables such as &lt;user&gt;, &lt;title&gt;, and &lt;part\_of\_day&gt;. For example, you could display a banner title such as `Hello Mr. Luddy! Good Morning.`

-   &lt;user&gt;: The name of the logged-in user.
-   &lt;title&gt;: The salutation of the logged-in user. The &lt;title&gt; variable details are retrieved from the User \[sys\_user\] table.
-   &lt;part\_of\_day&gt;: Displays the greeting based on the part of the day of the user's region. For example, Good morning, Good afternoon, or Good evening.

</td></tr><tr><td>

Description

</td><td>

Required subtitle that appears below the heading. The default description is `This is home page description`.

</td></tr><tr><td>

Background Image

</td><td>

Image to appear as the background on the banner. **Note:** You can select images from the Images \[db\_image\] table or upload a new image to it. For more information, see [Storing images in the database](https://www.servicenow.com/docs/access?context=c_StoringImagesInTheDatabase&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Heading Text Color Hex code

</td><td>

Color of the heading text in hex code format.The default value is \#FFFFFF \(white\).

</td></tr><tr><td>

Description Text Color Hex code

</td><td>

Color of the description text color in hex code format.The default value is \#FFFFFF \(white\).

</td></tr><tr><td>

Alignment

</td><td>

Alignment of the banner content inside the widget.The available options are:

-   Left
-   Center

The default alignment is Center.

**Note:** Currently, if you select None, the alignment is set to Left.

</td></tr><tr><td>

Show Search bar

</td><td>

Option to display the search bar on the Portal Banner widget to search content.**Note:** You can enable the AI search for a banner widget to get quick results. For more information, see [Enable and configure AI Search in Service Portal](https://www.servicenow.com/docs/access?context=enable-ais-sp&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Show Primary Button

</td><td>

Option to display the primary button on the Portal Banner widget.

</td></tr><tr><td>

Primary Button Label

</td><td>

Label of the primary button.

</td></tr><tr><td>

Primary Button URL

</td><td>

The URL that opens an internal web page or a portal page in the same tab and an external page or a portal in a new tab. The two types of primary URLs are:-   Absolute URL: The full URL including its protocol \(http or https\). For example:

    ```
https://example.servicenow.com/scripts/sn_csm_ec.js?v=3.1
    ```

-   Relative URL: A URL that includes only the path that comes after the domain. For example:

    ```
scripts/sn_csm_ec.js?v=3.1
    ```


</td></tr><tr><td>

Show Secondary Button

</td><td>

Option to display a secondary button on the banner widget.

</td></tr><tr><td>

Secondary Button Label

</td><td>

Label of a secondary button.

</td></tr><tr><td>

Secondary Button URL

</td><td>

The URL that opens an internal web page or a portal page in the same tab and an external page or a portal in a new tab. The two types of secondary URLs are:-   Absolute URL: The full URL including its protocol \(http or https\). For example:

    ```
https://example.servicenow.com/scripts/sn_csm_ec.js?v=3.1
    ```

-   Relative URL: A URL that includes only the path that comes after the domain. For example:

    ```
scripts/sn_csm_ec.js?v=3.1
    ```


</td></tr><tr><td>

Search Placeholder Text

</td><td>

Placeholder text for the search option.

 The default text is `Search articles and request items`.

</td></tr></tbody>
</table><table id="table_emr_mqk_2zb"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Buttons Condition Script

</td><td>

Script to show or hide the primary or secondary button.You can use the scripted extension point to implement the condition script. By default, the new script displays both buttons and doesn’t include any condition. For more information, see [Provide web page link buttons to display on the Portal Banner widget](../task/portal-scripted-extension-banner.md).

</td></tr><tr><td>

Widget Placeholder

</td><td>

Option to embed an additional widget on the Portal Banner widget.You can include only widgets from the Widgets \[sp\_widget\] table.

</td></tr><tr><td>

Widget Option Schema

</td><td>

Defines the parameters of the widget that you want to add.For more information, see [Add a widget in the Portal Banner widget](../task/portal-banner-option-schema.md).

</td></tr></tbody>
</table>**Related topics**  


[Portal Banner widget](../concept/portal-banner-widget.md)

[Add and configure the Portal Banner widget](../task/config-portal-banner-widget-inst-opt.md)

[Provide web page link buttons to display on the Portal Banner widget](../task/portal-scripted-extension-banner.md)

[Add a widget in the Portal Banner widget](../task/portal-banner-option-schema.md)

