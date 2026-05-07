---
title: Real-time prevention monitoring for Scan Engine
description: Real-time prevention monitoring is a Scan Engine feature that actively monitors records as they are created or modified, displaying finding messages in real time when saving records in any instance where the Scan Engine is installed and activated.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-13"
reading_time_minutes: 3
breadcrumb: [Scan Engine, Platform Health, Using Impact, Impact]
---

# Real-time prevention monitoring for Scan Engine

Real-time prevention monitoring is a Scan Engine feature that actively monitors records as they are created or modified, displaying finding messages in real time when saving records in any instance where the Scan Engine is installed and activated.

Real-time prevention monitoring provides the following capabilities:

-   **Immediate detection:** Identifies potential violations in scripts, includes, and other fields at the moment of edit.
-   **On-screen alerts:** Displays findings in real time with severity levels.
-   **Guided resolution:** Provides details such as line numbers, impact levels, and steps to resolve found issues.
-   **Governance:** Supports exception workflows and links to supporting documentation for compliance.

**Note:** Real-time prevention monitoring must be enabled on the Scan Engine properties page for this feature to function. For more information, refer to [Configure Scan Engine properties](../task/configure-scan-engine-properties.md).

## Finding levels

Findings identified by real-time monitoring are assigned one of four levels. Review and Suggest level findings are shown in blue. Recommend and Act level findings are shown in red.

<table id="table_finding_levels"><thead><tr><th>

Level

</th><th>

Color

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Act

</td><td>

Red

</td><td>

-   Prevents users from saving the record until they fix the code to meet the definition's requirements.
-   No exception reason option is available.
-   An override requires admin-level rights or disabling of the definition.

</td></tr><tr><td>

Recommend

</td><td>

Red

</td><td>

-   Prevents users from saving the record unless they resolve the issue or provide an exception reason.
-   For more information, refer to [Submit exceptions for the Scan Engine findings](submitting-exception-reasons-scan-engine.md).

</td></tr><tr><td>

Suggest

</td><td>

Blue

</td><td>

-   Prompts users to check for a better solution if one is available.
-   Select whether to Exclude suggestion finding, which when enabled hides Suggestion level findings messages from displaying onLoad of a form, so the blocking messages display for the object when real-time validation is enabled.

</td></tr><tr><td>

Review

</td><td>

Blue

</td><td>

Displays an informational message without blocking saves or creating finding records.

</td></tr></tbody>
</table>**Note:** Depending on the level of the definition, users may be required to fix a finding before saving a record.

## Finding information window

When a finding is detected, an information window displays. The fields shown depend on the severity of the finding.

<table id="table_finding_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Finding level

</td><td>

The severity level of the finding and a brief description.

</td></tr><tr><td>

Details

</td><td>

Generally, the line number the finding occurred on.

</td></tr><tr><td>

Steps to resolve issue

</td><td>

Suggested steps the developer can follow to resolve the finding.

</td></tr><tr><td>

Exception reason required

</td><td>

For Recommend level findings, reminds developers they can submit an exception if they believe the issue is not a valid finding.

</td></tr><tr><td>

Supporting documentation

</td><td>

-   If the definition contains a **Supporting documentation** link, it appears here as a hyperlink that opens in a new browser tab.
-   This can link to documentation, knowledge base articles, FAQs, and more.

</td></tr><tr><td>

Impact

</td><td>

-   Lists the finding's impact level and **Impact to instance** for the associated definition.
-   The impact to instance is a number between 1 and 10, where 10 is the most impactful.

</td></tr></tbody>
</table>## Resolving a finding

Using the information provided in the finding window, you can do one of the following:

-   Correct the issue. If the issue is corrected, the Scan Engine will not return a new finding notice.
-   For Recommend level findings, submit an exception reason, then select **Update**. See [Submit exceptions for the Scan Engine findings](submitting-exception-reasons-scan-engine.md).

## Configuration

Real-time messaging enforcement can be disabled on the Scan Engine properties page. When enforcement is disabled, users see the messaging but are not required to make corrections for Act and Recommend findings.

Visibility of real-time messaging can also be configured to limit which users receive finding notifications. You can restrict messaging to a specific group if necessary.

For more information, refer to [Configure Scan Engine properties](../task/configure-scan-engine-properties.md).

