---
title: Text to RegEx error handling
description: When errors occur during regex generation or testing, Text to RegEx displays an error message to help you understand what went wrong and how to resolve the issue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-discovery/r\_error\_handling.html
release: australia
product: Data Discovery
classification: data-discovery
topic_type: reference
last_updated: "2026-06-24"
reading_time_minutes: 1
keywords: [error, error message, troubleshooting, LLM unreachable]
breadcrumb: [Using Text to RegEx, Create new data pattern, Data Discovery sources, Data Discovery Store, Data Discovery, Platform Privacy]
---

# Text to RegEx error handling

When errors occur during regex generation or testing, Text to RegEx displays an error message to help you understand what went wrong and how to resolve the issue.

## Common error scenarios

The following scenarios can trigger error messages when using Text to RegEx:

## LLM service is unreachable

When clicking Generate or attempt to use Text to RegEx, the configured LLM provider does not respond.

Review the following:

-   Check your network connection to ensure you can reach external services
-   Verify that the LLM provider \(OpenAI, Azure, Google, or Anthropic\) is not experiencing an outage or service disruption
-   Contact your ServiceNow administrator to verify that the LLM provider credentials are correct and that the instance is authorized to call the LLM
-   Try again after a few minutes, as temporary service interruptions may resolve themselves

## LLM returned an unexpected response

The LLM service responds, but the response is not in the expected format or does not contain a valid regular expression.

Review the following:

-   Try again with a different or more specific description of the pattern you need
-   If the error persists, contact your ServiceNow administrator

## License check failed

You do not have the required licenses or plugins to use Text to RegEx. You may receive the error message, "This feature requires an additional license. Please contact procurement."

See [Licensing prerequisites for Text to RegEx](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/data-discovery/r_licensing_prerequisites.md) for details on required licenses and how to request them from your procurement team.

## General troubleshooting

If you encounter an error that is not covered above:

1.  Note the exact error message text.
2.  Take a screen shot if possible.
3.  Check the browser console for any JavaScript errors \(press F12 to open Developer Tools\).
4.  Contact your ServiceNow administrator or support team with the error message and screen shot.

## Logging and diagnostics

When errors occur, the system logs diagnostic information to the table. Administrators can review these logs to diagnose issues.

