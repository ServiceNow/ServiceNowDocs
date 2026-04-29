---
title: Assign Health and Safety profile to a contractor worker
description: Assign the Health and Safety profile to all contractor workers who need to complete assigned tasks to work at your site.
locale: en-US
release: australia
product: Health and Safety Contractor Management
classification: health-and-safety-contractor-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Health and Safety Contractor Management, Health and Safety, Employee Service Management]
---

# Assign Health and Safety profile to a contractor worker

Assign the Health and Safety profile to all contractor workers who need to complete assigned tasks to work at your site.

## Before you begin

Confirm that the snc\_external role is assigned to the contractor worker. For more information on this explicit role, see [Explicit Roles](https://www.servicenow.com/docs/access?context=explicit-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US).

Role required: sn\_hs\_crm.contractor\_coordinator

## About this task

**Note:** The **Generate Health And Safety Profiles** scheduled job runs weekly and automatically creates health and safety user profiles for users \[sys\_user\] with an assigned role in any of the Health and Safety applications.

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the configuration icon \(![Configuration icon](../../hs-risk-management/image/icon-config.png)\).

3.  In the **Lists** tab, select **Health and safety profiles** and then **All**.

4.  Select **New** to add a contractor worker for health and safety.

5.  On the form, fill in the fields.

    For information on form field descriptions, see [Health and Safety profile form](../../ohs-incident-management/reference/hs-health-safety-profile-form.md).

6.  Select **Save**.


## Result

-   The contractor worker is listed in the **Health and safety profile** list under **Configuration** on the Health and Safety Workspace. The user profile is saved in the Health and Safety profile \[sn\_ohs\_im\_health\_and\_safety\_profile\] table.
-   The user is available for selection on these forms:
    -   Contractor company when registering a contractor company for health and safety. For more information, see [Add a contractor company from Health and Safety Workspace](hs-add-contractor-company-from-workspace.md).
    -   Worker form when adding a contract worker to a contractor company.
    -   Site access form when granting site access to a contract worker. For more information, see [Grant site access to a contractor worker](hs-grant-site-access-worker.md).

