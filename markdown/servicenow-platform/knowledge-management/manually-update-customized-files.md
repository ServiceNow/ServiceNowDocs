---
title: Manually update customized files
description: If you have customized any of the files that are updated as part of the Knowledge Management Advanced Installer plugin, these files are skipped during plugin activation and must be updated manually.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use article versioning, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Manually update customized files

If you have customized any of the files that are updated as part of the Knowledge Management Advanced Installer plugin, these files are skipped during plugin activation and must be updated manually.

Manually update your customization to include the article versioning-related changes.

-   Add the **Version** field to the Knowledge form layout and the Knowledge list view, if it is not already present.
-   Add the **outdated** choice to the **Workflow** choice list field on the Knowledge form, if it is not already present. Keep the value as **outdated** because of dependencies that article versioning functionalities have on this choice.
-   Update the **Knowledge** &gt; **My Flagged** and **Self-Service** &gt; **My Knowledge Articles** modules to include the following condition in the **Filter** field, if these modules do not already reflect this change: **Revised by is \(dynamic\) me**.

If you have customized any of the Knowledge Management Overview dashboard reports, these files are also skipped during plugin activation and must be updated manually.

**Parent Topic:**[Use article versioning](../concept/use-article-versioning_0.md)

