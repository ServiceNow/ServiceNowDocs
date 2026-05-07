---
title: Fetching dependencies from the CMDB and BIA
description: You can fetch the dependencies for the services or business services from CMDB in Operational Resilience. Similarly, when the BCM applications are installed, the Operational Resilience scheduled job also monitors for the changes in the business impact analysis \(BIA\) dependencies and fetches the dependency updates.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Fetching dependencies from the CMDB and BIA

You can fetch the dependencies for the services or business services from CMDB in Operational Resilience. Similarly, when the BCM applications are installed, the Operational Resilience scheduled job also monitors for the changes in the business impact analysis \(BIA\) dependencies and fetches the dependency updates.

## Fetching the dependencies from CMDB for the services

Beginning with the Australia release, the Data Relationships Framework supports the Operational Resilience application with the underlying framework to fetch the dependencies from CMDB. The Data Relationships Framework \(app-grc-relationship-config\) is installed with the Operational Resilience application by default. The CMDB dependencies are retrieved by calling an API from the Data Relationships Framework.​

To get the CMDB dependencies, the Operational Resilience administrator must activate the main node configuration, labeled as **Service \(CMDB\)** in the Data Relationships Framework first.​

For each retrieved dependency, the Operational Resilience application searches for an existing entity first. If there is no existing entity, the dependency is skipped. If there is an existing entity and the entity belongs to any entity type in Operational Resilience, it is added to the downstream of its parent’s entity. If the entity does not belong to any entity type, such as Facilities/People/Suppliers/Technology, you must add it manually to the corresponding entity type in Operational Resilience.​

The following example shows a sample CMDB relationship setup for a business service. When the service **Windows mobile** updates its dependencies, the entity of **OWA-SD-01** gets added to the downstream of its entity, **IronMail-SD-01** and **IronMail-SD-02** gets added to the downstream of the **Email** child service entity.

<table id="table_j4p_rzb_f1c"><thead><tr><th>

Business service

</th><th>

Associated dependency, business process, and business service: Email

</th><th>

Process and dependencies associated with business service: Email

</th></tr></thead><tbody><tr><td>

Windows mobile

</td><td>

-   Dependency: **OWA-SD-01**
-   Business process: **Inbound payment validation**
-   Business service: **Email**

</td><td>

-   Process: **Fraud\_escalation**
-   Dependency 1: **IronMail-SD-01** \(The table is cmdb\_ci\_email\_server.\)
-   Dependency 2: **IronMail-SD-02** \(The table is cmdb\_ci\_email\_server.\)

</td></tr></tbody>
</table>## Fetching the dependencies from the business impact analysis \(BIA\)

When the BCM applications are installed, Operational Resilience fetches the BIA's dependency update if the BIA's **Applies to** field is a business process used in Operational Resilience.

The following conditions must be met for pulling the BIA dependencies in Operational Resilience:

-   The BIA has to be in the **Approved** state.
-   The BIA should not be in the **Expired** state.
-   The dependency group has to be completed.

**Note:** Only when the **Applies to** field of the BIA record matches with any business process within the **Business Processes** Entity Type, its dependencies are fetched by the scheduled job.

For each fetched dependency, the Operational Resilience application looks for an existing valid entity first. If the dependency has an existing valid entity and the entity belongs to any entity type in Operational Resilience, it is added to the downstream of its parent's entity.

To fetch the CMDB dependency updates or BIA dependency updates, the following conditions are followed:

-   If there is no entity for the dependency, it is skipped. Operational Resilience does not create an entity for the dependency.
-   If a dependency entity is inactive, it is ignored.
-   If a dependency entity is active, but it has no pillar, it is ignored.
-   If a dependency entity is active and has a pillar, but it does not belong to any Operational Resilience entity type, it is ignored.

## Adding the dependencies manually

If the entity does not belong to an entity type such as Facilities, People, Suppliers, Technology, Operational Resilience users must add it to the corresponding entity type manually.​ Instead of using the scheduled job, Operational Resilience administrators and managers can update the dependencies manually.

## Support for main node configuration in Data Relationships Framework

For information on the Data Relationships Framework and main node configuration, see [Data Relationships Framework](../../grc-common/concept/data-relationship-framework.md) and [Create a main node configuration record](../../grc-common/task/create-a-main-node-config-record.md).

