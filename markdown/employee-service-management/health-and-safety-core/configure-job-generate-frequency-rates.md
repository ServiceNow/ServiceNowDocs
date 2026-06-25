---
title: Configure scheduled job to generate frequency rates
description: Configure the scheduled job to load the safety frequency rates and ensure that the safety metrics on the Health and Safety Workspace landing page are up to date.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/health-and-safety-core/configure-job-generate-frequency-rates.html
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

Ensure that the application scope is selected as Health and Safety Incident Management PA Content Pack. For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationPicker.md).

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


**Parent Topic:**[Setting up Health and Safety Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety-core/setting-up-hs-core.md)

**Parent Topic:**[Setting up Health and Safety Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety-incident-management/setting-up-hs-incident-mgmt.md)

**Related topics**  


[Install Health and Safety Core]()

[Workplace location data]()

[Enable a Health and Safety table for configuring report field mapping]()

[Create a safety report field mapping for generating reports]()

[Configure groups for Health and Safety]()

[Assign Health and Safety profile to a user]()

[Add a Health and Safety visitor]()

[Migrate existing safety documents to the Document library]()

