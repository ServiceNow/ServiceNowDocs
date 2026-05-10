---
title: Installed with Service Portfolio Management
description: Service Portfolio Management Core is active by default for users with ITSM licenses. Service Portfolio Management Foundation is administrator activated and enables you to document portfolios, taxonomies, services, and service offerings using a standardized, structured format.
locale: en-US
release: australia
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Service Portfolio Management, IT Service Management]
---

# Installed with Service Portfolio Management

Service Portfolio Management Core is active by default for users with ITSM licenses. Service Portfolio Management Foundation is administrator activated and enables you to document portfolios, taxonomies, services, and service offerings using a standardized, structured format.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

## Service Portfolio Management plugins

The following two plugins enable you to use the full functionality of Service Portfolio Management:

-   Service Portfolio Management Core \[com.snc.service\_portfolio\_core\]
-   Service Portfolio Management Foundation \[com.snc.service\_portfolio\]

The Service Portfolio Management Foundation plugin automatically activates the Service Portfolio Management Core plugin. Each plugin independently installs a set of roles and tables.

If you install Service Builder from the ServiceNow Store, its plugin \[com.snc.service\_builder\] automatically installs. Service Builder uses the same role set as Service Portfolio Management. See [Service Builder](../../service-builder/concept/service-builder.md) for more information.

## Service Portfolio Management Core roles and tables

<table id="table_vfq_lgw_5hb"><thead><tr><th>

Role

</th><th>

Role actions

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

\[portfolio\_admin\]

</td><td>

-   Set up, create, edit, and delete services and service portfolios.
-   Manage portfolios including related commitments and availability.
-   Update taxonomy nodes, services, service offerings, and reparent services.

</td><td>

-   portfolio\_editor
-   service\_admin
-   sla\_manager

</td></tr><tr><td>

\[service\_editor\]

</td><td>

Edit services and service offerings that they own or are a delegate of.

</td><td>

service\_viewer

</td></tr><tr><td>

\[service\_viewer\]

</td><td>

View all services and service offerings.

</td><td>

cmdb\_read

</td></tr></tbody>
</table><table id="table_rd3_4gw_5hb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[service\_offering\]

</td><td>

Extends the \[cmdb\_ci\_service\] table.

</td></tr></tbody>
</table>## Service Portfolio Management Foundation roles and tables

<table id="table_sfy_qhw_5hb"><thead><tr><th>

Role

</th><th>

Role actions

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

\[portfolio\_editor\]

</td><td>

-   Edit and delete services and service portfolios.
-   Update portfolios, taxonomy nodes, services, service offerings, and reparent services.

</td><td>

-   service\_editor
-   portfolio\_viewer
-   sla\_manager

</td></tr><tr><td>

\[portfolio\_viewer\]

</td><td>

View portfolios, taxonomy nodes, services, and service offerings.

</td><td>

service\_viewer

</td></tr><tr><td>

\[service\_admin\]

</td><td>

Set up, create, edit, and delete services and service offerings.

</td><td>

service\_author

</td></tr><tr><td>

\[service\_author\]

</td><td>

Create, edit, and delete services and service offerings of which they’re an owner or have created.

</td><td>

service\_editor

</td></tr></tbody>
</table><table id="table_exd_shw_5hb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[spm\_service\_portfolio\]

</td><td>

Used to create or modify a service portfolio.

</td></tr><tr><td>

\[spm\_taxonomy\_layer\_definition\]

</td><td>

Used to define the order of a taxonomy layer associated with a service portfolio.

**Note:** Use this table with the legacy portfolio structure. The standard portfolio structure doesn’t have taxonomy layers. For more information, see [Service Portfolio Management portfolios](../concept/SPM2-service-portfolios.md).

</td></tr><tr><td>

\[spm\_taxonomy\_node\]

</td><td>

Used to create or modify a taxonomy node associated with a service portfolio.

</td></tr><tr><td>

\[service\_subscribe\_company\]

</td><td>

Used to associate service offering subscriptions to a specific company.

</td></tr><tr><td>

\[service\_scope\]

</td><td>

Used to store user-defined limits to the service levels of a service.

</td></tr><tr><td>

\[service\_subscribe\_department\]

</td><td>

Used to associate service offering subscriptions to a specific department.

</td></tr><tr><td>

\[service\_availability\]

</td><td>

Used to store the calculated availability records of a service.

</td></tr><tr><td>

\[service\_subscribe\_sys\_user\]

</td><td>

Used to create a module enabling you to categorize subscribers by individual users.

</td></tr><tr><td>

sc\_cat\_item\_subscribe\_mtom

</td><td>

Used to create a catalog item and make it available for subscription.

</td></tr><tr><td>

sc\_cat\_item\_subscribe\_no\_mtom

</td><td>

Used to create an item while not making it available for subscription.

</td></tr><tr><td>

service\_subscribe\_location

</td><td>

Used to specify where a service offering is located, by actual physical address.

</td></tr><tr><td>

sc\_cat\_item\_service

</td><td>

Used to enter an item in the Service Catalog.

</td></tr><tr><td>

service\_offering\_commitment

</td><td>

Used to create and configure service commitments by specifying orders and associating service offerings.

</td></tr><tr><td>

service\_in\_scope

</td><td>

Used to create and define services In Scope and specify the scope parameters.

</td></tr><tr><td>

service\_subscribe\_sys\_user\_grp

</td><td>

Used to create a module enabling you to categorize subscribers by group.

</td></tr><tr><td>

service\_commitment

</td><td>

Used to store records from the **Service Commitments** related list in the Service Offerings form.

</td></tr><tr><td>

service\_out\_scope

</td><td>

Used to create and define services Out of Scope and specify the scope parameters.

</td></tr></tbody>
</table>**Parent Topic:**[Service Portfolio Management reference](SPM2-reference.md)

