---
title: Incident Management use case
description: Incident Management restores normal service operation, while also minimizing impact to your business and maintaining the quality of your data.
locale: en-US
release: zurich
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Applying CSDM guidelines to Incident Management, Configure, Incident Management, IT Service Management]
---

# Incident Management use case

Incident Management restores normal service operation, while also minimizing impact to your business and maintaining the quality of your data.

## Incident Management Use Case

Use Incident Management to create an incident that captures information about the asset-related CIs. An incident keeps a record of the updated, repaired, swapped, or retired CIs.

By keeping track of the assets, you can tell where the assets are located, how they are used, and when changes were made to them. This information helps you systematically monitor and manage the assets in your company.

A CI generates an incident. Use a dependency view to identify other CIs that are affected by the incident. Associate the affected CIs with an incident record to find out how the incident affects other dependent CIs.

Following the CSDM framework provides value to Incident Management in the following ways:

-   Incident Management understands the impact of the Incident on services and service offerings.
-   Incident Management dynamically routes incidents.
-   Incident Management identifies all affected services.

## Results of the use case

The CSDM framework provides context for incidents—both the CIs involved in the incident and the services that it affects.

Use the Incident form to see the impact of an incident and restore affected services. Complete the following steps:

1.  Populate the **Impacted Services** related list with the services and service offerings that are related to the populated CI.
2.  \(Optional\) Use the **Service** and **Service Offering** attributes to help narrow the list of available CIs.

    **Note:** Narrowing the list of available CIs is not a feature of the base system. To narrow the list, you need to configure the Incident form.

3.  Populate the **Configuration Item** attribute \[configuration\_item\] with the CI or the affected service. You can then use the CI to identify details for incident routing. For example, you can use the CI data like Support Group and provide information about the service impact by using dependency relationships.
4.  \(Optional\) Add the **Affected CI** related list \[task\_ci\] to identify the CIs that might have caused the incident.
5.  \(Optional\) Add the **Impacted Services** related list \[task\_cmdb\_ci\_service\] to see the services and CIs that are impacted by the incident.

**Parent Topic:**[Applying CSDM guidelines to Incident Management](itsm-incident-use-case-product-view.md)

