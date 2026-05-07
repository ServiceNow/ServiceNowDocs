---
title: Boundaries and limits
description: View a list of boundaries and limits in CPQ.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Boundaries and limits

View a list of boundaries and limits in CPQ.

## Blueprints

No limits are imposed on the number of fields, rules, or layouts associated with a Blueprint.

## Fields

Text fields: 2000 characters.

Picklist extensions: ProductOrderNumber accepts an integer up to 88 characters.

## Fields

Simple message actions: 256 characters.

Picklist fields will only display 100 options in a drop-down list. Options not included in the list are still searchable by typing into the field.

Subfields that product picker can contain: 50.

## Sets

Each set can contain up to 2000 records. An error will be thrown if the set.size field is greater than 2000.

No hard limit exists on the number of fields that can be associated with a set. However, a practical threshold exists, beyond which runtime performance will suffer. This threshold has several dependencies, including the number and complexity of rules running between fields on set index, the number of set records defined during configuration, the total number of fields shown in the UI, and so on. Unfortunately, no simple rule of thumb exists to determine this threshold for your implementation.

Set repeater indices that display on a layout: 50.

## Rules

Custom grouping: 2000 characters.

## Tables

Rows in a table: no practical limit.

Columns in a table: no practical limit.

Length of value stored in text-type column cell: 2000 characters.

Length of value stored in number-type column cell: For practical purposes, no limit.

## ProductList object

ProductList.orderNumber: 28 digits.

## Scripting and enrichments

Lookup: returns a maximum of 10,000 rows from a managed table.

Advanced rules and enrichments are limited to 50,000 characters.

## Matrix Loader

ZIP files over 75 MB cannot be imported.

## Layout Wizard

500 fields can be automatically loaded when the Layout Wizard is initialized. Additional fields must be added manually via the Add Field menu.

**Parent Topic:**[CPQ reference](../reference/servicenow-cpq-reference.md)

