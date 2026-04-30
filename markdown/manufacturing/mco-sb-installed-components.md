---
title: Components installed with Manufacturing Commercial Operations with Service Exchange
description: Several types of components are installed when you activate the Service Exchange application in Manufacturing Commercial Operations, including tables and user roles.Several types of components are installed when you activate the Service Exchange for Providers application in Manufacturing Commercial Operations, including tables and user roles.Several types of components are installed with activation of the Service Exchange for Consumers application in Manufacturing Commercial Operations, including tables and user roles.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Service Bridge reference, Manufacturing Commercial Operations reference, Manufacturing]
---

# Components installed with Manufacturing Commercial Operations with Service Exchange

Several types of components are installed when you activate the Service Exchange application in Manufacturing Commercial Operations, including tables and user roles.

## Plugins Installed with Service Bridge for Manufacturing Foundation

|Plug-In IDs|Store App Names|
|-----------|---------------|
|Sn\_sb|Service Bridge Base|
|Sn\_sb\_pro|Service Bridge for Providers|
|Sn\_sb\_con|Service Bridge for Consumers|
|Sn\_sb\_rps|Service Bridge Remote Process Sync Transport|
|Sn\_sb\_om\_provider|Service Bridge Order Management for Providers|

## Components installed with Service Exchange for Providers in Manufacturing Commercial Operations

Several types of components are installed when you activate the Service Exchange for Providers application in Manufacturing Commercial Operations, including tables and user roles.

### Roles installed

The following roles are installed with the Service Exchange for Providers application.

<table id="table_gtr_pw3_bmb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Service Bridge requester \[sn\_sb.requestor\]

</td><td>

-   Enables members of the customer IT staff to request and monitor services from the provider from their service catalog.

**Note:** Any member of the customer's staff who needs access to the provider's remote record producers requires this role.

-   Provides access to the remote record producers and provider tasks.

</td><td>

N/A

</td></tr><tr><td>

Service Bridge read \[sn\_sb.read\]

</td><td>

-   Enables the provider's customer service agents to read the contents of the provider task record.
-   Provides read-only access to the Service Exchange application.

</td><td>

N/A

</td></tr><tr><td>

Service Bridge admin \[sn\_sb.admin\]

</td><td>

-   Typically assigned to an administrator for the Service Exchange applications on both the customer and the provider side.
-   Provides read access to all Service Exchange tables

</td><td>

-   sn\_sb.requestor
-   sn\_sb.remote\_task\_creator
-   sn\_sb.read
-   flow\_designer
-   sn\_customerservice.case\_viewer
-   sn\_customerservice.customer\_data\_viewer
-   catalog

</td></tr></tbody>
</table>### Tables Installed

The following tables are installed with the Service Exchange for Providers application.

<table id="table_ur3_nv2_ccc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Authorized Users \[sn\_sb\_pro\_authorized\_user\]

</td><td>

Contains the authorized user records.

</td></tr><tr><td>

Consumer Connection \[sn\_sb\_pro\_consumer\_connection\]

</td><td>

Consumer connection record for provider, extends the base connection table.

</td></tr><tr><td>

Entitlement \[sn\_sb\_pro\_entitlement\]

</td><td>

Provider entitlements associating records to entitled consumers, extends base entitlement table.

</td></tr><tr><td>

Inbound Field \[sn\_sb\_pro\_inbound\_field\]

</td><td>

Manages provider side inbound field mappings for remote task definitions.

</td></tr><tr><td>

Outbound Field \[sn\_sb\_pro\_outbound\_field\]

</td><td>

Manages provider side outbound field mappings for remote task definitions.

</td></tr><tr><td>

Personas \[sn\_sb\_pro\_persona\]

</td><td>

Manages personas for Service Exchange.

</td></tr><tr><td>

Provider \[sn\_sb\_pro\_provider\]

</td><td>

Provider association record to tie provider side records together.

</td></tr><tr><td>

Provider Task \[sn\_sb\_pro\_provider\_task\]

</td><td>

Provider tasks on provider side, created by consumers through remote record producers.

</td></tr><tr><td>

Registration \[sn\_sb\_pro\_registration\]

</td><td>

Service Exchange registration records.

</td></tr><tr><td>

Remote Choice Definition \[sn\_sb\_pro\_remote\_choice\_definition\]

</td><td>

Remote choice definitions for remote record producer.

</td></tr><tr><td>

Consumer Criteria

 \[sn\_sb\_pro\_remote\_record\_producer\_

 consumer\_criteria\]

</td><td>

Consumer criteria records attributed to remote record producers, controls which consumers are entitled to a given remote record producer.

</td></tr><tr><td>

Remote service \[sn\_sb\_pro\_remote\_service\]

</td><td>

Remote service record.

</td></tr><tr><td>

Remote Task \[sn\_sb\_pro\_remote\_task\]

