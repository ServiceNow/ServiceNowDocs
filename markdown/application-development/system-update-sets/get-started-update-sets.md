---
title: General guidelines for planning the update process
description: A reference topic that contains general guidelines to create a standard process for moving customizations from instance to instance.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, System update sets, Deploying applications, Building applications]
---

# General guidelines for planning the update process

A reference topic that contains general guidelines to create a standard process for moving customizations from instance to instance.

-   Use a standard path for update sets: migrate from development to test, then from test to production. Avoid moving the same update set from more than one source.

-   Check that both instances are on the same version. While it is possible to move an update set from an instance on an older version to an instance on a newer version, it increases the likelihood of problems. Customizations may not work if they rely on code that has changed between versions.
-   Change a single update set for each small or medium task. Large update sets with schema changes or major workflow revisions are tougher to review, slower to process, more conflict-prone, and take longer to preview or commit.
-   Ensure that all base system records have consistent sys\_id fields. Certain base system records may be generated on an instance post-provisioning, resulting in differences between instances and potential complications with update sets.

-   Schedule update set commits outside business hours to avoid slowing down the production instance. Any reduced performance is brief.

-   Use clear update set names and establish a naming convention to coordinate developer changes and streamline referencing during commits.
    -   If update sets are being generated as fixes for problems, consider including the problem ticket in the name. For example **PR10005 - Duplicate Email Issues Fix**.
    -   If you need more than one update set to address a problem, include a sequence number in the naming convention. Sequenced naming conventions confirm that update sets are applied in the order that they were created. For example, **PR10005 - Duplicate Email Issues Fix** and **PR10005.2 - Duplicate Email Issues Fix**.

**Parent Topic:**[Update sets reference](update-sets-reference.md)

