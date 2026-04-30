---
title: Web to mobile component conversion
description: Use guided UI to configure native mobile components using an existing web component as a starting reference.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using the Mobile App Builder, Mobile App Builder, Mobile app building tools, Building mobile apps, Mobile Platform]
---

# Web to mobile component conversion

Use guided UI to configure native mobile components using an existing web component as a starting reference.

![window with option to choose to either create a screen from scratch of use web to mobile](../image/web-mobile-conversion.png "Web to mobile")

Web to mobile streamlines the component creation process by enabling you to select an existing web component to serve as a template instead of building a new record screen from the ground up. Currently, web conversion supports generating a record screen with a details screen segment.

## Selecting a card

Choose what card will serve as the template for your mobile record screen. You can choose from three different options and preview how each will look before confirming your selection.

-   **Use an existing card**

    Select an existing card to use for your record. You can preview the card and make changes before confirming your selection.

-   **Use a generic card**

    Start with a basic card template that has the essential components to get you started. You can preview the card and make changes before confirming your selection.

-   **Use Now Assist**

    Use AI-powered Now Assist to create a card for your record screen. Now Assist uses semantic search to populate the card with the fields that best match your web component. You can preview the generated card and make changes before confirming your selection. If you want to see more options, you can ask Now Assist to regenerate the card with different fields.

    Records created using Now Assist have a sparkle icon \(![sparkle icon](../image/mab-sparkle-icon-na.png)\) next to their name to indicate they were generated using AI. Once the records have been edited and reviewed, the indicator disappears.


## Mobile component preview

![visual preview of your new mobile component](../image/web-mobile-preview.png "Mobile component preview")

The web to mobile selection page presents a list of all available tables and web forms that can be used as templates. When selecting a web component to serve as the template, a preview of the new record is generated. You can freely switch between the existing card, generic card, and Now Assist generated card previews to compare them and see which option looks best. Selecting **Looks good, continue** generates the relevant records using the selected card.

The generated records have an icon \(![icon for generated records](../image/mab-generated-icon.png)\) next to their name to indicate that they were automatically generated. Once the records have been edited and reviewed, the indicator disappears.

![generated mobile record screen](../image/web-mobile-generated-record.png "Record generated using a web component")

