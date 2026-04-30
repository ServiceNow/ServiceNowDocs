---
title: Discovered Items for Configuration Compliance
description: Assets are automatically matched to configuration items \(CIs\) using CI lookup rules, when they are imported using the host and test results integrations. Discovered Items give you visibility into how asset identification is mapped to CIs in the CMDB.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuration Compliance imported data, Explore, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Discovered Items for Configuration Compliance

Assets are automatically matched to configuration items \(CIs\) using CI lookup rules, when they are imported using the host and test results integrations. Discovered Items give you visibility into how asset identification is mapped to CIs in the CMDB.

Discovered Items are considered **Matched**, **Unmatched**, or **Reclassified**. Identified CIs are in the **Matched** state.

To make it easier to find potential matching issues, the CI Lookup Rule that matched the CI appears in the **CI matching rule** field.

**Note:** **CI matching rule** field support is available only for the Qualys integration.

If a match was not found, a CI is created in the Unmatched CI class `[sn_sec_cmn_unmatched_ci]`, `[cmdb_ci_unclassed_hardware]`, or `[cmdb_ci_incomplete_ip]` of the CMDB. If the original unmatched CI was reclassified, Discovered item records are updated to reflect that state. For more information, see [Unmatched CIs](../../vulnerability-response/concept/unmatchedCIs.md) and [View and reclassify unmatched configuration items](../../vulnerability-response/task/view-discovered-items.md) for more information.

By default, the **Security Operations** &gt; **CMDB** &gt; **Discovered Items** module lists unmatched configuration items. You can view all discovered items from an import by removing the filter.

For a description of the fields in Discovered Items, see [Discovered Items form fields](../../vulnerability-response/reference/discovered-items-fields.md).

