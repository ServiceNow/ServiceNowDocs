---
title: Upload firmware packages
description: If you're using a local repository, upload firmware packages to the Discovery Console for OT so the system knows when an update is needed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Settings page, Use the Console pages, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Upload firmware packages

If you're using a local repository, upload firmware packages to the Discovery Console for OT so the system knows when an update is needed.

## Before you begin

Role required: admin

## Procedure

1.  Obtain the latest firmware packages directly from your Discovery Console for OT account representative.

2.  Navigate to the Settings page and open the **Package** tab.

3.  Select **Import Packages**.

4.  Select the provided firmware package and select **Open** to upload the files.

    The Package Import status modal window tracks the upload status.

5.  Repeat steps 2–4 for each firmware package.


## Result

The Discovery Console for OT verifies the integrity and authenticity of the uploaded file before they're made available for device updates. Packages that fail authenticity checks are automatically rejected during the upload process.

