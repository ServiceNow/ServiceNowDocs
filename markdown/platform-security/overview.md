---
title: Overview Dashboard
description: The Overview dashboard provides a centralized view of your Code Signing environment, offering real-time insights into key components and their status.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Health and Status Dashboard, Code Signing, Platform Security]
---

# Overview Dashboard

The Overview dashboard provides a centralized view of your Code Signing environment, offering real-time insights into key components and their status.

The Overview dashboard displays the following reports:

<table id="table_w3q_t1h_cfc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enterprise plugin

</td><td>

Text field

</td><td>

Status of essential plug-ins and system properties required for Code Signing functionality. **Enterprise plugin** displays the core plugin needed for signing operations.

</td></tr><tr><td>

Opt-in property

</td><td>

Text field

</td><td>

Configuration flag that enables Code Signing capabilities.

**Note:** This setting must be **Active** to confirm that code signing functions according to the specific requirement.

</td></tr><tr><td>

Signature validation status

</td><td>

Text field

</td><td>

Indicates whether signature validation is enforced during code execution to verify that only the trusted scripts are executed.

</td></tr><tr><td>

Signature states

</td><td>

Pie chart

</td><td>

Comprehensive overview of all the script signatures, including their current validation status. The signatures are categorized into:

 -   **Trusted** signatures are valid and associated with trusted code signing certificate.

-   **Untrusted** signatures fail validation or are linked to untrusted verification certificate.

-   **Orphan** signatures are present but no longer linked to a known or active certificate.


 **Note:** Use this information to assess script integrity and take corrective action as needed.

</td></tr><tr><td>

MID Server configuration state

</td><td>

Pie chart

</td><td>

Status and trust relationship of all the MID Servers in your instance. Use this section to view the total number of MID Servers and check their status.

 -   **Active MID Servers**: The number of servers that are currently running and successfully connected.

-   **Inactive MID Servers**: The number of servers that aren’t running or are disconnected.


</td></tr><tr><td>

Signed records by type

</td><td>

Pie chart

</td><td>

Distribution of signed records by record type, showing the percentage coverage across the following categories:

 -   **Business Rules**: The percentage of signed business rule records.
-   **Script Includes**: The percentage of signed script include records.
-   **Others**: The percentage of signed records in other supported categories.

</td></tr><tr><td>

Signed records by application

</td><td>

Pie chart

</td><td>

Distribution of signed records across different application modules, showing the percentage of code signing coverage.

 -   **User Management**: Percentage of signed records in the User Management module.
-   **Form Validation**: Percentage of signed records related to form validation.
-   **Others**: Percentage of signed records in all other application modules.

</td></tr></tbody>
</table>**Parent Topic:**[Code Signing Health and Status Dashboard](code-signing-health-and-status-dashboard.md)

