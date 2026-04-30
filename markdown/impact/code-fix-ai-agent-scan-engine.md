---
title: Fix code in real-time with Now Assist
description: Fix code in real-time with Now Assist allows developers to receive real-time, AI-driven recommendations within their workspace to identify and resolve code quality issues, enabling adherence to ServiceNow, Inc. leading practices and reducing technical debt proactively.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-11-21"
reading_time_minutes: 1
breadcrumb: [Scan Engine, Platform Health, Using Impact, Impact]
---

# Fix code in real-time with Now Assist

Fix code in real-time with Now Assist allows developers to receive real-time, AI-driven recommendations within their workspace to identify and resolve code quality issues, enabling adherence to ServiceNow, Inc. leading practices and reducing technical debt proactively.

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

If code is misconfigured in those development areas in an instance, Fix code in real-time can be triggered by the developer after a finding is returned for Act or Recommend level findings.

**Note:** Fix code in real-time with Now Assist only displays if there are actual findings for the code, and if there is an Act or Recommend level violation against active Scan Engine definitions.

The agent will not display if:

-   The only finding is at the Recommend level with an approved exception.
-   All findings are filtered out based on the applicable tables.
-   The definition is listed in the exclusion property.

**Related topics**  


[Configure Fix code in real-time for Platform Health](configure-ai-code-fix-for-platform-health.md)

