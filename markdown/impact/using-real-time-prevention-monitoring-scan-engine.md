---
title: Real-time prevention monitoring for Scan Engine
description: Real-Time Prevention is a Scan Engine feature that actively monitors records as they are created or modified by developers and administrators, displaying real-time finding messages when saving records in any instance where the Scan Engine is installed and activated.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Scan Engine, Platform Health, Using Impact, Impact]
---

# Real-time prevention monitoring for Scan Engine

Real-Time Prevention is a Scan Engine feature that actively monitors records as they are created or modified by developers and administrators, displaying real-time finding messages when saving records in any instance where the Scan Engine is installed and activated.

How it works:

-   **Immediate Detection:** Identifies potential violations in scripts, includes, and other fields at the moment of edit.
-   **On-Screen Alerts:** Displays findings in real-time with severity levels
-   **Guided Resolution:** Provides details, such as line numbers, impact levels, and steps to resolve found issues.
-   **Governance:** Supports exception workflows and links to supporting documentation for compliance.

**Note:** Real-Time Prevention must be enabled in the Scan Engine properties page for this feature to function. For more information, refer to [Configure Scan Engine properties](configure-scan-engine-properties.md).

Findings identified by real-time monitoring can have the following levels.

<table id="table_dlv_bvk_hhc"><thead><tr><th>

Level

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Review

</td><td>

Displays an informational message without blocking saves or creating finding records.

</td></tr><tr><td>

Suggest

</td><td>

Prompts users to check for a better solution if one is available.

</td></tr><tr><td>

Recommend

</td><td>

-   Prevents users from saving the record unless they resolve the issue or provide an exception reason.
-   For more information, refer to [Submit exceptions for the Scan Engine findings](../concept/submitting-exception-reasons-scan-engine.md).

</td></tr><tr><td>

Act

</td><td>

-   Prevents users from saving the record until they fix the code to meet the definition's requirements.
-   No exception reason option is available.
-   An override requires admin-level rights or the disabling of the definition.

</td></tr></tbody>
</table>**Note:** Depending on the level of the definition, users may be required to fix a finding before saving a record.

