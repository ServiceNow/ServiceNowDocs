---
title: Duplicate software installations in the Software Asset Management application
description: Duplicate software installation are created when you discover software installations with the same publisher, product, version, and edition through multiple discovery sources.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Software discovery and normalization, Explore, Software Asset Management, IT Asset Management]
---

# Duplicate software installations in the Software Asset Management application

Duplicate software installation are created when you discover software installations with the same publisher, product, version, and edition through multiple discovery sources.

A software installation record is created for each software record in the Software Installation \[cmdb\_sam\_sw\_install\] table.

By default, the Software Asset Management application prioritizes IBM software installations that are discovered through ServiceNow discovery. Duplicate entries are initially marked as false in the Active column in the Software Installation \[cmdb\_sam\_sw\_install\] table. When the **SAM - Deduplicate Install Table** scheduled job runs, records for all IBM software installations that are discovered through ServiceNow discovery are marked as active, while records for the same software installations that are discovered through an authorized Software Asset Management discovery provider are marked as inactive.

The **SAM - Deduplicate Install Table** scheduled job ensures that only one software installation record is marked as active and included in reconciliation.

**Parent Topic:**[Software discovery and normalization](c_SAMDiscovery.md)

