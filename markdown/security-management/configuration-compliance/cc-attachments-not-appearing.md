---
title: Attachments not appearing after import
description: If attachments are not appearing as expected for data sources or on a security incident after third-party integration imports, check your IP restrictions.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Resolving Qualys Vulnerability Integration issues, Qualys, Integrate, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Attachments not appearing after import

If attachments are not appearing as expected for data sources or on a security incident after third-party integration imports, check your IP restrictions.

IP access restrictions can prevent attachments from being seen unless you are logged in from a safe IP. Since a new attachment is added with each import, this can result in duplicates you have to remove.

For example, when you run a third-party host import integration, if you do not see any attachments on your data sources, check your IP restrictions and add users to the safe list prior to import.

