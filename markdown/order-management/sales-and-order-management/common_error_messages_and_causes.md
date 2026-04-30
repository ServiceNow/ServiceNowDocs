---
title: Common error messages and causes
description: Look here for information and troubleshooting steps when you receive an error message.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 1
breadcrumb: [ServiceNow CPQ, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Common error messages and causes

Look here for information and troubleshooting steps when you receive an error message.

## Unable to roll back to previous state

This error is often related to a table lookup. Check to ensure that any tables in a lookup exist in your ServiceNow CPQ environment. Check the syntax of your lookup to ensure that the table column headers exactly match your query script. Capitalization or spelling could be off, causing a table lookup to fail, resulting in this error.

This could also involve circular logic being triggered by a field change, such as the condition and action of a rule both including the same field. If this error is seen right after selecting a field option, check the rules related to the field \(by last modified date\) to help isolate the cause.

## Error: Your rules are running beyond the stipulated time. Please contact your system administrator

Typically, this means that some rules are running in an infinite loop.

A rule may have the same field as part of conditions and actions. For example, a determination rule sets a field value based on a value already in that field.

Diagnose this by getting the click path to fire error and then inactivating recently modified rules one at a time to see if the error continues to be encountered.

## “...Index '0' is out of bounds…”

This almost always means that something is trying to reference an empty list or an empty array. In a literal sense, the error message is trying to reference the first index \(0\) of the list or array and is finding that 0 is beyond the bounds of the list or array.

Some possible causes:

-   Something is misspelled in a table query.
-   The query references a cfg value that hasnʼt yet been set, due to the rule conditions.
-   The lookup query returned no results.

Null checks on arrays are always a good idea.

## Cannot read properties of undefined \(reading 'map'\)

This error occurs on the buyside when the user opens ServiceNow CPQ config.

Review the layout file. Make sure that references to set the variable names are accurate.

**Parent Topic:**[ServiceNow CPQ reference](../reference/servicenow-cpq-reference.md)

