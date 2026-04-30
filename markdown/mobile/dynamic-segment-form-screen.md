---
title: Using dynamic segments to display data in a record screen
description: Dynamic segments in a record screen enable users to see a subset of relevant records rather than a whole list of records.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Using dynamic segments to display data in a record screen

Dynamic segments in a record screen enable users to see a subset of relevant records rather than a whole list of records.

Use dynamic segments to create a link between selected elements near the top of the screen and the content displayed below. The data displayed can either be the whole list of records or specific records that relate to the individual segments. For example, a time sheet can contain a dynamic segment consisting of the days of the working week. When a day is tapped, the relevant data displays according to the selected segment.

A record screen that contains a dynamic segment is comprised of the following components. For configuration details, see [Configure a dynamic segment to display selected data in a record screen](../task/form-screen-dynamic-segment.md)

-   Record screen header - An item view that displays a summary of records within a record screen. For more information, see [Record screen](form-screen.md).
-   Dynamic segment - List of records where each segment is a section of the list, for example, a day of the week. The data displayed in the embedded list screen area varies according to the selected segment.
-   Header segment - Optional component that displays the whole list of records. For more information, see [Embedded lists for a record screen](sg-embedded-list.md).
-   Segmented control - Area that includes both the dynamic segment and the header segment.
-   Embedded list screen - Display area as defined by the user's selection in the segmented control. For more information, see [Embedded lists for a record screen](sg-embedded-list.md).
-   Footer function - A function instance or function location that appears at the bottom of a record screen. For more information, see [Associate a function with a location in the app](../reference/sg-studio-button-instances.md).

![Dynamic segment in a record screen with callouts.](../image/dynamic-segment-form-callout.png "Record screen containing a dynamic segment")

## Sizing of dynamic segment buttons

When configuring a dynamic segment, you must define the height and width of the buttons. The options are small, medium, or large. Use the illustration to get a perspective of the sizes available.

![Graph showing the different available sizes of dynamic segment buttons.](../image/dynamic-segment-button-sizes.png "Dynamic segment button sizing graph")

