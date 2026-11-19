---
title: Using comments and the console to debug scripts
description: Learn how comments and the console can help you debug your scripts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/rules-enrichments-comments-and-console\_log.html
release: zurich
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 2
breadcrumb: [Setting up enrichments and rules scripting, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Using comments and the console to debug scripts

Learn how comments and the console can help you debug your scripts.

ServiceNow CPQ has several areas where the admin can use scripts to define behavior. These include advanced conditions for rules, advanced actions for rules, and enrichments.

## Advanced conditions for rules

\[Omitted image "cpq-rules-advanced-conditions.png"\] Alt text: Advanced conditions for Rules

## Advanced actions for rules

\[Omitted image "cpq-rules-advanced-actions.png"\] Alt text: Advanced conditions for Rules

## Enrichments

\[Omitted image "cpq-rules-enrichments.png"\] Alt text: Enrichments

This article highlights a few key features to help you test and prepare your code before you deploy it in a blueprint.

**Note:** The scripting language in ServiceNow CPQ is JavaScript-like, meaning it follows JavaScript-style syntax but lacks the full capabilities of JavaScript.

## Console.log

When the admin starts to write a script, the ServiceNow CPQ Admin looks like this:

\[Omitted image "cpq-scripting-console-1.png"\] Alt text: Console.log

Clicking **Run Debugger** in the lower panel raises the debugger and the Debugger Output section. This section is also called the console.

This box shows the output of the script based on the script and the inputs added to the debugger \(if applicable\). For example, the BOM enrichment script shows the updated BOM based on the enrichment and inputs put in the debugger.

Lines of code can be logged to the console. So, you can send text to the console, as in the following:

\[Omitted image "cpq-scripting-console-2.png"\] Alt text: Console.log

You can also log variables, which is helpful to make sure your script is working correctly. You can add text to the log to help the lines of code stand out:

\[Omitted image "cpq-scripting-console-3.png"\] Alt text: Console.log

## Comments

Comments are lines of code that the script ignores. Comments have a few uses. First, it is very helpful to future coders \(and to you, when you revisit the code much later\) if you have commented on how and why you coded lines of the script as you did. Commenting can also be used to save code to use again. And if you do not use a block of code but may want to use it later, you can comment it so it does not affect your current work.

You can write comments on a single line or across multiple lines.

To add single-line comments, use two slashes. Anything written after the slashes on the same line is ignored by the script.

`// This comment is ignored by the script`

However, any code before the slashes is still executed. For example, in the image below, the variable `be4comment` remains 12345, as the script ignores the comment "67890" following the slashes.

\[Omitted image "cpq-scripting-comments-single-line.png"\] Alt text: Comments

To create a multiline comment, add a slash and an asterisk before the comment. Add an asterisk and a slash after the comment.

```
/*
Your comment goes here.
It can span multiple lines.
*/
```

When you add a multiline comment, be careful not to comment out important elements such as closing brackets, parentheses, or return statements.

\[Omitted image "cpq-scripting-comments-multi-line.png"\] Alt text: Comments

When you frequently revisit or modify a rule that takes inputs from many other fields, it can be helpful to paste the input into the debugger section as a multiline comment. This way, when you return to work on the rule later, you won't need to rewrite the inputs.

```
/* inputs
{"Field1": "testValue1",
    "Field2Quantity": 2,
      "Field3": "testValue3"
    },
*/
```

