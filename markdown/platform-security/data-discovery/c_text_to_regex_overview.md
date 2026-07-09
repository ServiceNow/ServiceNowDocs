---
title: Using Text to RegEx
description: Text to RegEx is an AI-powered capability that automatically generates regular expressions from natural language descriptions, helping you create data patterns without manual regex syntax.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-discovery/c\_text\_to\_regex\_overview.html
release: australia
product: Data Discovery
classification: data-discovery
topic_type: concept
last_updated: "2026-06-24"
reading_time_minutes: 1
keywords: [text to regex, regular expression, AI-generated, data patterns, data discovery]
breadcrumb: [Create new data pattern, Data Discovery sources, Data Discovery Store, Data Discovery, Platform Privacy]
---

# Using Text to RegEx

Text to RegEx is an AI-powered capability that automatically generates regular expressions from natural language descriptions, helping you create data patterns without manual regex syntax.

**Important:**

Text to RegEx requires a license. You must have Vault license and Now Assist for Vault plugin installed to access this feature. Verify with your organization that you have the appropriate licenses before using this capability.

## What is Text to RegEx

Text to RegEx leverages large language models \(LLMs\) to interpret natural language descriptions and automatically generate corresponding regular expressions. Instead of manually writing complex regex syntax, you provide a description of the pattern you need, and the system generates the regex for you.

**Note:**

Each generated regex consumes credits from your Assists balance when you accept and save the pattern.

## Key benefits

-   Eliminates the need to manually write regular expression syntax
-   Provides AI-generated explanations alongside each regex, so you understand what the pattern does
-   Includes a built-in test mode to verify your generated regex before saving
-   Supports multiple LLM providers for flexibility and reliability

## How it works

The Text to RegEx workflow consists of three steps:

1.  Generate: Enter a natural language description of the pattern you need \(for example, "Email ID"\). The system uses an LLM to generate a regular expression that matches that pattern.
2.  Test: Review the generated regex and test it against sample data using keyword and keyword proximity options to verify it works as expected.
3.  Accept: If the regex meets your needs, accept it to save the data pattern. The generated regex is then available for use in your data discovery workflows.

You can access Text to RegEx with the Next Experience UI. It is integrated directly into the data pattern form with dedicated Generate Regex and Test buttons.

