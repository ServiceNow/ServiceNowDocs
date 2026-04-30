---
title: Import sets maximum row size
description: Rows imported using import sets must not exceed the maximum row size.
locale: en-US
release: zurich
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Import sets, Imports, Workflow Data Fabric]
---

# Import sets maximum row size

Rows imported using import sets must not exceed the maximum row size.

A single row in a database may not contain more than 8126 bytes of data. The size of each row is determined by the amount of content in all fields, as well as the character set for text fields. For example, a row with 10 text fields each containing 1000 characters using a French character set takes 15360 bytes.

Attempting to import more data to a single row than the maximum size causes the import to skip that row. Any rows that were skipped for this reason are listed in the import log.

