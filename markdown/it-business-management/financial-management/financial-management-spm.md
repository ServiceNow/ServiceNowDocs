---
title: Financial Management for licensed SPM users - Legacy
description: If you are a Strategic Portfolio Management \(SPM\) user and have activated Financial Management, then the base system provides you with a Service Offering Costing cost model. Use this cost model to evaluate the amount spent at each level of service. Financial Modeling allocates expenses and generates cost lines based on the level of service for a defined price.
locale: en-US
release: yokohama
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Financial Management for licensed SPM users - Legacy

If you are a Strategic Portfolio Management \(SPM\) user and have activated Financial Management, then the base system provides you with a Service Offering Costing cost model. Use this cost model to evaluate the amount spent at each level of service. Financial Modeling allocates expenses and generates cost lines based on the level of service for a defined price.

## Service Offering Costing cost model

![Service Offering Costing cost model](../image/ServiceOfferingCostingCM.png "Service Offering Costing cost model")

The specifications of the Service Offering Costing cost model are:

-   IT shared service segment accounts are sourced from the IT shared service \[itfm\_shared\_service\] table.
-   Service Offering segment accounts are sourced from the Service Offering \[service\_offering\] table.
-   IT Shared Service segment rolls up to the Service Offering segment. However, there are no default rollup overrides.
-   All sub-buckets are spread equally to all accounts in IT Shared Services provided by the base system setup.
-   There is no data source to this cost model, which means that you should enter the spend information directly into the model and not come from the general ledger. Using the general ledger as a source of spend information is an optional feature that you can configure. See [Prerequisites to modify data source of a cost model](../reference/transition-data-source-cost-model.md) for more information.
-   The expenses are allocated from IT Shared Services segment to the Service Offering segment by Equal method of the base system. By default, the allocation setup provided in the Allocation Setup stage is Equal rollup method. You can configure the rollup method, if needed, to match your specific requirements.

## Seeded IT Shared Services

See the list of [seeded IT Shared Services](financial-management-apm.md#section_bzn_mxw_yhb).

## ITFM prescribed metrics

-   **Allocate to Service Offering on Allocation Maps**

    The metric allocates shared service cost to service offering based on the following weighted metric:

    ![Allocate to service offering on allocation maps](../image/ServiceOfferingAllocationMap.png "Allocate to service offering on allocation maps")

    -   The Service Offering Allocation Map \[itfm\_service\_offering\_allocation\_map\] provides a list of all service offering allocations. This intermediary table references IT shared services from IT shared service \[itfm\_shared\_service\] table and service offering from the Service Offering \[service\_offering\] table.
    -   The prescribed metric performs a sum of shared services and weights the costs accordingly to the receiving service offerings.
-   **Allocate to Service Offerings on related CIs**

    The metric allocates shared service cost to service offerings based on the following weighting table:

    ![Allocate to service offering on allocation maps](../image/ServiceOfferingRelatedCIs.png "Allocate to service offering on allocation maps")

    -   The CI Relationship \[cmdb\_rel\_ci\] table provides a list of all relationships between configuration items.
    -   The prescribed metric performs a count of configuration items and weights the costs accordingly to the receiving service offerings.
-   **Allocate to Service Offerings on Total Subscribers**

    The metric allocates shared service cost to service offerings based on the following weighting table:

    ![Allocate to service offerings on total subscribers](../image/ServiceOfferingTotalSubscription.png "Allocate to service offerings on total subscribers")

    -   The Service Offering \[service\_offering\] table provides a list of all service offerings.
    -   The prescribed metric performs a sum of all subscribers and weights the costs accordingly to the receiving service offering by **Sys ID**.

-   **[Configure service offering costing cost model - Legacy](../task/customize-service-offering-costing-cost-model.md)**  
Configure the service offering costing cost model to allocate expenses and generate bucket cost lines for services offered at each level.
-   **[Allocate expenses using service offering allocation map - Legacy](../task/use-service-offering-allocation-maps.md)**  
You can allocate expenses based on the actual consumption of services offered using the weighted method. In the weighted rollup method the metric weights the amount by the account values. Use the service offering allocation maps table to store your actual consumption data of the cost for service offerings.

**Parent Topic:**[Financial Management - Legacy](c_ITFinance.md)

