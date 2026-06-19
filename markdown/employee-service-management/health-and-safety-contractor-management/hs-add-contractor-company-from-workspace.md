---
title: Add a contractor company from Health and Safety Workspace
description: Add a contractor company to prequalify it and its workers. You can then manage the contractor workers from this company for their health and safety.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/health-and-safety-contractor-management/hs-add-contractor-company-from-workspace.html
release: australia
product: Health and Safety Contractor Management
classification: health-and-safety-contractor-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage contractors, Health and Safety Contractor Management, Health and Safety, Employee Service Management]
---

# Add a contractor company from Health and Safety Workspace

Add a contractor company to prequalify it and its workers. You can then manage the contractor workers from this company for their health and safety.

## Before you begin

Verify that the primary contact person from the contractor company is added as a system user \(sys\_user\) and the snc\_external role is assigned to them. For more information on this explicit role, see .

Role required: sn\_hs\_crm.contractor\_coordinator and nds\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Health and Safety Workspace**.

2.  Select the contractor management icon \(\[Omitted image "icon-contractor-mgmt.png"\] Alt text: Contractor management icon\) to open the **Contractor Management** tab.

3.  In the **Lists** tab, select **Contractor companies** and then **All**.

4.  Select **New** to add a contractor company for health and safety.

5.  In the **Create new contractor** dialog box, fill in the fields.

<table id="table_acd_3p2_mjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Company name

</td><td>

Name of the company being added.Select an existing company from the list. If the company doesn't already exist in the system, select the **New company** check box and then enter the company name to be added.

</td></tr><tr><td>

New company

</td><td>

Option to enable entering the name of a new company.When selected, the **Company name** field is enabled for typing a new company name.

</td></tr><tr><td>

Industry type

</td><td>

Industry that the contractor company operates in.

</td></tr><tr><td>

Description

</td><td>

Brief description of the company or the nature of the work it performs.

</td></tr><tr><td>

Primary contact

</td><td>

Primary contact person from the contractor company.The **Primary contact** field displays only users who have been assigned the \[snc\_external\] role and have the Health and Safety profile created for them.

For more information, see [Assign Health and Safety profile to a contractor worker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety-contractor-management/hs-assign-hs-user-profile-contract-worker.md).

</td></tr></tbody>
</table>6.  Select **Submit**.


## Result

-   The contractor company is added for health and safety. The record for this company is stored in the Contractor company \[sn\_hs\_crm\_company\] table.
-   Workers, Documents, and Site access tabs appear for this contractor company.

## What to do next

-   In the **Workers** tab, select **Add** to add contract workers from this company who will perform required tasks at your site. Add all the contractor workers including their areas of expertise and contact details.

    **Note:** Only users who have been assigned the \[snc\_external\] role and have the Health and Safety profile created for them appear in the list and can be added as contract workers.

-   In the **Documents** tab, add any documents collected from the contractor company or its workers.

    -   Select **Add** to link an existing document stored in the **Health and Safety document library** list.
    -   Select **New** to upload a new document.
    For information on storing safety-related documents in Health and Safety Workspace, see [Add a new Health and Safety related document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety-core/add-hs-related-document.md).

-   In the **Site access** tab, select **New** to grant site access to workers from this contractor company so that they can perform required tasks at your location.

    If any workers associated with this company already have the site access, they appear in this list. For information on adding site access for a worker, see [Grant site access to a contractor worker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety-contractor-management/hs-grant-site-access-worker.md).

-   If necessary, add attachments related to the company using the add attachments icon \(\[Omitted image "icon-add-attachment.png"\] Alt text: Add attachment icon.\).

