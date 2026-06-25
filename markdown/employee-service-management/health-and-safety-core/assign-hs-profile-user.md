---
title: Assign Health and Safety profile to a user
description: Assign the Health and Safety profile to all users in your organization, including employees, visitors, and contractors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/health-and-safety-core/assign-hs-profile-user.html
release: australia
product: Health and Safety Core
classification: health-and-safety-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Health and Safety Core, Health and Safety, Employee Service Management]
---

# Assign Health and Safety profile to a user

Assign the Health and Safety profile to all users in your organization, including employees, visitors, and contractors.

## Before you begin

Role required: sn\_ohs\_im.hs\_profile\_writer

## About this task

For more information on Health and Safety user profiles, see [Health and Safety user profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety-core/health-and-safety-user-profile.md).

**Note:** The **Generate Health And Safety Profiles** scheduled job runs weekly and automatically creates health and safety user profiles for users \[sys\_user\] with an assigned role in any of the Health and Safety applications.

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the configuration icon \(\[Omitted image "icon-config.png"\] Alt text: Configuration icon\).

3.  In the **Lists** tab, select **Health and safety profiles** and then **All**.

4.  Select **New**.

5.  On the form, fill in the fields.

    For information on form field descriptions, see [Health and Safety profile form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety-core/hs-health-safety-profile-form.md).

6.  Select **Save**.


## Result

-   The user is listed in the **Health and safety profile** list under **Configuration** on the Health and Safety Workspace.
-   The user profile is saved in the Health and Safety profile \[sn\_ohs\_im\_health\_and\_safety\_profile\] table.

**Parent Topic:**[Setting up Health and Safety Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety-core/setting-up-hs-core.md)

**Related topics**  


[Install Health and Safety Core]()

[Workplace location data]()

[Enable a Health and Safety table for configuring report field mapping]()

[Create a safety report field mapping for generating reports]()

[Configure groups for Health and Safety]()

[Configure scheduled job to generate frequency rates]()

[Add a Health and Safety visitor]()

[Migrate existing safety documents to the Document library]()

