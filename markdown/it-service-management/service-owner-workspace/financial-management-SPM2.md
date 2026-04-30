---
title: Financial Management for Service Owner Workspace
description: Integrate Service Owner Workspace with Financial Management to access preconfigured service offering cost models. You can use these cost models to evaluate expenses and generate cost lines based on the level of service offering for a defined cost.
locale: en-US
release: xanadu
product: Service Owner Workspace
classification: service-owner-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Service Owner Workspace, Service Owner Workspace, IT Service Management]
---

# Financial Management for Service Owner Workspace

Integrate Service Owner Workspace with Financial Management to access preconfigured service offering cost models. You can use these cost models to evaluate expenses and generate cost lines based on the level of service offering for a defined cost.

**Important:** As of the San Diego release, Service Owner Workspace is in a planned deprecation. New customers can't find or activate Service Owner Workspace. ServiceNow® continues to support existing customers with Service Owner Workspace. For information on the product replacement and the deprecation process, see [Service Owner Workspace](SPM2-premium.md).

<table id="table_e2x_rbr_nkb"><tbody><tr><td>

![Use Service Owner Workspace](../image/SOWUseBanner2.png "Navigate")

</td></tr></tbody>
</table>## Activation and features

Activate the Financial Management for SPM plugin \(com.snc.financial\_management\_for\_spm\) to access the preconfigured, base system models. Financial Management for SPM contains demo data and activates related plugins if they are not already active.

The Service Portfolio Management Estimated Spend plugin \(com.snc.spm.spend\) is available to enhance your Service Owner Workspace experience. With this feature, you can choose to use the default local service offering cost model or access the cost models offered via the Financial Management application.

When Service Owner Workspace \(com.spm\_owner\_workspace\) and Financial Management for SPM \(com.snc.financial\_management\_for\_spm\) are activated and the **sn\_spm\_spend.offering\_cost\_source** system property is set to the value **Financial Management** the **Estimated Spend** form section displays the fields **Estimated annual spend**, **FM aggregated period**, and **FM aggregated cost**. These fields reveal read-only data stored on the service offering, service, and taxonomy records.

## View calculated spend per offering in Service Owner Workspace

When you choose to use the cost models offered via the Financial Management application, calculated spend per service offering is displayed as a single score widget in Service Owner Workspace. View **Estimated Spend** as part of the **Overview** dashboard displaying associated service offering health and performance metrics.

![Estimated spend](../image/EstimatedSpend.png "Estimated spend")

Service offering spend estimates are combined and summed up per period to the service and portfolio levels within your portfolio taxonomy. Estimated spend at the service and portfolio level enables you to better understand costs and how this aligns with performance throughout your service portfolio. With the estimated spend feature, you can:

-   Balance your required service performance with the appropriate spend.
-   Compare similar services by weighing spend to performance.
-   Verify whether service spend is meeting your desired goals.
-   View cost drivers within your service portfolio and the taxonomy structure.
-   Compare an internal service spend to external service provider options.

## Local model compared to Financial Management model for estimated spend

Estimated spend calculations run daily as a separate job.

When the system property **sn\_spm\_spend.offering\_cost\_source** = **Local Model**, the estimated annual spend for a service offering, service, and taxonomy is determined by adding the estimated annual spends for all child entities. Estimated annual spend data is stored on the service offering, service, and taxonomy records.

When the system property **sn\_spm\_spend.offering\_cost\_source** = **Financial Managment**, the estimated spend for a service offering, service, and taxonomy is determined by adding the Financial Management estimated spends for all child entities.

For each node, determine the Financial Management estimated spend for the currently selected Financial Management period by adding all the child entity estimated spends. This happens recursively up the entire taxonomy structure, starting with the service offering, to the service, to the taxonomy.

For detailed information about integrating with Financial Management and configuring costing for a service offering, refer to [Financial Management for licensed SPM users](https://www.servicenow.com/docs/access?context=financial-management-spm&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

