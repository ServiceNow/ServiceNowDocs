---
title: Resolving duplicate configuration items in Security Posture Control
description: Resolving duplicate entries for configuration items \(CIs\) in your Configuration Management Database ensures that you get accurate audits with your SPC policies.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use the workspace, Security Posture Control, Security Operations]
---

# Resolving duplicate configuration items in Security Posture Control

Resolving duplicate entries for configuration items \(CIs\) in your Configuration Management Database ensures that you get accurate audits with your SPC policies.

## Duplicate configuration items overview

In certain cases, your asset discovery sources, that is, your service graph connector products \(SGCs\), import asset data that might create duplicate entries in your Configuration Management Database \(CMDB\) for assets \(configuration items\). These duplicate CI records occur when two or more assets are listed in your CMDB with the same names, but the CMDB references are different.

An example might be an asset that named by its IP address, `10.0.2.11`, that is listed twice on the CMDB 360 Data \[cmdb\_multisource\_data\] table. One entry for `10.0.2.11` is listed in the CMDB reference column as `10.0.2.11`, and another is listed as `10.0.65.159`. These assets might be from the same Discovery source, an SGC product, or they might be from two or more Discovery sources. In either case, to avoid problems with SPC policies and your asset inventories, you must remove the duplicate CIs.

## Identifying and removing duplicate configuration items

You can identify duplicate CIs by filtering on the Name column on the \[sn\_sec\_spc\_core\_asset\_cache\] table and noting which assets have the same name.

If you identify duplicates, the [CI deduplication](spc-resolve-duplicate-cis.md) process incorporates a deduplication template that you must publish, a system property that you activate, and a scheduled job that removes duplicate CIs in the SPC Cached Assets \[sn\_sec\_spc\_core\_asset\_cache\] table. The process removes duplicates and preserves the master, or canonical, CI record that has the most related items.

