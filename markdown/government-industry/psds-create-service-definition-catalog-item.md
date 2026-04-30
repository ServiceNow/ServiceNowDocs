---
title: Configure service definition catalog items for License and Permit Playbook application
description: Create a service definition for use with the License and Permit Playbook in Public Sector Digital Services.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [License and Permit Playbook, Playbooks, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configure service definition catalog items for License and Permit Playbook application

Create a service definition for use with the License and Permit Playbook in Public Sector Digital Services.

## Before you begin

Service definitions are records used to store details about a service that is available to end customers. You can create service definitions for each license/permit service offered by your government agency.

**Important:** After upgrade to Public Sector Digital Services v8.0, you will now be required to create a Service Definition for every previous Service Offered record. The deprecation of Services Offered means that Service Definitions now must be created for every Service that your agency offers. For more information, see [Services Offered and Services Received Migration Guidance](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1559449).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Categories** &gt; **Licenses/Permits**.

2.  Select **Permits** or **Licenses**, depending on which category you wish to add a catalog item to.

3.  Switch to the Public Sector Digital Services Core application, if prompted.

4.  Under the Catalog item related list, select **New**.

5.  On the form, fill in the fields.

<table id="table_b5k_gcj_rsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the public service.

</td></tr><tr><td>

Catalog

</td><td>

Product category that the service falls under. If blank, select Government Service.

</td></tr><tr><td>

Category

</td><td>

Indicates the type of public service. If blank, select either **Permits** or **Licenses**, depending on which category you wish to add a catalog item to.

</td></tr><tr><td>

Application

</td><td>

Application scope of the service. If blank, select .

</td></tr><tr><td>

Status

</td><td>

Status of the public service. Mapped in the active field as:-   Available = true
-   Not available = false


</td></tr><tr><td>

Short description

</td><td>

Short description of the public service.

</td></tr><tr><td>

Description

</td><td>

Description of the public service.

</td></tr></tbody>
</table>6.  Select **Submit**.

    Your catalog item is created and ready for use by constituents submitting cases through the Government Service Portal, or agents creating a case from scratch in the CSM Configurable Workspace.


