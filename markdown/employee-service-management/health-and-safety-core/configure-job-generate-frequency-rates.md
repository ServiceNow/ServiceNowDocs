---
title: Configure scheduled job to generate frequency rates
description: Configure the scheduled job to load the safety frequency rates and ensure that the safety metrics on the Health and Safety Workspace landing page are up to date.
locale: en-US
release: australia
product: Health and Safety Core
classification: health-and-safety-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Health and Safety Core, Health and Safety, Employee Service Management]
---

# Configure scheduled job to generate frequency rates

Configure the scheduled job to load the safety frequency rates and ensure that the safety metrics on the Health and Safety Workspace landing page are up to date.

## Before you begin

Ensure that the application scope is selected as Health and Safety Incident Management PA Content Pack. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=australia&pubname=australia-application-development&ft:locale=en-US).

Role required: sn\_ohs\_im.admin

## About this task

The **\[OHS\] Safety Metrics** job is set to run daily by default.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Jobs**.

2.  Search and open the **\[OHS\] Safety Metrics** scheduled job.

3.  In the **Run** field, set the frequency of the scheduled job.

4.  To activate the scheduled job, select the **Active** check box.

5.  Select **Update**.

    **Note:** To run the scheduled job and update metrics on demand, select **Execute Now**.


**Parent Topic:**[Setting up Health and Safety Core](../../hs-core/concept/setting-up-hs-core.md)

**Parent Topic:**[Setting up Health and Safety Incident Management](../concept/setting-up-hs-incident-mgmt.md)

**Related topics**  


[Install Health and Safety Core](../../hs-core/task/install-hs-core.md)

[Workplace location data](configure-hs-workplace-location-data.md)

[Enable a Health and Safety table for configuring report field mapping](enable-hs-table-report-field-mapping.md)

[Create a safety report field mapping for generating reports](create-safety-report-field-mapping.md)

[Configure groups for Health and Safety](configure-groups-health-and-safety.md)

[Assign Health and Safety profile to a user](assign-hs-profile-user.md)

[Add a Health and Safety visitor](hs-add-health-safety-visitor.md)

[Migrate existing safety documents to the Document library](../../hs-core/task/hs-migrate-sync-existing-safety-document-docs-library.md)

