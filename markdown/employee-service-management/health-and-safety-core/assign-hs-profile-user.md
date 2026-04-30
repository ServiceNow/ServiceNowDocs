---
title: Assign Health and Safety profile to a user
description: Assign the Health and Safety profile to all users in your organization, including employees, visitors, and contractors.
locale: en-US
release: xanadu
product: Health and Safety Core
classification: health-and-safety-core
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure settings, Health and Safety Core, Health and Safety, Employee Service Management]
---

# Assign Health and Safety profile to a user

Assign the Health and Safety profile to all users in your organization, including employees, visitors, and contractors.

## Before you begin

Role required: sn\_ohs\_im.hs\_profile\_writer

## About this task

For more information on Health and Safety user profiles, see [Health and Safety user profile](../concept/health-and-safety-user-profile.md).

**Note:** The **Generate Health And Safety Profiles** scheduled job runs weekly and automatically creates health and safety user profiles for users \[sys\_user\] with an assigned role in any of the Health and Safety applications.

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the configuration icon \(![Configuration icon](../../hs-risk-management/image/icon-config.png)\).

3.  In the **Lists** tab, select **Health and safety profiles** and then **All**.

4.  Select **New**.

5.  On the form, fill in the fields.

    For information on form field descriptions, see [Health and Safety profile form](../reference/hs-health-safety-profile-form.md).

6.  Select **Save**.


## Result

-   The user is listed in the **Health and safety profile** list under **Configuration** on the Health and Safety Workspace.
-   The user profile is saved in the Health and Safety profile \[sn\_ohs\_im\_health\_and\_safety\_profile\] table.

**Parent Topic:**[Setting up Health and Safety Core](../../hs-core/concept/setting-up-hs-core.md)

**Related topics**  


[Install Health and Safety Core](../../hs-core/task/install-hs-core.md)

[Set up your workplace location data](configure-hs-workplace-location-data.md)

[Enable a Health and Safety table for configuring report field mapping](enable-hs-table-report-field-mapping.md)

[Create a safety report field mapping](create-safety-report-field-mapping.md)

[Configure groups for Health and Safety](configure-groups-health-and-safety.md)

[Configure scheduled job to generate frequency rates](configure-job-generate-frequency-rates.md)

[Add a Health and Safety visitor](hs-add-health-safety-visitor.md)

