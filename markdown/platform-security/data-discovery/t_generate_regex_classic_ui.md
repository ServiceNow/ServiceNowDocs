---
title: Using Text to RegEx with the classic UI
description: Use the Generate Regex button and modal in the classic UI to automatically create a regular expression from a text description.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-discovery/t\_generate\_regex\_classic\_ui.html
release: australia
product: Data Discovery
classification: data-discovery
topic_type: task
last_updated: "2026-06-24"
reading_time_minutes: 1
keywords: [generate, regex, classic UI, modal]
breadcrumb: [Configure patterns, Data Discovery jobs, Exploring Data Discovery \(Classic\), Data Discovery, Platform Privacy]
---

# Using Text to RegEx with the classic UI

Use the Generate Regex button and modal in the classic UI to automatically create a regular expression from a text description.

## Before you begin

Before you begin:

-   Vault license is activated in your instance
-   Now Assist for Vault plugin is installed
-   You are working in the classic UI
-   You have access to edit data patterns

Role required:

## About this task

The classic UI provides a Generate Regex button that opens a modal dialog. This dialog guides you through generating a regular expression using Text to RegEx without needing to write regex syntax manually.

## Procedure

1.  Navigate to a data pattern record in the classic UI.

2.  Click the **Generate Regex** button.

    The button is displayed for data patterns that you can edit. Clicking the button opens the Generate Regex modal dialog.

3.  In the modal dialog, enter a natural language description of the regular expression pattern in the text box.

    For example, you might type "Email address", "Credit card number", or "Social security number". Be as specific as possible so the LLM generates an accurate regex.

4.  Click the **Generate** button.

    The system sends your description to an LLM to generate a matching regular expression. If the LLM service is unavailable or encounters an error, an error message is displayed in the modal.

5.  Review the generated regular expression in the modal.

    The LLM provides both the regex and an explanation of what it matches.

6.  If the generated regex is correct for your use case, click the **Accept** button.

    The generated regular expression is copied into the expression field of your data pattern. The modal closes and you return to the data pattern form.

7.  Save the data pattern record to persist your changes.


## Result

The regular expression has been generated and inserted into your data pattern. The pattern is ready to use in your data discovery processes.

## What to do next

Each generated regex that you accept consumes credits from your Assists balance. If the generated regex does not meet your needs, you can use the modal again to generate an alternative expression.

