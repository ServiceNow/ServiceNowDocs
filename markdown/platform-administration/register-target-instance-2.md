---
title: System property error
description: Troubleshoot a system property error that occurs while registering a target instance.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Troubleshooting for registering target instance, Reference, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# System property error

Troubleshoot a system property error that occurs while registering a target instance.

## Condition

By default, `glide.db.clone.allow_clone_target` is enabled on instances whose name ends in Dev, Test, Stage, UAT, or QA. An error occurs if the property isn't set to `True`.

**Note:** If it's a production instance, set this property back to `False` to avoid accidental clones over production in future.

## Cause

The `glide.db.clone.allow_clone_target` system property is set to `False`.

## Remedy

## Procedure

1.  Navigate to **All** &gt; **System properties** &gt; **All properties**.

2.  Search for `glide.db.clone.allow_clone_target` in the system properties list.

3.  Select the property.

4.  If the value is set to `False`, set the value to `True`.

5.  Select **Update**.


**Parent Topic:**[Troubleshooting for registering target instance](register-target-instance-troubleshooting.md)

