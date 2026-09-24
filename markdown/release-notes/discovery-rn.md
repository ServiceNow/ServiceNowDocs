---
title: Discovery release notes
description: The ServiceNow Discovery application automatically identifies and maps IT infrastructure across on-premises and cloud environments. It helps organizations maintain an accurate Configuration Management Database \(CMDB\), improve operational visibility, and reduce manual data collection efforts.The Brazil release expands Discovery's monitoring and scanning capabilities with daily performance snapshots for slow-pattern tables, PowerShell 7 support for MID Server configuration, and expanded credential-less scan options.Discovery Admin Workspace continues to centralize Discovery workflows with new certificate discovery capabilities, Kubernetes resource visibility, and integrated Shazzam insights. These updates help administrators manage discovery activities more efficiently without switching between multiple tools and dashboards.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/discovery-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Discovery, Discovery Admin Workspace, Discovery, Discovery Admin Workspace]
breadcrumb: [ITOM Visibility release notes, IT Operations Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Discovery release notes

The ServiceNow® Discovery application automatically identifies and maps IT infrastructure across on-premises and cloud environments. It helps organizations maintain an accurate Configuration Management Database \(CMDB\), improve operational visibility, and reduce manual data collection efforts.

## About Discovery

-   Gain comprehensive visibility into your IT infrastructure by automatically discovering on-premises, cloud, and hybrid resources, helping you maintain an accurate and up-to-date CMDB.
-   Improve CMDB accuracy and data quality with automated identification and population of configuration item \(CI\) information, reducing manual effort and helping teams make more informed decisions.
-   Accelerate service operations and troubleshooting by providing detailed infrastructure insights that help teams identify dependencies, diagnose issues faster, and reduce service disruptions.
-   Reduce operational overhead through automated discovery processes that continuously identify infrastructure changes, minimizing manual inventory management and administrative tasks.
-   Enhance visibility across cloud environments by discovering and mapping resources across multiple cloud providers, enabling better governance, resource management, and service awareness.

For more information, see [Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/r-discovery.md).

## Activation and other requirements

-   **Activation information**

    Request and activate the Discovery \(com.snc.discovery\) plugin. For more information, see [Request Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/t_ActivateTheDiscoveryPlugin.md).


**Parent Topic:**[ITOM Visibility release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/itom-visibility-rn.md)

## Brazil Early Availability

The Brazil release expands Discovery's monitoring and scanning capabilities with daily performance snapshots for slow-pattern tables, PowerShell 7 support for MID Server configuration, and expanded credential-less scan options.

### What's new

-   **[Configure MID Server parameters for PowerShell 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/config-mid-params-ps7.md)**

    Configure MID Server parameters to run File-based Discovery and Windows ADME on target hosts that use PowerShell 7. Beginning with Brazil, you can set two MID Server configuration parameters to prefer PowerShell 7 over the default PowerShell 5 on the MID Server and on remote target hosts.


### What's changed

-   **[Scan options for credential-less discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/nmap-credential-less-discovery.md)**

    Credential-less Discovery can now check UDP ports and guess the operating system of a target host when it can't confirm an exact match. Enable each option by setting a MID Server property. Both options are inactive by default. Set **mid.discovery.credentialless.include\_udp\_scan** to `true` to check UDP ports and TCP ports. Set **mid.discovery.credentialless.include\_os\_scan\_guess** to `true` to let the scan guess the operating system of the target host.


### What's deprecated or removed

-   **findOrCreateRelationshipType function**

    The `findOrCreateRelationshipType` function is deprecated beginning with Zurich Patch 10, Australia Patch 2 Hotfix 2a, Australia Patch 3, and Brazil. Moving forward, it no longer creates CI relationship types. Instead, it finds an existing CI relationship type and returns an error if the type does not exist. Update any custom scripts that call `findOrCreateRelationshipType` to use `findCIRelationshipType` instead.


## Discovery Admin Workspace version 1.20.0

Discovery Admin Workspace continues to centralize Discovery workflows with new certificate discovery capabilities, Kubernetes resource visibility, and integrated Shazzam insights. These updates help administrators manage discovery activities more efficiently without switching between multiple tools and dashboards.

### What's new

-   **Configure certificate discovery from Discovery Admin Workspace**

    Discovery Admin Workspace now supports certificate discovery configuration and management. Configure certificate discovery from a single location instead of switching between workspace and classic interfaces. The new **Certificate Discovery** tab on the Schedules page centralizes schedule management and access to discovered certificates. Certificate discovery can also use URL Monitoring data to automate discovery targets and reduce manual configuration. Existing certificate discovery configurations remain supported, and certificate discovery continues to respect role-based permissions.

-   **[View Shazzam insights in IP inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/daw-ip-inventory.md)**

    The IP Inventory page now includes a **Shazzam** tab that displays Shazzam Summary and Shazzam Status data alongside your other IP data. Previously, you had to leave the IP Inventory page and open the Shazzam Insights dashboard separately to review probe results. Now you can check which IPs are alive, active, or unreachable while working with your IP addresses, ranges, and networks in the same view

-   **[View Kubernetes resources in Discovery Admin Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/kubernetes-explorer-dash.md)**

    Get a consolidated view of the Kubernetes resources discovered in your environment without leaving the Discovery Admin Workspace. The new Kubernetes explorer dashboard organizes discovered clusters, nodes, namespaces, services, workloads, pods, and Docker images across dedicated tabs. Each tab includes a resource table and visualizations such as data counts, bar charts, and donut charts. Interact with a visualization to filter the table on the same tab. You can also select a resource to open its details page. The details page shows the resource properties and a Dependency View of related configuration items.


### What's changed

-   **[IP Inventory multi-schedule link](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/daw-ip-inventory.md)**

    IP ranges and IP network discovery ranges that belong to a discovery range set used across multiple schedules now display a linked value in the **Discovery Schedule** column. Select the **Multiple** link to open the associated records in the Discovery Schedule Range \[discovery\_schedule\_range\] table, filtered by the relevant discovery range.


