---
title: Input form screen
description: Use input form screens to provide an interface for your users to enter information in mobile apps.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Input form screen

Use input form screens to provide an interface for your users to enter information in mobile apps.

<table id="table_dhx_ngq_pnb"><tbody><tr><td>

Input form screens display inputs to enable your users to enter information into mobile apps. Use input form screens to create or edit records, complete surveys, or any other situation where your users must enter information. Input form screens work in offline mode, so users don't need an internet connection to input information into the app.

 After you create an input form screen and define its inputs and variables, you must associate the input form screen with an action item. Then these inputs and variables must be mapped to the action item.

 You can control how users input data, as well as the appearance of input types. You can further customize your input form screens using [Mobile UI Rules](mobile-ui-rules.md).

</td><td>

![Examples of input form screens](../image/parameter-screen-example-1.png)

</td></tr></tbody>
</table>## Input form screen components

Input form screens consist of a header, and input section, and an option footer section for screens with multiple pages.

-   **Header**

    The header of your input form screen displays the title of your input form screen, as well as **Cancel** and **Submit** buttons. You can change the labels of these buttons when you create your input form screen.

-   **Input section**

    Below the header are your inputs. When building your input form screen, you can choose from several input types to give your users an easy intuitive experience for inputting information.

    -   Attachment
    -   Barcode
    -   Boolean
    -   Choice
    -   Custom map
    -   Date/time
    -   Number
    -   Ranking
    -   Reference
    -   Signature
    -   String
    -   Screen
    For more detail on these parameter input types, see [Input form screen attributes for inputs](../reference/parameter-screen-var-attr.md)

-   **Pagination buttons**

    If you configure your input form screen to use multiple pages, the pagination buttons display at the bottom of the screen. Your users can tap the **Previous** and **Next** buttons at the bottom of the screen to navigate between pages. As with the header buttons, you can change the label of these buttons when you create your input form screen.


## Input form screen limitation

Unsupported features

Carried parameters are not supported in the input form screen.

