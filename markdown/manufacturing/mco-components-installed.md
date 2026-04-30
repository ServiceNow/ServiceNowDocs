---
title: Components installed with Manufacturing Commercial Operations Core
description: Several types of components are installed with installation of the Manufacturing Commercial Operations application. These components include user roles, tables, plugins, ServiceNow Store applications, and business rules.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manufacturing Commercial Operations reference, Manufacturing Commercial Operations]
---

# Components installed with Manufacturing Commercial Operations Core

Several types of components are installed with installation of the Manufacturing Commercial Operations application. These components include user roles, tables, plugins, ServiceNow Store applications, and business rules.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Roles installed

User roles are assigned by the use case that is being supported. For each feature, there are both roles with view-only access and roles with various levels of interactive access.

<table id="table_h1g_24n_lfc"><thead><tr><th>

Role

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_mfg\_cmn.manufacturing\_operations\_admin

</td><td>

-   sn\_sls\_prm\_clm\_mgt.bulk\_upload\_admin
-   sn\_sales\_prm\_mgmt.sales\_promotion\_manager
-   sn\_mfg\_cmn.input\_set\_writer
-   sn\_labr\_cmn.labr\_admin
-   sn\_repr\_claim\_mgmt.claim\_admin
-   sn\_sls\_prm\_clm\_mgt.sales\_promotion\_claim
-   sn\_rcl\_claim\_mgmt.adminsn\_prd\_pm.product\_catalog\_admin
-   sn\_sales\_prm\_mgmt.sales\_promotion\_admin
-   sn\_prm.enterprise\_partner\_admin
-   sn\_dealer\_mgmt.dealer\_admin
-   sn\_customerservice\_manager
-   sn\_claim\_cmn.claims\_agent

</td></tr><tr><td>

sn\_claim\_cmn.claims\_agent

</td><td>

-   sn\_sales\_prm\_mgmt.sales\_promotion\_viewer
-   sn\_prm.enterprise\_partner\_agent
-   sn\_rcl\_claim\_mgmt.campaign.viewer
-   sn\_customerservice\_agent
-   sn\_dealer\_mgmt.dealer\_viewer
-   sn\_repr\_claim\_mgmt.navigation\_menu
-   sn\_prd\_pm.product\_catalog\_viewer
-   sn\_repr\_claim\_mgmt.claim\_writer
-   sn\_sls\_prm\_clm\_mgt.sales\_promotion\_claim\_writer
-   sn\_mfg\_cmn.navigation\_menu

</td></tr><tr><td>

sn\_dealer\_mgmt.dealer\_service\_advisor

</td><td>

-   sn\_repr\_claim\_mgmt.claim\_creator
-   sn\_rcl\_claim\_mgmt.campaign.viewer
-   sn\_customerservice.customer\_case\_manager
-   sn\_prd\_pm.external\_product\_viewer
-   sn\_dealer\_mgmt.dealer\_viewer
-   sn\_customerservice.requester
-   sn\_prm.external\_partner\_associate

</td></tr><tr><td>

sn\_dealer\_mgmt.dealer\_sales\_agent

</td><td>

-   sn\_dealer\_mgmt.dealer\_viewer
-   sn\_prm.external\_partner\_associate
-   sn\_sls\_prm\_clm\_mgt.bulk\_upload\_creator
-   sn\_sales\_prm\_mgmt.sales\_promotion\_viewer
-   sn\_sls\_prm\_clm\_mgt.sales\_promotion\_claim\_creator
-   sn\_customerservice.customer\_case\_manager

</td></tr><tr><td>

sn\_rcl\_claim\_mgmt.recall\_manager

</td><td>

-   sn\_rcl\_claim\_mgmt.campaign.creator
-   sn\_mfg\_cmn.navigation\_menu

</td></tr><tr><td>

sn\_sales\_prm\_mgmt.sales\_promotion\_manager

</td><td>

-   sn\_sales\_prm\_mgmt.sales\_promotion\_creator
-   sn\_sls\_prm\_clm\_mgt.sales\_promotion\_claim\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_mfg\_cmn.navigation\_menu

</td></tr><tr><td>

sn\_dealer\_mgmt.dealer\_operations\_admin

</td><td>

-   sn\_prm.external\_partner\_manager
-   sn\_sls\_prm\_clm\_mgt.bulk\_upload\_admin
-   sn\_dealer\_mgmt.dealer\_sales\_agent
-   sn\_dealer\_mgmt.dealer\_service\_advisor

</td></tr><tr><td>

sn\_rcl\_claim\_mgmt.recall\_phase\_owner

</td><td>

-   sn\_mfg\_cmn.navigation\_menu
-   sn\_rcl\_claim\_mgmt.campaign\_phase.writer

</td></tr></tbody>
</table>**Related topics**  


[Exploring Manufacturing Commercial Operations](../concept/manufacturing-explore.md)

