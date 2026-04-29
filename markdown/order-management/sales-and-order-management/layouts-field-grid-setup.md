---
title: Layouts: Field grid setup
description: A field grid collects multiple fields in a single layout, but unlike a set, it can reference other rows.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up layouts, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Layouts: Field grid setup

A field grid collects multiple fields in a single layout, but unlike a set, it can reference other rows.

A field grid presents numerous fields in a matrixed layout. These are helpful when you need to request the same set of information a predetermined number of times. Field grids allow users to create a table of repeated values. In a field grid, rows can reference other rows, while in a set a user cannot write rules between indexes.

Field grids can expand in columnar or row direction \(that is, horizontally or vertically\).

Define all fields that are intended to be displayed in the field grid. Matrix Loader is a good tool for this. Associate the fields with the blueprint in which they will be used.

## Field grid layout setup

To add a field grid to the layout, a column set is not needed because the field grid creates the rows and columns. Instead, the following row types are needed:

-   **fieldgrid**: this type tells the layout that a field grid will be used in the layout
-   **fieldgriddata**: this type is used for each column of the field grid
-   **field**: this type is needed for each cell in the field grid \(not each row\)

The first three images show the CSV file. The last image shows the corresponding user layout. The numbers above align with the numbers in the images below. \(Because number 3 is shown several times, a letter is added for clarity.\) Individual cells in the field grid cannot have both a label and an input field. Note that by 3C, both a label and input field are added to the layout CSV file. However, only the input field goes in the layout.

![Field grid](../images/cpq-field-grid-setup-1.png)

![Field grid](../images/cpq-field-grid-setup-2.png)

![Field grid](../images/cpq-field-grid-setup-3.png)

![Field grid](../images/cpq-field-grid-setup-4.png)

[fieldGrid Sample Layout JSON](https://docs.google.com/document/d/123dT0vwmwBUWgyrEV5RzI3rH3WugJd2xUUkpI9O2Ias/edit?usp=sharing)

## Field grid UI controls

Various aspects of the field grid UI can be controlled by updating the value field in the layout CSV file:

-   Gridline visibility
-   Dynamic column headers
-   Field grid field width

## Fieldgrid elements

The following values can be added to the value column of fieldgrid elements:

-   **indexPre**: String value to be displayed in the index column before the index number. optional
-   **indexPost**: String value to be displayed in the index column after the index number. optional
-   **indexVisible**: true \| false, whether to display the index number and column in the field grid layout. Optional, default: true
-   **maximumHeight**: Maximum height to set in CSS px. I.e. "180px". optional
-   **gridlines**: all \| horizontal \| vertical \| none, control how grid lines are displayed between cells. Optional, default is all.

## Fieldgriddata elements

The following values can be added to the value column of fieldgriddata elements:

-   **fieldIndex**: name of field to use for header value. Optional. If included, the label for the fieldgriddata element should be blank.
-   **width**: width of the fields. Optional. If included, examples of valid value are **auto**, **300** \(px are assumed here\), **300px**, **20vw**, and **calc\(100% - 100px\).**

Field grids default to 100% width, but if even one width value is specified for a contained fieldgriddata component, the field grid’s width will change to **auto** so that a specified width can be applied.

[Example field grid dynamic headers and grid lines CSV file](https://drive.google.com/file/d/1MrYYBg8_tjHOa2QfhHWLmkReNbRDmkA-/view?usp=share_link)

[Example field grid width CSV file](https://drive.google.com/file/d/130w2Cz-5R7z1BwFO7_o1rD9IIlPol3DQ/view?usp=share_link)