</td><td>

Remote tasks for managing data transfer between parent tasks on synced instances.

</td></tr><tr><td>

Remote Task Definition \[sn\_sb\_pro\_remote\_task\_def\]

</td><td>

Remote task definition, controls creation and processing of remote tasks.

</td></tr><tr><td>

Consumer Criteria

 \[sn\_sb\_pro\_remote\_task\_def\_

 consumer\_criteria\]

</td><td>

Consumer criteria records attributed to remote task definitions, controls which consumers are entitled to a given remote task definition.

</td></tr><tr><td>

Remote Task Variable \[sn\_sb\_pro\_remote\_task\_variable\]

</td><td>

Glide variables associated with a remote task, allows displaying incoming synced data

</td></tr><tr><td>

Service Bridge Settings \[sn\_sb\_pro\_service\_bridge\_settings\]

</td><td>

Settings record for provider, manages various Service Exchange settings alignment between provider and consumer.

</td></tr><tr><td>

Transform \[sn\_sb\_pro\_transform\]

</td><td>

Provider side transform records.

</td></tr></tbody>
</table>## Components installed with Service Exchange for Consumers

Several types of components are installed with activation of the Service Exchange for Consumers application in Manufacturing Commercial Operations, including tables and user roles.

**Note:** The Application Files \[sys\_metadata\] table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

### Roles installed

The following roles are installed with the Service Exchange for Consumers application.

<table id="table_gtr_pw3_bmb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Service Bridge admin \[sn\_sb.admin\]

</td><td>

-   Typically assigned to an administrator for the Service Exchange applications on both the customer and the provider side.
-   Provides read access to all Service Exchange tables

</td><td>

-   sn\_sb.read
-   sn\_sb.requestor
-   sn\_sb.remote\_task\_creator
-   flow\_designer
-   catalog

</td></tr><tr><td>

Service Bridge read \[sn\_sb.read\]

</td><td>

Provides read-only access to provider tasks

</td><td>

N/A

</td></tr><tr><td>

Service Bridge requester \[sn\_sb.requestor\]

</td><td>

Provides access to remote record producers and provider tasks

</td><td>

N/A

</td></tr></tbody>
</table>### Tables installed

The following tables are installed with the Service Exchange for Consumers application.

<table id="table_ttz_z2q_gzb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Authorized user \[sn\_sb\_con\_authorized\_user\]

</td><td>

Authorized users.

</td></tr><tr><td>

Connection \[sn\_sb\_con\_consumer\]

</td><td>

Consumer side connection record.

</td></tr><tr><td>

Entitlement \[sn\_sb\_con\_entitlement\]

</td><td>

Consumer side table extending entitlements.

</td></tr><tr><td>

Inbound Field \[sn\_sb\_con\_inbound\_field\]

</td><td>

Consumer side inbound fields for Remote Task Definitions.

</td></tr><tr><td>

Outbound Field \[sn\_sb\_con\_outbound\_field\]

</td><td>

Consumer side outbound fields for Remote Task Definitions.

</td></tr><tr><td>

Personas \[sn\_sb\_con\_persona\]

</td><td>

Consumer side persona records.

</td></tr><tr><td>

Provider Connection \[sn\_sb\_con\_provider\_connection\]

</td><td>

Provider Connection record linking consumer to provider instance, extending base connection table.

</td></tr><tr><td>

Provider Task \[sn\_sb\_con\_provider\_task\]

</td><td>

Consumer side provider task records, extends Provider Task base table.

</td></tr><tr><td>

Remote Choice Cache \[sn\_sb\_con\_remote\_choice\_cache\]

</td><td>

Consumer side cache for remote choice queries.

</td></tr><tr><td>

Remote Record Producer \[sn\_sb\_con\_remote\_record\_producer\]

</td><td>

Consumer side Remote Record Producer records.

</td></tr><tr><td>

Remote Task \[sn\_sb\_con\_remote\_task\]

</td><td>

Consumer side remote task records, extends remote task base table.

</td></tr><tr><td>

Remote Task Definition \[sn\_sb\_con\_remote\_task\_def\]

</td><td>

Consumer side Remote Task Definition records.

</td></tr><tr><td>

Remote Task Variable\[sn\_sb\_con\_remote\_task\_variable\]

</td><td>

Remote Task associated variable table extending glide vars.

</td></tr><tr><td>

Service Bridge Settings \[sn\_sb\_con\_service\_bridge\_settings\]

</td><td>

Consumer side Service Exchange setting records, extends settings base table.

</td></tr><tr><td>

Remote Choice \[sn\_sb\_con\_st\_remote\_choice\]

</td><td>

Consumer side remote choice records.

</td></tr><tr><td>

Transform \[sn\_sb\_con\_transform\]

</td><td>

Consumer side transform records, extends transform base table.

</td></tr></tbody>
</table>