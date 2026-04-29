---
title: Add a Health and Safety visitor
description: Create a record for a Health and Safety visitor so that they can be easily referenced in the Visitor field on related records.
locale: en-US
release: australia
product: Health and Safety Core
classification: health-and-safety-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Health and Safety Core, Health and Safety, Employee Service Management]
---

# Add a Health and Safety visitor

Create a record for a Health and Safety visitor so that they can be easily referenced in the **Visitor** field on related records.

## Before you begin

Role required: sn\_ohs\_im.hs\_profile\_writer

## About this task

A visitor is a person from outside the organization who came to visit the site.

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the configuration icon \(![Configuration icon](../../hs-risk-management/image/icon-config.png)\).

3.  In the **Configuration** tab, select **Health and safety visitors** and then **All**.

4.  Select **New**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |First name|Visitor's first name.|
    |Middle name|Visitor's middle name.|
    |Last name|Visitor's last name.|
    |Visitor ID|System-generated ID for the visitor.|
    |Phone number|Visitor's contact number.|
    |Company|Organization that the visitor works for.|
    |Email|Visitor's email address.|

6.  Select **Save**.

    A Visitor ID is generated for the visitor.

7.  Assign the Health and Safety user profile to the visitor record.

    For more information, see [Assign Health and Safety profile to a user](assign-hs-profile-user.md).

    **Note:** Only a visitor with the assigned Health and Safety profile is available to select in the **Visitor** field on a form.


## Result

-   The visitor is listed in the **Health and safety visitors** list under **Configuration** and is saved in the Health and Safety visitor \[sn\_ohs\_im\_health\_and\_safety\_visitor\] table.

    **Note:** If the Workplace Visitor Management \(com.sn\_wsd\_visitor\) application is also installed on your instance, then the list of WSD visitors from the Visitor \[sn\_wsd\_visitor\_visitor\] table is automatically synchronized with the Health and Safety visitors list in the Health and Safety visitor \[sn\_ohs\_im\_health\_and\_safety\_visitor\] table. So, the WSD visitors also show up in the **Health and safety visitors** list and should be assigned the Health and Safety user profile.

-   The visitor's Health and Safety user profile is saved in the Health and Safety profile \[sn\_ohs\_im\_health\_and\_safety\_profile\] table.
-   The visitor is available to be referenced in the **Visitor** field on Health and Safety records such as safety incidents that the visitor is involved in.

**Parent Topic:**[Setting up Health and Safety Core](../../hs-core/concept/setting-up-hs-core.md)

**Related topics**  


[Install Health and Safety Core](../../hs-core/task/install-hs-core.md)

[Workplace location data](configure-hs-workplace-location-data.md)

[Enable a Health and Safety table for configuring report field mapping](enable-hs-table-report-field-mapping.md)

[Create a safety report field mapping for generating reports](create-safety-report-field-mapping.md)

[Configure groups for Health and Safety](configure-groups-health-and-safety.md)

[Configure scheduled job to generate frequency rates](configure-job-generate-frequency-rates.md)

[Assign Health and Safety profile to a user](assign-hs-profile-user.md)

[Migrate existing safety documents to the Document library](../../hs-core/task/hs-migrate-sync-existing-safety-document-docs-library.md)

