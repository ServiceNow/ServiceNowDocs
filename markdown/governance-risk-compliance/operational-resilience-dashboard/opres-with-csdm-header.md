---
title: Opres with CSDM header Main node configuration
description: The Opres with CSDM header Main node configuration, used by new customers, fetches CMDB objects such as business services, business processes, service offerings, and application services into Operational Resilience. Existing customers typically use the Service \(CMDB\) Main node configuration. Administrators or UI Builder administrators can display or hide the Services overview or Business services overview tab from the Workspace view based on organizational needs.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring 360º views for services and processes, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Opres with CSDM header Main node configuration

The Opres with CSDM header Main node configuration, used by new customers, fetches CMDB objects such as business services, business processes, service offerings, and application services into Operational Resilience. Existing customers typically use the Service \(CMDB\) Main node configuration. Administrators or UI Builder administrators can display or hide the **Services overview** or **Business services overview** tab from the Workspace view based on organizational needs.

For Opres with CSDM header configuration, Operational Resilience administrators set up the records in the following required tables:

-   Business Service \[cmdb\_ci\_service\_business\]
-   Service Offering \[service\_offering\]
-   Business Process \[cmdb\_ci\_business\_process\]
-   Application Service \[cmdb\_ci\_service\_auto\]

After setting up the records in the required tables, Operational Resilience administrators define the hierarchy levels and add relationships for the records. For example, you can set up a hierarchy from business service to service offering, from service offering to business process, and from business process to application service.

## Node relationship configurations

You can configure the node relationships such as the sequence, source table, relationship table, target table, and active flag in the Opres with CSDM header Main node configuration as shown in the example.

![Opres with CSDM header Main node configuration.](../image/node-rel-config-opres-w-csdm-header.png)

The following illustration shows the node relationship configurations for Opres with CSDM header Main node configuration, provided as the base version. For each relationship \[cmdb\_rel\_ci\] table, you can set up combined relationship configurations. For example, for a business service as the parent class, you can configure its relationship to a service offering, then to a business process, and to an application service.

![Relationships.](../image/node-rel-example.png)

The relationship of the CMDB objects is shown in the illustration. The data shown in the illustration exists in the CMDB tables. Main node relationships are configured to inform Operational Resilience about the type of data that should be imported into the application.

![CSDM objects.](../image/csdm-objects-rel.png)

For information on updating the node relationship configurations, see [Configure the Node relationship configurations](../task/update-node-rel-config.md)

.

