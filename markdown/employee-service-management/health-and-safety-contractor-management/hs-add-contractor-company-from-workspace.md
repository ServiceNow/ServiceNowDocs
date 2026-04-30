---
title: Add a contractor company from Health and Safety Workspace
description: Add a contractor company to prequalify it and its workers. You can then manage the contractor workers from this company for their health and safety.
locale: en-US
release: xanadu
product: Health and Safety Contractor Management
classification: health-and-safety-contractor-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage contractors, Health and Safety Contractor Management, Health and Safety, Employee Service Management]
---

# Add a contractor company from Health and Safety Workspace

Add a contractor company to prequalify it and its workers. You can then manage the contractor workers from this company for their health and safety.

## Before you begin

Role required: sn\_hs\_crm.contractor\_coordinator

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the contractor management icon \(![Contractor management icon](../image/icon-contractor-mgmt.png)\) to open the **Contractor Management** tab.

3.  In the **Lists** tab, select **Contractor companies** and then **All**.

4.  Select **New** to add a contractor company for health and safety.

5.  On the form, fill in the fields.

    1.  Enter company details such as Company name, Services provided, Industry type, address, and its star rating.

    2.  Add a primary contact from the contractor company in the **Primary contact** field.

        The **Primary contact** field displays only users who have been assigned the \[snc\_external\] role and have the Health and Safety profile created for them.

        For more information, see [Assign Health and Safety profile to a contractor worker](hs-assign-hs-user-profile-contract-worker.md).

6.  If necessary, add attachments related to the company using the add attachments icon \(![Add attachment icon.](../../ohs-incident-management/image/icon-add-attachment.png)\).

7.  Select **Save**.


## Result

-   The contractor company is added for health and safety. The record for this company is stored in the Contractor company \[sn\_hs\_crm\_company\] table.
-   Workers, Documents, and Site access tabs appear for this contractor company.

## What to do next

-   In the **Workers** tab, select **Add** to add contract workers from this company who will perform required tasks at your site. Add all the contractor workers including their areas of expertise and contact details.

    **Note:** Only users who have been assigned the \[snc\_external\] role and have the Health and Safety profile created for them appear in the list and can be added as contract workers.

-   In the **Documents** tab, select **Add** to add any documents collected from the contractor company or its workers. For information on storing safety-related documents in Health and Safety Workspace, see [Add a Health and Safety related document](../../ohs-incident-management/task/add-hs-related-document.md).
-   In the **Site access** tab, select **New** to grant site access to workers from this contractor company so that they can perform required tasks at your location.

    If any workers associated with this company already have the site access, they appear in this list. For information on adding site access for a worker, see [Grant site access to a contractor worker](hs-grant-site-access-worker.md).


