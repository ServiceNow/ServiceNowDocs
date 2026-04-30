---
title: Exploring FSC common applications
description: Explore the FSC common application plugins and their dependencies.
locale: en-US
release: yokohama
product: Common Service Delivery
classification: common-service-delivery
topic_type: concept
last_updated: "2025-02-05"
reading_time_minutes: 2
breadcrumb: [Finance and Supply Chain common applications, Finance and Supply Chain applications, Finance and Supply Chain]
---

# Exploring FSC common applications

Explore the FSC common application plugins and their dependencies.

<table id="table_ilp_t2t_g2c"><thead><tr><th>

Plugin name

</th><th>

Description

</th><th>

Dependencies

</th><th>

Mandatory/Optional

</th></tr></thead><tbody><tr><td>

Finance Common Architecture \[sn\_fin\]

</td><td>

Maintains primary data such as Enterprise Resource Planning \(ERP\) sources, legal entities, accounting periods, and so on.

 For more information about the components installed with this plugin, see [Components installed with Finance Common Architecture](../../sourcing-procurement-operations/reference/installed-with-finance-common.md).

</td><td>

-   Finance Applications – Common Dependencies \[com.snc.fin\_dep\]
-   Fiscal Calendar \[com.snc.fiscal\_calendar\]
-   Scoped Application Restricted Caller Access \[com.glide.scope.access.restricted\_caller\]
-   Insert Multiple Web Service \[com.glide.web\_service\_insert\_multiple\]

</td><td>

Mandatory for SPO, SLO, and APO

</td></tr><tr><td>

ERP Integration Framework \[sn\_fcms\_integrations\]

</td><td>

Provides integration support between the Platform and common ERP systems.For more information about the components installed with this plugin, see [Components installed with ERP Integration Framework](../../sourcing-procurement-operations/reference/installed-with-FSC-ERP.md).

</td><td>

-   Scoped Application Restricted Caller Access \[com.glide.scope.access.restricted\_caller\]
-   Insert Multiple Web Service \[com.glide.web\_service\_insert\_multiple\]

</td><td>

Mandatory only if you want to use a common integration framework to get the data from third-party ERP systems into Source-to-Pay applications: SPO, SLO, and APO

</td></tr><tr><td>

Common Service Delivery \[sn\_spend\_sdc\]

</td><td>

Contains Finance Case, Finance Case Line, Finance Task, and Playbook status tables, as well as other infrastructure that forms the basis of Finance and Supply Chain workflows products.

</td><td>

-   Process Automation Designer Core \[com.glide.pad.core\]
-   Process Automation Designer for App Engine \[com.glide.pad.license\]
-   Playbook Experience \[com.playbook\_experience\]

</td><td>

Mandatory for SPO, SLO, and APO

</td></tr><tr><td>

Source-to-Pay Common Architecture \[snc.sn\_shop\]

</td><td>

Provides an architecture to store purchase orders, requisitions, sourcing requests, and other objects that are commonly used across the source-to-pay business processes.For more information about the components installed with this plugin, see [Components installed with Source-to-Pay Common Architecture](../../sourcing-procurement-operations/reference/components-installed-with-source-to-pay-common-architecture.md).

</td><td>

-   Finance Common Architecture \[com.sn\_fin\]
-   Common Service Delivery \[com.sn\_spend\_sdc\]

</td><td>

Mandatory for SPO, SLO, and APO

</td></tr><tr><td>

Source-to-Pay Integration Framework \[sn\_spend\_intg\]

</td><td>

Provides a set of staging tables, transform maps, and workflows to integrate Source-to-Pay Operations with third-party ERP system. For more information, see [Source-to-Pay integration framework](source-to-pay-integration-framework.md).

</td><td>

Source-to-Pay Common Architecture \[com.snc.sn\_shop\]

</td><td>

Mandatory only if you want to use a framework to develop a set of API integrations with Source-to-Pay applications: SPO, SLO, and APO

</td></tr><tr><td>

Supplier Common Architecture \[snc.sn\_slm\]

</td><td>

Provides a common architecture to track data objects related to a supplier used in both Supplier Lifecycle Operations andSupplier Collaboration Portal.For more information about the components installed with this plugin, see [Components installed with Supplier Lifecycle Operations](../../supplier-lifecycle-operations/reference/installed-with-supp-mgmt.md).

</td><td>

-   Finance Common Architecture \[sn\_fin\]
-   External User Registration \[snc.external\_user\_self\_registration\]
-   Common Service Delivery \[sn\_spend\_sdc\]
-   Common Vendor Core \[snc.sn\_vendor\_core\] and \[com.snc.vendor\_core\]
-   Document Management \[snc.platform\_document\_management\]

</td><td>

Mandatory for SLO

</td></tr></tbody>
</table>