---
title: Signature Verification Status
description: View the status of valid, invalid, and missing signatures across different applications to assess code signing coverage. Use this information to identify areas that may require additional attention or action.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Health and Status Dashboard, Code Signing, Platform Security]
---

# Signature Verification Status

View the status of valid, invalid, and missing signatures across different applications to assess code signing coverage. Use this information to identify areas that may require additional attention or action.

The Signature Verification Status dashboard displays the following reports:

<table id="table_w3q_t1h_cfc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Script name

</td><td>

Text field

</td><td>

Identifier or title assigned to a specific script within the system.

</td></tr><tr><td>

Type

</td><td>

Text field

</td><td>

Category of the script within the system. It helps define the role and functionality of the script.Example:

-   Business rule
-   Script include
-   Client script
-   Flow action

</td></tr><tr><td>

Application

</td><td>

Text field

</td><td>

Module or area within the system where the script is applied.Example:

-   User management
-   Reporting
-   Form validation
-   Workflow
-   Notifications

</td></tr><tr><td>

Status

</td><td>

Text field

</td><td>

Indicates the current verification status of the script signature.

 -   **Valid**: The script signature is verified and is trusted.
-   **Invalid**: The script signature isn’t verified or is deemed untrusted.
-   **Missing**: The source document is eligible for signing but doesn't have a signature yet. Use this status to identify eligible records that remain unsigned and require code signing.

</td></tr><tr><td>

Last scanned

</td><td>

Text field

</td><td>

Date and time when the script was last scanned for signature verification in the format: `DD/MM/YY/H:S (Day/Month/Year/Hour:Minute)`

</td></tr></tbody>
</table>**Parent Topic:**[Code Signing Health and Status Dashboard](code-signing-health-and-status-dashboard.md)

