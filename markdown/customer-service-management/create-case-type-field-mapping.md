---
title: Create a table map for case types
description: Create table maps to configure the case type fields that are copied from a case record to the post case review or the case action summary records.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure case digests, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create a table map for case types

Create table maps to configure the case type fields that are copied from a case record to the post case review or the case action summary records.

## Before you begin

Role required: admin

## About this task

Case Type tables extend from the Case table but do not inherit the table mappings.

## Procedure

1.  Access the CSM Table Map list by navigating to **csm\_table\_map\_list.do**.

2.  Create two new table map records in the Case Digest scope, one for the post case review mapping and one for the case action summary mapping.

3.  In the first record:

    1.  Select the desired Case Type table in the **Source Table** field.

    2.  Select the Post Case Review \(sn\_csm\_case\_digest\_pcr\) table in the **Target Table** field.

    3.  Click **Submit**.

4.  In the second record:

    1.  Select the desired Case Type table in the **Source Table** field.

    2.  Select the Case Action Summary \(sn\_csm\_case\_digest\_cas\) table in the **Target Table** field.

    3.  Click **Submit**.

5.  For the two new case type table map records, map the fields from the source table to the target table in the Basic Field Mapping form section.

    For details, see Create a case digest table map.

6.  Click **Update**.


