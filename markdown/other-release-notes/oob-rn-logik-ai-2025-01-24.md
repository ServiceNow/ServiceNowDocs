---
title: Logik.ai 2025/01/24 release notes
description: Logik.ai 2025/01/24 release notes include minor bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2025-01-24.html
release: other
topic_type: reference
last_updated: "2025-11-25"
reading_time_minutes: 1
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2025/01/24 release notes

Logik.ai 2025/01/24 release notes include minor bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, Jan 23, 2025, 8 pm CT|
|Test|Thursday, Feb 06, 2025, 8 pm CT|
|Prod|Friday, Feb 21, 2025, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Feb 21, 2025.

## Release notes

This release version includes the following fixes.

|Fix|Short description|
|---|-----------------|
|LGK-14358|Added performance optimizations to initialization and configuration flows for complex configurations. This will help mitigate INIT and PATCH call latency that customers were facing.|
|LGK-14581|When a product picker Bulk Action references fields that are not added to the Blueprint, the Blueprint was skipping to validate all the product picker rules. This has been fixed so that the full list of Bulk Actions is processed when the Blueprint is compiled.|
|LGK-14587|When using Dynamic Options for Nested Bundles with Solution Configuration, products that were removed on reconfiguration were not removed from the Salesforce Quote Lines when the reconfiguration was saved. This has been fixed.|
|LGK-14792|Added Tooltip messages for the Select column of a product picker grid.|
|LGK-14918|In some scenarios, product picker selections were not saved on reconfigure. This has been corrected.|

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

