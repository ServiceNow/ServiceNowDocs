---
title: Dynamic artifact detection in Localization Workspace
description: With Dynamic artifact detection, Localization Workspace identifies all translatable content, including your custom artifacts.
locale: en-US
release: zurich
product: Localization Workspace
classification: localization-workspace
topic_type: concept
last_updated: "2025-12-04"
reading_time_minutes: 1
breadcrumb: [Exploring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer]
---

# Dynamic artifact detection in Localization Workspace

With Dynamic artifact detection, Localization Workspace identifies all translatable content, including your custom artifacts.

When you create translation requests, your custom artifacts can be selected in the [content type](../task/lw-request-translations-types.md) stage. All untranslated or partially translated documents in the artifact's table are retrieved and displayed to you.

To make custom artifacts \(content types\) available for selection, you must configure them as follows.

-   Create your translation artifact in the Artifact Configurations \[sn\_lf\_config\] table. For details see [Create and configure a custom artifact](../../localization-framework/task/create-configure-custom-artifact.md).
-   You must set Cross-scope privileges for your artifact's table and processor script. For information, see [Cross-scope privileges for Localization Workspace](../task/lw-cross-scope-privilege.md).
-   You may also need to set Restricted Caller Access for artifact resources. For information, see [Restricted Caller Access for Localization Workspace](../task/lw-restricted-caller-access.md).

Some preconfigured artifact types are already available when you install Localization Workspace. For information about translation artifacts that are available by default, see [Types of Localizable content in Localization Workspace](../reference/lw-localizable-content.md).

For examples of Localization Framework artifacts that you can set up, see the LF Artifact blog posts list on [https://www.servicenow.com/community/international-localization/need-to-translate-a-par-dashboard-check-this/ta-p/2839751](https://www.servicenow.com/community/international-localization/need-to-translate-a-par-dashboard-check-this/ta-p/2839751) in the ServiceNow Community. These examples include Processor scripts.

