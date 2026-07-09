---
title: Generate a regular expression using the discovery UI
description: Use the Text to RegEx feature in the discovery UI to automatically generate a regular expression from a natural language description of the pattern you need.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-discovery/t\_generate\_regex\_discovery\_ui.html
release: australia
product: Data Discovery
classification: data-discovery
topic_type: task
last_updated: "2026-06-24"
reading_time_minutes: 2
keywords: [generate, regex, discovery UI, data pattern]
breadcrumb: [Using Text to RegEx, Create new data pattern, Data Discovery sources, Data Discovery Store, Data Discovery, Platform Privacy]
---

# Generate a regular expression using the discovery UI

Use the Text to RegEx feature in the discovery UI to automatically generate a regular expression from a natural language description of the pattern you need.

## Before you begin

Before you begin:

-   Vault license is activated in your instance
-   Now Assist for Vault plugin is installed
-   You have access to create or edit data patterns

Role required:

## About this task

When you need to create a regular expression but do not want to manually write regex syntax, use the Text to RegEx feature. This feature is available on the record-view and new-record pages for data patterns. The feature guides you through a three-step workflow: generate, test, and accept.

## Procedure

1.  Open or create a data pattern record in the discovery UI.

    You can create a new data pattern or edit an existing one.

2.  Click the **Generate Regex** button.

    The button appears only for data patterns that can be edited. If you see a grayed-out button, check that you have the required license and permissions.

3.  In the Generate Regex modal, enter a natural language description of the pattern you need in the text area.

    For example, type "Email ID", "Phone number", or "IP address". The LLM uses this description to generate an appropriate regex.

4.  Click the **Generate** button.

    The system calls the LLM to generate the regex and a natural language explanation. If an error occurs \(for example, if the LLM service is unreachable\), an error message appears on the screen.

5.  Review the generated regular expression and its explanation.

    The explanation helps you understand what the regex pattern matches and why it was generated for your description.

6.  To verify the regex works correctly, click **Next** to proceed to the test step.

    Proceeding to the test step is optional but recommended to validate the regex against sample data before saving.

7.  In the Test step, enter keywords and keyword proximity values if needed, then click **Test**.

    This allows you to verify that the generated regex correctly matches your test data under the conditions you specify.

8.  After testing, click **Next** to proceed to the Accept step.

9.  In the Accept step, review your data pattern configuration and click **Accept** to save the pattern.

    If this is a new record, a new data pattern is created. If you are editing an existing pattern, the pattern is updated with the generated regex.

10. The generated regex is now saved and available for use in your data discovery workflows.


## Result

You have successfully generated and saved a regular expression using Text to RegEx. The regex is now associated with your data pattern and can be used to identify matching data in your discovery scans.

## What to do next

Each time you accept and save a generated regex, credits from your Assists balance are consumed. Monitor your Assists balance to ensure you have sufficient credits for future Text to RegEx operations.

