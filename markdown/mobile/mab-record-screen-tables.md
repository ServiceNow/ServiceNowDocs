---
title: Record screen tables
description: Use tables in the Mobile App Builder record screen to reference child records to a parent record. These records can consist of either single reference records or multi-reference records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mab-record-screen-tables.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Record screen, Mobile App Builder, Building tools, Building mobile apps, Mobile Platform]
---

# Record screen tables

Use tables in the Mobile App Builder record screen to reference child records to a parent record. These records can consist of either single reference records or multi-reference records.

Tables in a record screen are one of a few input field types. For a complete list of input field types, see [Record screen input field types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mab-record-screen-input-types.md). Tables contain reference records where you can select or create a child record that the parent record can reference. The option to select or create a reference record is predefined according to the record you select.

\[Omitted image "mab-record-screen-table-large.png"\] Alt text: Mobile App Builder record screen table

## Usage of Choose and New buttons in record screen tables

Each table within a record screen table displays either a **Choose** button \(\[Omitted image "mab-button-choose.png"\] Alt text: Choose button in record screen table.\), a **New** button \(\[Omitted image "mab-button-new.png"\] Alt text: New button in record screen table.\), or both buttons \(\[Omitted image "mab-button-choose-and-new.png"\] Alt text: Choose and New button in record screen table.\).

-   In a situation where you can only reference existing records, the **Choose** button displays.
-   In a situation when you can only create a new reference to the record you are working on, the **New** button displays.

If the **Choose** or **New** button is inactive after you make a single selection, it means that only a single record can be referenced. This is known as a single-reference record. Alternatively, when more than one selection can be made, this is a multi-reference record.

To change a single-reference record, first remove the existing reference by selecting the delete row icon \(\[Omitted image "mab-button-delete-row.png"\] Alt text: Delete row icon.\), then either choose or create a new reference.

For more information about working with these options, see [Create reference record entries in record screen tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mab-record-screen-table-add-edit.md) and [Edit record reference entries in record screen tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mab-record-screen-table-edit.md).

## UI elements in a table reference record

The Mobile App Builder table reference records contain the following UI elements.

|UI element|Function|
|----------|--------|
|\[Omitted image "mab-table-entry-blue.png"\] Alt text: Actionable item in table reference record.|Actionable items in a table reference record are blue. These items can be record names that open the record, remove buttons, and editable fields.|
|\[Omitted image "mab-column-sort.png"\] Alt text: Column sort button in table reference record.|The column sort icon is available within the header row of all tables in the Mobile App Builder. Select the column sort icon \(\[Omitted image "mab-column-sort-triangle.png"\] Alt text: Column sort icon.\) to list the column contents in either ascending or descending order. The black triangle indicates the sorting order for the entire table.|
|\[Omitted image "mab-field-inline-editing.png"\] Alt text: order being set to 100|You can perform inline editing in certain fields, such as the **Order** field. When performing inline editing, you change content within the table and you do not need to open the record.|
|\[Omitted image "mab-button-delete-row.png"\] Alt text: Delete row button.|Use the remove icon to remove an entry from the record. It does not delete the entry from the database.|

**Related topics**  


[Create reference record entries in record screen tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mab-record-screen-table-add-edit.md)

[Edit record reference entries in record screen tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mab-record-screen-table-edit.md)

