---
title: Service Owner Workspace Migration Dashboard
description: Service Owner Workspace provides a migration dashboard to support your transition from the legacy Service Portfolio Management structure to the enhanced application structure.
locale: en-US
release: xanadu
product: Service Owner Workspace
classification: service-owner-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Setting up Service Owner Workspace, Service Owner Workspace, IT Service Management]
---

# Service Owner Workspace Migration Dashboard

Service Owner Workspace provides a migration dashboard to support your transition from the legacy Service Portfolio Management structure to the enhanced application structure.

**Important:** As of the San Diego release, Service Owner Workspace is in a planned deprecation. New customers can't find or activate Service Owner Workspace. ServiceNow® continues to support existing customers with Service Owner Workspace. For information on the product replacement and the deprecation process, see [Service Owner Workspace](SPM2-premium.md).

By viewing the **Migration Dashboard**, portfolio managers can quickly determine which existing services and offerings contain a deprecated structure or are considered orphaned in the enhanced Service Portfolio Management taxonomy structure.

Users with the following assigned roles can view the Service Portfolio Management dashboard:

-   service\_viewer
-   portfolio\_admin

Users with the portfolio\_admin or service\_editor role can modify services and service offerings to structurally comply with and migrate to the Service Portfolio Management Foundation application.

By default, the dashboard displays reports for all existing service portfolios. An interactive filter enables you to choose a single portfolio to view. The dashboard reports are visible even if there are no service portfolios defined.

Dashboard report categories display the number of related identified migration issues. If there are no migration issues identified for a report category, a 0 is shown.

Access the dashboard by navigating to **Service Portfolio Management** &gt; **Migration Dashboard**. To view detailed information, hover over any report graphic. All report graphs can be refreshed for the latest data.

Migration issues are indicated when a number graphic greater than zero is indicated on the report. For these reports, hover over and click the number graphic. A list opens displaying the services or offerings that require modification to migrate to the Service Portfolio Management Enterprise structure.

The following reports are available on the **Migration Dashboard**. If migration issues are indicated, refer to the report description and how to remedy the issue for migration.

<table id="table_ldv_zbb_zdb"><thead><tr><th>

Migration Dashboard report

</th><th>

Description and migration task

</th></tr></thead><tbody><tr><td>

Deprecated Operational Status Used for Offerings

</td><td>

Indicates the number of existing service offerings using the deprecated singular status of **Operational Status**. Modify these offerings by filling in both the **Phase** and **Status** fields on the **Service Offering** form.

 **Note:** Status can be one of several choices, such as **Design**, **Development**, **Build/Test/Release**, **Operational**, and **Retiring**.

 Click **Update**.

</td></tr><tr><td>

Deprecated Operational Status Used for Service

</td><td>

Indicates the number of existing services using the deprecated singular status of **Operational Status**. Modify these services by filling in both the **Phase** and **Status** fields on the **Service** form.

 **Note:** Status can be one of several choices, such as **Requirements**, **Definition**, **Analysis**, **Approved**, and **Chartered**.

 Click **Update**.

</td></tr><tr><td>

Operational Services not in a Portfolio

</td><td>

Indicates the number of existing services not currently associated with a portfolio. Modify the **Service** form by selecting a portfolio in the **Service portfolio** field. Click **Update**.

</td></tr><tr><td>

Orphaned Services in Catalog Phase

</td><td>

Indicates the number of services in Catalog phase that do not have a parent taxonomy node. Modify the **Service** form by selecting a taxonomy node in the **Taxonomy node** field. Click **Update**.

</td></tr><tr><td>

Deprecated Usage of Service Catalog Entry

</td><td>

Indicates the number of services or offerings linked to a catalog item via the deprecated **Service Catalog Entry**\(sc\_cat\_item\_service\) table.

</td></tr><tr><td>

Orphaned Service Offerings

</td><td>

Indicates the number of service offerings where the **Parent** field on the **Service Offering** form is not pointing to a parent service. Offerings must be children of a service.In the **Parent** field on the **Service Offering** form, search for and select the associated service. Click **Update**.

</td></tr><tr><td>

Cataloged Non-operational Offerings

</td><td>

Indicates the number of active catalog items connected to service offerings not in the catalog phase or with an operational status. Modify the **Service Offering** form **Phase** field to **Catalog** and the **Status** field to **Operational**. Click **Update**.

</td></tr><tr><td>

Services in Catalog Phase without Offering

</td><td>

Indicates the number of services in the **Catalog** phase without at least one associated service offering. An offering must be defined for a service to move into Catalog phase.To associate a service offering to a service, open a specific service offering associated with the cataloged service indicated in the **Migration Dashboard**. In the **Parent** field on the **Service Offering** form, search for and select the associated service. Click **Update**.

</td></tr></tbody>
</table>