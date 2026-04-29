---
title: Setting up the Image Viewer
description: You can use the Image Viewer to add images to fields for viewing in a media carousel.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Setting up the Image Viewer

You can use the Image Viewer to add images to fields for viewing in a media carousel.

The image viewer allows a Logik Admin to add featured images to supported fields that can be viewed in a media carousel. This article covers how to set up the Image Viewer in the Logik Admin and how it displays on your layout.

## Supported field display types

-   Static Image
-   MultiSelectProductPickerGrid
-   MultiSelectVisualProductPicker
-   ProductPickerGrid
-   VisualProductPicker
-   MultiSelect picklistGrid
-   SingleSelect picklistGrid
-   Multiselect Visual Picker
-   Visual Picker

## Static images

To display the Image Viewer for a Static Image field, follow these steps:

1.  Open the layout where you want to add the Image Viewer.
2.  Hover over the field and click the gear icon.
3.  Open the raw value menu and add the following while including the required inputs in place of the placeholder text below.

    ![Static images code](../images/cpq-image-viewer-raw-value.png)

4.  Click **Save**, and deploy the blueprint.

## Raw value details for Image Viewer

Add the following to the “Raw Value” section of an image display component through the Admin UI, where `Array<FeatureImage>` is an array of your additional feature images in the Feature Image type format and `carouselEnabled` is set to true or false.

```
"featureImageSettings": {
      "additionalImages": Array<FeatureImage>,
      "carouselEnabled": boolean
  }
```

By default, `carouselEnabled` is false.

## Defining a feature image

```
FeatureImage = {
  “src”: string,
  “alt”?: string,
  "label"?: string,
}
```

## Product Pickers

To display the Image Viewer for a product picker field, follow these steps:

1.  Select your product picker field.
2.  Select the Option Fields tab.
3.  Click **+ Add**.
    -   Set the Field Type to Text.
    -   Set the Product List Property to Product Extended.
4.  Create one Text field for each image to include in the Image Viewer.

    **Note:** To display alt text or a label, additional fields for each type must be created. These fields are not required.

    ![Product picker setup](../images/cpq-image-viewer-product-picker-fields.png)

5.  Select the Bulk Actions tab.
6.  Click Add New Action.
7.  Select type Determined Action.
8.  Enter a Bulk Action Name.
9.  Select all of the fields added for your Image Viewer.

    ![Product picket setup](../images/cpq-image-viewer-product-picker-bulk-action-1.png)

10. Click **Save**.
11. On the Bulk Actions tab, provide the URL for each image as well as text for labels and alt text if desired.

    ![Image viewer demo](../images/cpq-image-viewer-product-picker-bulk-action-2.png)

12. Click **Save**
13. Open a layout that includes the product picker field.
14. Hover over the field and click the gear icon.
15. Toggle Enable Image Viewer to On.
16. Expand the Image Viewer Settings section.
17. Select the fields created from steps 3-4 that correspond to Image URL, Alt Text, and Label.

    Alt Text and Label are optional.

18. Click **+ Add** and repeat step 17 for each image that you want to include.

    ![Image viewer settings](../images/cpq-image-viewer-settings.png)

19. Click **Save**, and deploy the blueprint.

## Picklists

1.  Open the picklist field.
2.  Click the Picklist Extension tab.
3.  Click **Import Data**.
4.  Create a CSV that includes the following columns:
    -   value
    -   imageUrl
        -   Ensure this is a valid URL for the image to display.
        -   Create an imageUrl column for each image to include in the Image Viewer.
    -   imageLabel \(optional\)
    -   imageAltText \(optional\)

        ![CSV file](../images/cpq-image-viewer-picklist-csv.png)

5.  Import the created CSV.
6.  Click **Column Mapping**.
7.  For each field added, select the mapping menu and select the column name under the Extension mapping section.

    ![Picklist extension](../images/cpq-image-viewer-picklist-column-mapping.png)

8.  Click **Save Mapping**.
9.  Open a layout that includes the product picker field.
10. Hover over the field and click the gear icon.
11. Toggle Enable Image Viewer to On.
12. Expand the Image Viewer Settings section.
13. Select the fields created from the picklist extension data that correspond to Image URL, Alt Text, and Label.

    Alt Text and Label are optional.

14. Click **+ Add** and repeat step 13 for each image that you want to include.

    ![Image viewer settings](../images/cpq-image-viewer-picklist-field-properties.png)

15. Click **Save**, and deploy the blueprint.

## General guidelines

Ensure that the image sizes are the same for all images in a viewer. If they do not match, the thumbnails and featured image will not align properly.

Add images in the order you want them to display. Images will display from the Image Viewer settings from top to bottom. The name of the field does not affect the display order.

Use images with a high enough resolution to properly fill the window. Low resolution images will be expanded in size to fit the window and will not look good when select as the featured image.

For optimal performance, avoid large or high resolution images since that will impact the render time for the image viewer.

## Image Viewer display

On a layout with a field that includes an image view, a user can hover over an image to see the expand icon.

![Products screen](../images/cpq-image-viewer-display-1.png)

Once clicked, the image view will open in a dialog box.

![Image viewer display](../images/cpq-image-viewer-display-2.png)

A user can move between images with the arrow buttons or by clicking the thumbnails below the feature image. This carousel displays any label and alt text if provided. A user can close the dialog box by clicking outside it or by clicking **X** in the top right.

