---
title: Fix code in real-time with Now Assist
description: Fix code in real-time with Now Assist allows developers to receive real-time, AI-driven recommendations within their workspace to identify and resolve code quality issues, enabling adherence to ServiceNow, Inc. leading practices and reducing technical debt proactively.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/code-fix-ai-agent-scan-engine.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Prevent and resolve technical debt, Platform Health, Using Impact, Impact]
---

# Fix code in real-time with Now Assist

Fix code in real-time with Now Assist allows developers to receive real-time, AI-driven recommendations within their workspace to identify and resolve code quality issues, enabling adherence to ServiceNow, Inc. leading practices and reducing technical debt proactively.

Fix code in real-time with Now Assist provides the following capabilities:

-   Immediate detection: Identifies potential violations in scripts, includes, and other fields at the moment of edit.
-   On-screen alerts: Displays findings in real-time with severity levels.
-   Guided resolution: Provides details such as line numbers, impact levels, and steps to resolve found issues.
-   Governance: Supports exception workflows and links to supporting documentation for compliance.

**Note:** Real-time prevention monitoring must be enabled on the Scan Engine properties page for this feature to function. For more information, refer to [Configure Fix code in real-time for Platform Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-ai-code-fix-for-platform-health.md).

When working with ServiceNow code, the following development areas are supported with the Fix code in real-time with Now Assist feature:

-   Scheduled script execution \(`sysauto_script`\)
-   Script action \(`sysevent_script_action`\)
-   Business rule \(`sys_script`\)
-   Client script \(`sys_script_client`\)
-   Catalog client scripts \(`catalog_script_client`\)
-   Email script \(`sys_script_email`\)
-   Script include \(`sys_script_include`\)
-   Transform script \(`sys_transform_script`\)
-   List client script \(`sys_ui_list_script_client`\)
-   UI script \(`sys_ui_script`\)

## Finding levels

Findings identified by real-time monitoring are assigned a specific level. Depending on the level of the definition, users may be required to fix a finding before saving a record.

<table id="table_finding_levels"><thead><tr><th>

Level

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Act

</td><td>

-   Prevents users from saving the record until they fix the code to meet the definition's requirements.
-   No exception reason option is available.
-   An override requires admin-level rights or the disabling of the definition.

</td></tr><tr><td>

Recommend

</td><td>

-   Prevents users from saving the record unless they resolve the issue or provide an exception reason.
-   For more information, refer to [Submit exceptions for Scan Engine findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/submitting-exception-reasons-scan-engine.md).

</td></tr><tr><td>

Suggest

</td><td>

Prompts users to check for a better solution if one is available.

</td></tr><tr><td>

Review

</td><td>

Displays an informational message without blocking saves or creating finding records.

</td></tr></tbody>
</table>If code is misconfigured in those development areas in an instance, Fix code in real-time can be triggered by the developer after a finding is returned for Act or Recommend level findings.

**Note:** Fix code in real-time with Now Assist only displays if there are actual findings for the code, and if there is an Act or Recommend level violation against active Scan Engine definitions.

The agent will not display if:

-   The only finding is at the Recommend level with an approved exception.
-   All findings are filtered out based on the applicable tables.
-   The definition is listed in the exclusion property.

## Findings panel

When findings are detected, a summary banner displays at the top of the form listing the number and types of findings. The Findings panel is a slide-in side panel that displays alongside the development workspace and remains visible until dismissed. Findings are organized into tabs by level with a total count shown on each tab. Within each tab, findings are ordered by impact level.

Each finding card displays the finding level, impact level, a link to the Scan Engine definition, the line number where the issue occurred, steps to resolve the issue, and a link to supporting documentation. For Recommend level findings, a **Create exception** button is embedded directly on the card. See [Submit exceptions for Scan Engine findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/submitting-exception-reasons-scan-engine.md) for details.

When findings are resolved, a blue banner displays a summary of the resolved issues, and the summary banner and Findings panel update to reflect the remaining finding counts.

**Related topics**  


[Configure Fix code in real-time for Platform Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-ai-code-fix-for-platform-health.md)

[Work with Scan Engine findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/work-with-scan-engine-findings.md)

