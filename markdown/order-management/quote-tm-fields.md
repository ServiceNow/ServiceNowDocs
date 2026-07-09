---
title: Quote transaction fields
description: ServiceNow Quote Experience supports five field types at two levels —transaction \(header\) and transaction line —enabling administrators to capture all required quote data in ServiceNow CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-fields.html
release: australia
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 4
breadcrumb: [Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Quote transaction fields

ServiceNow Quote Experience supports five field types at two levels —transaction \(header\) and transaction line —enabling administrators to capture all required quote data in ServiceNow CPQ.

Fields in ServiceNow Quote Experience store data on a quote. Administrators create fields at the transaction level for deal-level data and at the transaction line level for product and pricing data. The level at which a field is created affects its availability in rules, which also operate at transaction or transaction line level.

## Field levels

|Field level|Description|
|-----------|-----------|
|Transaction level \(header\)|Transaction-level fields sit outside the quote lines grid. They capture information about the deal as a whole, such as account, addresses, list price total, total discount, and net total.|
|Transaction line level|Transaction line-level fields sit in the quote lines grid. They can appear as column fields or as fields in the Line Details UI Effect.|

## Field types

ServiceNow Quote Experience supports the following field types at both levels.

Every field, regardless of type, includes these standard attributes and settings:

-   Field name — Display label that appears in the user interface
-   Variable name — Unique system identifier for the field, locked after creation \(select a descriptive name that does not require changes later\)
-   Default value — Value that automatically populates when a new transaction is created
-   Required — Toggle that enforces validation so users must provide a value before proceeding
-   Access Control — Settings that determine user permissions:
    -   Editable — Users can view and modify the field
    -   Read-only — Users can view but cannot modify the field
    -   No Access — Field is hidden from users

For details on configuring access control rules for different user groups, see [ServiceNow Quote Experience: Transaction Access Control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/cpq-transaction-manager-transaction-access-control.md).

<table id="table_nwg_ldp_hjc"><thead><tr><th>

Field type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Text

</td><td>

Stores free-form text input, such as names, descriptions, or open-ended responses. Text fields support configurable length constraints—administrators can set a minimum character length to ensure users enter sufficient detail and a maximum character length to prevent long entries.

</td></tr><tr><td>

Number

</td><td>

Stores numeric values for quantities, amounts, or calculations.Number fields support three distinct types: Integer \(whole numbers only\), Decimal \(numbers with decimal places\), and Currency \(numbers formatted as currency\). Supports configurable minimum and maximum value constraints to validate that users enter data within acceptable ranges.

</td></tr><tr><td>

Boolean

</td><td>

Stores a true or false value, typically displayed as a check box or toggle switch.You can customize the labels for each state—for example, "Yes/No," "Enabled/Disabled," or "Active/Inactive"—to match your business terminology. You can set a default checked state so the field comes pre-checked or unchecked when a transaction is created.

</td></tr><tr><td>

Picklist

</td><td>

Stores a single selected value or multiple selected values from a defined list of options, depending on the configuration mode selected.When defining picklist options, you control the order in which they appear, assign a label \(the user-facing name\) and value \(the system identifier\), designate a default selection, provide an optional description, and include an optional image URL to visually represent the option.

Picklist fields support a comparison type setting—select Text to compare options as text strings or Number to compare them numerically. This setting affects how the system processes and sorts picklist selections.

</td></tr><tr><td>

Date/Time

</td><td>

Stores both date and time values in UTC format \(YYYY-MM-DDTHH:MM:SSZ\) to ensure consistency across time zones.You can set a default date/time value that pre-fills when a transaction is created. The Not Before and Not After constraints restrict the date/time range users can select, enforcing business rules such as "quotes cannot be created for dates in the past" or "expiration dates must be within 30 days."

For detailed guidance on date and time field configuration and best practices, see [Date and time field fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-date-time-field-behavior.md).

</td></tr></tbody>
</table>## System-provided fields

ServiceNow Quote Experience provides a set of system-provided fields at both levels that are commonly used in transaction processing.

Transaction-level system fields cover the following categories: pricing information, opportunity information, transaction information, and account information. For a complete list, see [Transaction-level system fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-header-level-system-fields.md).

Transaction line-level system fields cover the following categories: pricing information, transaction line information, configuration information, product information, and order information. For a complete list, see [Transaction line-level system fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-line-level-system-fields.md).

## Custom fields

Custom fields can be added to a blueprint through the ServiceNow Quote Experience administration interface. Fields created through the interface are automatically associated with the blueprint.

**Related topics**  


[Create a transaction field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-field.md)

[Transaction-level system fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-header-level-system-fields.md)

[Transaction line-level system fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-line-level-system-fields.md)

[Date and time field fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-date-time-field-behavior.md)

