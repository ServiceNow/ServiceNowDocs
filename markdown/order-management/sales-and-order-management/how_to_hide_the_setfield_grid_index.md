---
title: Hiding the set grid and field grid indexes
description: You can hide the index column in a set grid or a field grid.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure sets, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Hiding the set grid and field grid indexes

You can hide the index column in a set grid or a field grid.

By default, the index column is displayed in a set grid or a field grid. This index column can be hidden in two ways: by using the layout wizard or by modifying the layout CSV file.

![Combo options](../images/cpq-index-column.png)

## Hide the index by using the layout wizard

Navigate to the layout in question in the CPQ Admin. Then click the gear icon next to the set or field grid. Then select the General Settings expandable section. Set the Show Index toggle to false, save the layout, and deploy. The index will no longer be displayed.

**Note:** the Show Index setting is available for field grids as well.

## Hide the index by modifying the layout CSV file

To hide the column, adjust your layout CSV to include the following instruction in the “Value”, for an appropriate row: `{“indexVisible” : “false”}`

The examples below illustrate the CSV files for a field grid and for a set. In both cases, the Index is hidden on runtime:

![CSV file](../images/cpq-grid-index-hidden.png)

## Field grid CSV file

![CSV file](../images/cpq-index-hiding-with-csv-sets.png)

[Link](https://docs.google.com/spreadsheets/d/13tWln8PHc6ITf8_gheuML_CCO-IuFLIps8-jOZNIsPw/edit?usp=sharing) to CSV example

## Sets CSV file

![CSV file](../images/cpq-index-hiding-with-csv-fieldgrid.png)

[Link](https://docs.google.com/spreadsheets/d/1Kt7lISg87_aNTOrKcKLbJ4ObKeROcGqOOT8vPVx00Vc/edit?usp=sharing) to CSV example

**Related topics**  


[Modifying the Size and Change Size fields for a set](how_to_alterhide_the_size_and_change_size_field_for_a_set.md)

