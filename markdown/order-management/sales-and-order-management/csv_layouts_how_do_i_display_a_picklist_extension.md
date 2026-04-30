---
title: Displaying a picklist extension on a layout
description: Learn how to display a picklist extension \(PLE\) on a layout using either the ServiceNow CPQ Admin UI or a CSV upload. Configure foundational picklist fields, map extension columns, and design layouts that present rich, multi-column picklist data.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 3
breadcrumb: [Configure picklist extensions, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Displaying a picklist extension on a layout

Learn how to display a picklist extension \(PLE\) on a layout using either the ServiceNow CPQ Admin UI or a CSV upload. Configure foundational picklist fields, map extension columns, and design layouts that present rich, multi-column picklist data.

In this article, we show a simple picklist extension \(PLE\) as it appears to an end user and how to display it in the layout, either by adding it using the admin UI or by uploading a CSV file.

## End-user view

![CSV layout display](../images/cpq-csv-layouts-display-picklist-extension-1.png)

In this layout, we have the following structure:

-   An ExpandableSection with the label "Select Your Doggo"
-   A ColumnSet with the label "Filters"
-   Three fields that act as filters for the PLE: Dog Size, Dog Bark/Voice, and Dog Hairiness
-   A ColumnSet with no label \(optional; administrators choice, but doesn't serve any purpose\)
-   The PLE framework. Label: "Dog Breeds...choose as many as you need". Displayed as a MultiSelect picklistGrid to match the multi-select type of the foundational picklist field \(Breed \[dogBreed\]\) that we're extending
-   Eight columns in the PLE framework, consisting of \(from left to right\):
    -   Breed: we're showing the label of the foundational multi-select picklist field, dogBreed
    -   Size \[size\], referenced from the PLE data structure
    -   Shedding \[shedding\], referenced from the PLE data structure
    -   Exercise Requirements \[exerciseReq\], referenced from the PLE data structure
    -   Biddability \[biddability\], referenced from the PLE data structure
    -   Bark \[dogBarking\], referenced from the PLE data structure
    -   Drive \[drive\], referenced from the PLE data structure
    -   Activities \[activities\], referenced from the PLE data structure

## Picklist extension data structure

In the dogBreed multi-select picklist field, extension information is mapped as follows:

![Picklist extendion](../images/cpq-csv-layouts-display-picklist-extension-2.png)

Observe the extended info columns, marked with yellow circles. Later, in the CSV layout, we will map these as fieldExtensions to the foundational dogBreed picklist field. \(See the picklist extension CSV layout section.\)

## Adding a picklist extension to the layout using the ServiceNow CPQ Admin UI

ServiceNow CPQ supports the ability to easily add a picklist extension to the layout using the ServiceNow CPQ Admin UI. Navigate to the layout from the Blueprint and add the picklist extension field as you normally would any other field. We’ve added a picklist extension field, “Motherboard” to our layout.

![Motherboard](../images/cpq-picklist-extensions-motherboard.png)

You will see a “+” at the bottom-right of the newly added picklist extension field. Click it, and from here you can add columns that you defined on the picklist extension field itself. In the image below, we’ve added our columns for “value”, “socketType”, and “memoryCapacity”.

![Motherboard](../images/cpq-picklist-extensions-motherboard-plus.png)

## Picklist extension CSV layout

The following is an image of the CSV layout. Ignore the gray-highlighted rows \(1-8\), as these have nothing to do with the picklist extension definition. Focus your attention on rows 9 through 17.

![CSV file](../images/cpq-csv-layouts-display-picklist-extension-3.png)

Row 9 \(green highlighted\): this is the picklist extension framework. In E9, we identify the variable name of the foundational picklist field \[dogBreed\]. As dogBreed is a multi-select picklist, we set the Component display type, F9, to 'MultiSelect picklistGrid', to match. \(If our foundational picklist field was a single-select picklist, we would set the corresponding Component display type to 'SingleSelect picklistGrid'.\)

In the rows highlighted yellow \(rows 10 through 17\), we reference the columns that are defined in the PLE data structure. Notes:

-   The type in A10:A17 is 'fieldExtension', the child type to a field whose Component display type is \[Multi\|Single\]Select picklistGrid \(F9\).
-   The path in B10:B17, /layout/tiers/doggo1/CS2/dogBreed, references the parent foundational picklist field, dogBreed \(E9\).
-   Row 10 instructs ServiceNow CPQ to show the labels \('label' in E10\) of the foundational picklist options. This is optional, but highly recommended. The first fieldExtension row \(A10\), this is the left most column of the PLE displayed.
-   The remaining fieldExtension rows lay out the remaining columns, from left to right, in the PLE display table.

The setup above would result in the following layout:

![Layout screen](../images/cpq-picklist-extensions-resulting-layout.png)

For your reference, this is the [sample CSV layout in spreadsheet format](https://docs.google.com/spreadsheets/d/1xNHwJ-ROze2xmz1gPCNNhBSCl9pmtMttd9U5zFI-5Ek/edit#gid%3D1182883775).

