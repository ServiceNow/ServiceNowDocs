---
title: Policies for Security Posture Control
description: Policies audit your assets based on data imported from your service graph connectors to help you find potential violations.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Explore, Security Posture Control, Security Operations]
---

# Policies for Security Posture Control

Policies audit your assets based on data imported from your service graph connectors to help you find potential violations.

## Policies

Security Posture Control policies are built on an asset-relationships-properties data model. There are policies that are included with the application, and you can create your own policies to look for specific criteria.

The criteria for policies can be specified either in the form of conditions on that asset’s properties or on a related entity's properties. From the policy builder in the Policy and findings module in the workspace, you can define policies to look for an asset type \(Hardware, Software\) and a Connection \(Reported by, Not reported by\), or an Entity \(Asset source, service graph connector product, or CMDB Metadata\), or you can match other types of specific criteria.

To help you with modifying or creating policies:

-   Set your conditions in the Asset search module and search for assets by specific service graph connector products or for assets that have specific data reported by a connector. You can save your searches as policies.
-   Clone the policies that are included with the application to create more expansive policies. You copy and then refine an existing policy’s conditions without having to re-enter them.
-   Create new policies \(child policies\) using base policies you select as a starting point for new policies.

## Asset types and policies

You use these primary, or top-level asset types as a starting point for defining policies.

-   **Hardware Asset**

    Hardware Asset is an abstraction that represents any device that includes personal computing devices, servers, network devices, cloud virtual machines, and other hardware. Policies audit your assets for potential violations based on the imported data from service graph connector products and ServiceNow® products such as Software Asset Management \(SAM\) and ITOM Discovery.

-   **Software Asset**

    Software Asset permits you to look for any discrepancies that exist between the installed software reported by imported data from service graph connectors, your vulnerability scanner products, and the software reported by scanners that is already accounted for in Software Asset Management \(SAM\) and other ServiceNow products.


|Entity|Relationship|Target entity|Description|
|------|------------|-------------|-----------|
|Hardware Asset|Reported by|Asset Source|Represents a source that reported this asset into CMDB.|
|Hardware Asset|Reported only by|Asset Source|Represents the only source reporting this asset into CMDB.|
|Hardware Asset|Not reported by|Asset Source|Represents a source that did not report this asset into CMDB.|
|Hardware Asset|With IRM Exception|IRM Exception|Represents an exception record in Integrated Risk Management.|
|Hardware Asset|With vulnerability|Vulnerability|Represents a vulnerability found on this asset.|
|Hardware Asset|Has configuration finding|Configuration|Represents a configuration and a compliance issue found on this asset.|
|Hardware Asset|With CMDB metadata|CMDB Metadata|Represents the collection of CMDB CI properties on this asset.|
|Hardware Asset|With connector data|Service Graph Connector|Represents collection of properties reported by selected service graph connector for this asset.|
|Hardware Asset|With aggregated data|Aggregated data|Collection of properties with aggregated values reported by different sources for a given asset. An example is OS.|
|Hardware Asset|From CI Class|CMDB CI Class|Used for defining conditions on specific CI class properties.|
|Hardware Asset|Has cloud metadata|Cloud Metadata|Represents cloud metadata \(applicable for cloud VMs\).|
|Hardware Asset|Has port exposed to internet|OpenPort|Represents a port open to the internet \(applicable for cloud VMs\).|
|Software|Reported by|Asset Source|Represents a source that reported this software.|
|Software|Reported only by|Asset Source|Represents the only source reporting this software.|
|Software|Not reported by|Asset Source|Represents a source that did not report this software.|
|Software|With software details|Software|Represents the collection of software properties such as publisher and version, for example.|

## Example policy audit and data population: CI classes in the CMDB

If a policy tries to retrieve an asset class that is reported or not-reported by a specific Service Graph Connector, Security Posture Control maps all the relevant configuration item \(CI\) classes that are related to that asset class in the CMDB that are populated or not-populated by that Service Graph Connector or connector Category.

For example, say a policy looks for all the hardware assets that are reported by the Service Graph Connector Jamf Pro. The following logic applies.

1.  Security Posture Control identifies which CI classes in the CMDB are mapped to the class 'Hardware Asset' for Jamf Pro.

    **Note:** Different Service Graph Connectors populate different CI classes in the CMDB, and the mapping to CI classes from 'Hardware Asset' varies from one Service Graph Connector to another.

2.  Security Posture Control determines that the CI classes, Computer, Server, and Printer in the CMDB are mapped to the ‘Hardware Asset’ asset class for the Service Graph Connector Jamf Pro.
3.  Security Posture Control then queries for any asset records populated in any of these three CI classes: Server, Computer, and Printer by the Jamf Pro Service Graph Connector in the CMDB and returns those assets.

    The 'CI classes supported by SPC' column in the following table indicates which classes of CI records are considered during a query by the Security Posture Control product as part of a policy evaluation. This table is not a comprehensive list, but you can use it to see how ingested data from various categories and sources is generally mapped and queried.


## Policies included with the application

Activate the asset proﬁles and policies in the Security Posture Control workspace that are [Included with the application](spc-polices-included.md) so that you can identify gaps in configuration or coverage for security tools.

## Creating your own policies

See [Creating your own policies in the Security Posture Control application](../task/spc-creating-policies.md) for more information about how to create your own policies.

For example policies, see [Examples of base, child, and cloned policies for Security Posture Control](spc-policy-examples.md).

See [Create and activate custom policies for Security Posture Control](../task/spc-create-policy.md) for more information about the steps required to create a policy.

## Supported SGCs

For a list of some of the supported service graph connectors, see [Supported hardware service graph connectors for Security Posture Control](../reference/scp-hw-connectors-ci-classes.md) and [Supported software service graph connectors for Security Posture Control](../reference/spc-connector-types-ci-classes.md).

## Mitigation Controls policies

From within in the Security Posture Control \(SPC\) Workspace, gain insight into which threats to your assets are mitigated by available mitigation controls based on how various security tools are configured. See [Mitigation controls policies](spc-mitigation-policies.md) for more information.

