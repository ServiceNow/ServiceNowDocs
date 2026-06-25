---
title: Create scripts
description: Learn how to create advanced functions using the scripting interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/scripting.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up enrichments and rules scripting, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create scripts

Learn how to create advanced functions using the scripting interface.

Some use cases require an advanced condition or action. Other times, the administrator may prefer script versus leveraging simple rules. For these occasions, CPQ offers the ability to write scripts in key areas.

Scripting is available in rule actions and conditions, behind the Advanced menu choice or toggle.

\[Omitted image "cpq-scripting-advanced.png"\] Alt text: Rule

When you click **Create Advanced Function**, the script editor opens, including the tools you need to write a script.

When the script editor first opens, it provides the expected return format of the script.

-   Advanced conditions return true or false.
-   Advanced hiding rules return a text string.
-   Advanced determination rules return the type of the field that they are setting.
    -   A determination rule that sets a number returns a number.
    -   A determination rule that sets a multi-select picklist returns an array.
-   Advanced inclusion and exclusion rules return an array.
-   Product rules return ProductList.

For more details and a script sample, review the "Advanced product actions" section of [Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/rules_101.md).

The **? Help** button opens a menu of available functions. Each entry includes a description of the function, the parameters it accepts, its output, and an example that can be inserted at the current location of the cursor in the script.

\[Omitted image "cpq-scripting-available-functions.png"\] Alt text: Script

As you type in the script editor, suggestions are provided, including functions, configurable field variable names, and local variables. Using this feature helps eliminate mismatched variable names and typing errors. In the screenshot below, typing `Ma` gives the user two available functions \(Map and Math\) and a list of all matching fields. Additional inputs narrow the list of matching options.

\[Omitted image "cpq-scripting-typeahead.png"\] Alt text: Map structure

At the bottom of the scripting interface, the debugger lets you test your script by defining values for the variables \(fields\) that it references. Debugger input is provided in JSON format. For your convenience, review field-specific formats in the fields information help \(arrow\).

\[Omitted image "cpq-scripting-debugger.png"\] Alt text: Help screen

It can be helpful to save your debugger inputs as comments in your script for easy pasting into the debugger when you need to test the script.

Calls to `console.log()` in the script are returned in the debugger output.

Also see the following sample scripts:

-   [Sample Message Script - Array and Map Function](https://docs.google.com/document/d/1SqDGH6Y6UKV-0kGhzuqfGyII1dI2CezzQifEzulNlfY/edit)
-   [Sample Number Field Determination](https://docs.google.com/document/d/1HvC6jybMhpgEgvsPnvlt7kwmiXKTYtVjJqmL3iANiHU/edit)
-   [Sample Product Rule Scripts](https://docs.google.com/document/d/1bSJ_kMcJmHnlH6C67U6tatpxha-EBzyp1IJX5XQ3FYA/edit)
-   [Sample Product Rule Script With For Loop](https://docs.google.com/document/d/1ICHHJVT3ITlbozUIqpMZTEkUEZgEBbwMoiNWAK6JsO8/edit)
-   [Sample Text Field Determination](https://docs.google.com/document/d/1Vgkixyoh4m51UYh1nC60gOyfNZ9-VSZKlU8ojJQuhF0/edit)

**Related topics**  


[CPQ scripting language reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Sample scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/cpq-sample-scripts.md)

[Using comments and the console to debug scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/rules-enrichments-comments-and-console_log.md)

[Scripting: Checking for first and subsequent configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/enrichments_on_configurer_and_reconfigure_behavior.md)

[Scripting: How to populate set values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/enrichments-on-configure-reconfigure-scripts-how-to-populate-set-values.md)

