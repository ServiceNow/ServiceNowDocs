---
title: Matrix Loader: CSV rules upload
description: Use the Matrix Loader to bulk create, edit, and export rules in CPQ. Define rule conditions, actions, and logic in a CSV file to streamline configuration management and automate large-scale updates.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure the Matrix Loader, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Matrix Loader: CSV rules upload

Use the Matrix Loader to bulk create, edit, and export rules in CPQ. Define rule conditions, actions, and logic in a CSV file to streamline configuration management and automate large-scale updates.

The the Matrix Loader enables administrators to efficiently upload and manage all rule types in CPQ. Instead of manually creating each rule in the Admin interface, you can define them in a spreadsheet, export the sheet to CSV format, and upload it directly into the environment. This enables faster configuration setup, easier testing, and simplified migration between sandbox and production environments.

## Rules upload structure

Each row in the CSV file represents a rule record. The following table outlines the columns and data that the Matrix Loader accepts for rule uploads.

|Column Name|Description|Valid Values|Notes|
|-----------|-----------|------------|-----|
|record\_type|Identifies this as a rule upload|rule|Required|
|rule\_name|Name displayed on the rule list Admin page|Valid strings can be composed of up to 255 characters, including letters, numbers, spaces, and the following special characters: `{}[]()|\~`_^@?<=>;:/.-,+*’&%$#”!`|Required|
|rule\_variable\_name|Unique string used by CPQ to reference the rule|Valid field variable names consist of up to 128 letters, numbers, and underscores. The first and last character must be a letter or number.|Required; must be unique|
|rule\_description|Contextual description for administrator reference|Valid strings can be composed of up to 255 characters, including letters, numbers, spaces, and the following special characters: `{}[]()|\~`_^@?<=>;:/.-,+*’&%$#”!`|Optional|
|rule\_status|Determines if the rule is active|active, inactive|Required; inactive rules are ignored by the engine|
|action\_type|Defines the type of action executed when the rule runs|visibility, message, exclusion, inclusion, determination, product|Required|
|action\_sub\_type|Supplementary definition augmenting action\_type|hide, info, warning, error, hidden, disabled, set, forceset, manufacturing, sales|Optional; depends on action\_type|
|action\_field|Field to which the action applies|&lt;field variableName&gt;|Required|
|action\_value|Value applied to the action\_field|Varies by action type|Required for message, exclusion, inclusion, or determination actions|
|action\_product|Product reference for bill-of-material \(BOM\) actions|SFDC Product Code, Product2 ID, or External ID|Required for product actions|
|action\_quantity|Quantity of the product added to the BOM|&lt;positive float&gt; or &lt;positive integer&gt;|Required for product actions|
|action\_mandatory|Specifies whether a BOM product is optional or mandatory|TRUE, FALSE, &lt;empty&gt;|Optional; defaults to TRUE|
|grouping|Defines how conditions are grouped and evaluated|any, all, custom, always|Required|
|resource / operator / value|Defines condition tuples forming the rule logic|&lt;field variableName&gt;, operator, value|Resource, operator, and value together define the condition expression|

## Condition groupings

Condition groupings determine how rule conditions are logically combined. Supported options include:

-   any: ORs all conditions defined in the row.
-   all: ANDs all conditions defined in the row.
-   custom: Allows complex logic expressions, such as \(1 OR 2\) AND 3.
-   always: Applies the rule unconditionally.

## Valid operators

The following operators are supported for condition evaluation:

-   equals \(=, ==, equals\)
-   not equals \(!=\)
-   less than \(&lt;\)
-   less than or equal
-   greater than \(&gt;\)
-   greater than or equal \(&gt;=\)
-   contains / not contains
-   in / not in

## General guidelines

-   Always verify variable names match the field references exactly.
-   Keep rule descriptions concise but descriptive to aid troubleshooting.
-   Use inactive status for testing new rules before enabling in production.
-   Validate grouping logic \(any/all/custom\) carefully to avoid unintended outcomes.
-   Ensure product references \(Product2 ID or External ID\) align with your Salesforce configuration.

## Exporting rules to CSV

Administrators can export all rule definitions from the CPQ environment to CSV format for review or migration. The resulting ZIP file contains a single CSV file of all exported rule definitions.

1.  In the left Admin navigation pane, click **Rules**.
2.  Optional: enter a search string and press Enter to narrow results.
3.  Click **Export**. A message confirming export appears at the bottom of the page.
4.  Open the Notification Center \(bottom left\) and click the **Download** link.

## Additional information

-   Valid strings may include letters, numbers, spaces, and special characters: `{ } [ ] ( ) | \ ~ ` _ ^ @ ? < = > ; : / . - , + * ’ & % $ # "`
-   Rule variable names can contain up to 255 alphanumeric characters and underscores. They must begin and end with a letter or number.
-   Cells with gray backgrounds in sample files denote irrelevant fields for the current context.
-   Use the provided sample files \(Admin → Matrix Loader → Sample Files → Rules\) as a template for formatting.

**Related topics**  


[Configure the Matrix Loader](cpq-using-the-matrix-loader.md)

[Matrix Loader: CSV rules upload](matrix_loader_csv_rules_upload.md)

