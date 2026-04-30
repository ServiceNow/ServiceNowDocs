---
title: Discovery patterns used by ITOM Visibility
description: Service Mapping and Discovery use patterns in their discovery process that cover most industry standard network devices and applications. You can customize these patterns and create new ones.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2025-10-09"
reading_time_minutes: 10
keywords: [Discovery role, Pattern role]
breadcrumb: [ITOM Visibility, IT Operations Management]
---

# Discovery patterns used by ITOM Visibility

Service Mapping and Discovery use patterns in their discovery process that cover most industry standard network devices and applications. You can customize these patterns and create new ones.

ServiceNow applications refer to devices and applications that comprise a service instance as configuration items \(CIs\).

## What discovery patterns are

A pattern is a sequence of commands whose purpose it is to detect attributes of a CI and its outbound connections. Service Mapping and Discovery share a set of preconfigured patterns that cover most of the commonly used devices and applications. Patterns can be of the infrastructure or application type. Infrastructure patterns are used only by Discovery for creating lists of devices. Application patterns serve both Service Mapping and Discovery, which use the same application patterns for their purposes. For example, Discovery runs the horizontal discovery with the Apache Web Server pattern to find and list all Apache Web Servers in your organization. Service Mapping runs the top-down discovery using the same pattern to discover a specific Apache Web Server and place it on a service instance map.

**Note:** Currently, pattern operations do not support multi-languages. If values returned from pattern operations are not in English, the returned data cannot be parsed properly and the pattern discovery will fail.

|Product|Pattern type|Result|
|-------|------------|------|
|Discovery|Infrastructure pattern|Inventory list of devices|
|Application pattern|Inventory list of applications|
|Service Mapping|Application pattern|Service instance map|

For discovering devices that act as hosts for applications, Service Mapping relies on Discovery. As part of the top-down discovery process, Service Mapping triggers Discovery to perform its horizontal discovery behind the scenes. Service Mapping then uses information on hosts provided by the horizontal discovery to create its service instance maps.

Patterns of all types are stored in the Discovery Patterns \[sa\_pattern\] table.

Discovery uses a combination of probes and patterns. For more information, see [Horizontal discovery process flow with probes and sensors](../../discovery/concept/c_DiscoProcessFlows.md).

## Correlation between pattern and CI type

Patterns are assigned to the CI types that they serve to discover. If necessary, you can assign more than one CI type per pattern. In that case, you define one main CI type and multiple related CI types. For example, a pattern for discovering BIG-IP Global Traffic Manager \(GTM\) F5 has F5 BigIP GTM as its main CI type. It also has related CI types for the Domain Name System \(DNS\) name, network adapter, and other components.

For the top-down discovery performed by Service Mapping, each application pattern serves to discover only the main CI type.

![During top-down discovery, a pattern discovers only the main CI type.](../image/PatternTopDownDiscovery.png "Main CI type discovery during top-down discovery")

However, Service Mapping usually uses more than one pattern to discover the same CI type, because a CI type can use different protocols, operating systems, entry points, and so on.

Unlike top-down discovery, the process of horizontal discovery uses each pattern to discover a main CI type with all related CI types.

![During horizontal discovery, a pattern discovers the main CI type and all related CI types.](../image/PatternHorizontalDiscovery.png "Discovery of main and related CI types during horizontal discovery")

## Why install patterns from the ServiceNow Store

ServiceNow releases new discovery patterns on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) on a monthly basis to ensure that your organization can discover the latest industry-standard devices and applications. Major ServiceNow versions incorporate patterns previously released on the ServiceNow Store.

ServiceNow releases all discovery patterns using the following applications:

-   **Discovery and Service Mapping Patterns \(sn\_itom\_pattern\)**

    This application provides the latest versions of discovery patterns the original version of which ServiceNow released on ServiceNow Store.

-   **Visibility Content \(sn\_pattern\_design\)**

    This application supplies the updated version of the patterns that were part of the family releases up until Tokyo.


You can install the latest available versions of the pattern applications from the ServiceNow Store. Alternatively, you can install these applications as plugins on your ServiceNow instance.

## Why customize patterns

You can customize patterns in the following cases:

-   If your organization uses proprietary devices and applications, create patterns for these items to enable Discovery and Service Mapping to discover them.
-   If you modify key attributes of CI types that had corresponding patterns, modify the relevant patterns to reflect the change.

## Pattern versions

When you customize a pattern, you actually create a copy of the original preconfigured pattern. While Service Mapping or Discovery use the customized version, the original version isn’t deleted. When you download an update of the pattern from the ServiceNow Store, the original pattern is updated, not the customized copy of it.

![A customized copy of a pattern is not updated.](../image/CustomizedPatternUpdate.png "Exclusion of a customized pattern from an upgrade")

If at some point you want to abandon the customized pattern and start using the updated original pattern, you can revert to the original pattern as described in [Choose the pattern version](../task/t_ChoosePatternVersionPatDef.md).

## Patterns users

The following user roles have access to patterns or pattern-related modules and can perform various actions. Note that customizing patterns requires basic knowledge of programming.

<table id="table_pg3_4ts_5gc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Discovery admin

</td><td>

Can view, create, edit, and publish patterns. The role enables users to run discovery, migrate probes or CAPI to patterns, and access discovery logs and dashboards.

</td></tr><tr><td>

PD user

</td><td>

Has read-only access to **Discovery Pattern Log**.

</td></tr><tr><td>

PD admin

</td><td>

Can view, create, edit, and publish patterns.

</td></tr><tr><td>

PDE viewer

</td><td>

Starting with Pattern Designer Enhancements version 3.9.0, users can view **Command Validation Tasks**, **Command Validation Tasks Results**, and **Command List**. The pde\_viewer can view the **Command Validation Tool** modules and related tables, but doesn't have permissions to modify or edit them.

The pde\_viewer role can view the following tables only:

-   Command List \[pd\_command\_list\]
-   Command Validation Task \[pd\_command\_validation\]
-   Command Validation Task Results \[pd\_command\_validation\_results\]
-   Pattern Shared Library Mapping \[pd\_pattern\_to\_shared\_library\_mapping\]
-   Temporary Variable Mappings \[pd\_temp\_variable\_value\_mapping\]

For more information, see [Discovery commands for probes and patterns](../../discovery/concept/discovery-command-probe-pattern.md).

</td></tr><tr><td>

PD MID

</td><td>

Not assigned to a user directly but to the MID Server record or the user under which the MID Server runs. The role enables the MID Server to interpret and run pattern-based probes.

</td></tr><tr><td>

MID Server

</td><td>

Can grant the MID Server access to the instance.

</td></tr></tbody>
</table>## Patterns for instances using domain separation

In instances that use domain separation, patterns might be domain-specific, covering only the domains that you created them for, or global, applying to all domains.

Patterns belong to domains. By default, all preconfigured patterns are assigned to the global domain and apply to all domains of all levels.

You can create patterns for specific domains. In that case, the new pattern is used only for this domain and doesn’t exist in any other domains. If you customize an existing pattern in the global domain and assign it to a specific domain, you create a copy of the global pattern. The original global pattern is still used for all other domains except for the domain that has the customized version of this pattern. Likewise, if you customize the pattern belonging to the global domain, the change affects all domains except for the one that uses a customized copy of this pattern.

![Patterns may be domain-specific or global.](../image/DomSepPatterns.png "Global or domain-specific patterns")

## Pattern creation or modification flow

Typically, you maintain two ServiceNow instances in your organization: for production and for development. Create or modify patterns, test them, and verify results in the development instance. When you are satisfied with the discovery results, export relevant patterns from the development instance to create an update set. Then you retrieve and commit the update set in your production instance.

If you’re creating a pattern for applications and devices that aren’t supported in the ITOM Visibility global content application, start from creating CI types for them.

![Flow describing pattern creation and modification](../image/PatternCreationFlow.png "Pattern creation flow")

1.  [Available discovery patterns](available-patterns.md)  
ITOM Visibility comes with an extensive library of patterns.
2.  [Configuring Pattern Designer and related applications](../reference/configuring-pattern-designer-plugins.md)  
Install the latest available versions of the ServiceNow applications to use the latest discovery patterns.
3.  [Create CI types for Service Mapping and Discovery](../task/t_CreateCITypeForSM.md)  
Create CI types \(or CI classes\) for applications and devices, which Service Mapping and Discovery do not support by default.
4.  [Create entry point types for Service Mapping](../task/t_CreateEntryPoint.md)  
An entry point is a point where clients access a service instance. Service Mapping starts the mapping process for every application service from the entry point you define for it. Service Mapping includes a wide range of preconfigured entry point types that cover most commonly used applications. If your organization uses a less known or proprietary application that does not have a corresponding entry point type in Service Mapping, you must create it.
5.  [Create or customize patterns](../task/t_CreatePatternPatDef.md)  
Create or modify a discovery pattern and define its basic attributes.
6.  [Discover related items together with the main CI](../task/add-related-cis-to-the-main-ci-pattern.md)  
Add related items to the patterns to perform horizontal discovery of configuration items with all their related items: CIs or non-CIs, like ports or serial numbers.
7.  [Enhance patterns without changing their identification sections](../task/modify-pattern-using-extensions.md)  
Enable patterns to search for additional attributes and modify pattern discovery logic defined in identification sections by using extension sections. Each extension section contains a preconfigured set of discovery steps referred to as a shared library.
8.  [Fine-tune patterns using traffic-based discovery](../task/connection-section-traffic-based.md)  
As an alternative to customizing the pattern from the Pattern Designer side, improve existing patterns so that Service Mapping can use them to find configuration item \(CI\) connections previously found using traffic-based discovery.
9.  [Finalize a pattern](../task/t_FinalizePatternPatDef.md)  
After you finish defining your pattern, make it ready for use by Service Mapping and Discovery.
10. [Copy patterns from one instance to another](../task/export-patterns.md)  
To copy patterns from one instance to another, create an update set containing new or modified patterns with their related items in your development instance. Then, import the update set into your production instance.
11. [Choose the pattern version](../task/t_ChoosePatternVersionPatDef.md)  
Every time you modify and save a pattern, you create a version of this pattern. Choose which pattern version Service Mapping and Discovery use for discovery.
12. [Activate a disabled pattern](../task/activate-disabled-pattern.md)  
If you want to use a pattern for discovery that's disabled by default, activate it manually.
13. [Improved query performance with direct field population in CI tables](query-service-account-ldc-fields.md)  
The **Populate Service Account and LDC IN CMDB** scheduled job populates the Service Account and Logical Datacenter fields in cloud configuration item \(CI\) tables, and the Virtual Machine Object field in the Hardware \[cmdb\_ci\_hardware\] table. This direct population reduces query complexity and improves query performance.

**Parent Topic:**[ITOM Visibility](../../it-operations-management/reference/itom-visibility-landing-page.md)

**Related topics**  


[Detailed information on products discovered by ITOM Visibility](../reference/r_SupportedApplications.md)

[Class diagrams and class attributes for key CMDB classes](https://www.servicenow.com/docs/access?context=c_ConfigurationManagementDatabase&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

[Description of key CMDB tables in the base system](https://www.servicenow.com/docs/access?context=cmdb-tables-details&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

[CMDB CI Class Models: ServiceNow Store app that adds class models that extend the base CMDB class hierarchy](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

[Information about the various options for populating the CMDB](https://www.servicenow.com/docs/access?context=c_OptionsToPopulateCMDB&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

[ServiceNow Store apps that provide pre-defined Service Graph connectors for importing and integrating common third-party data into CMDB classes](https://www.servicenow.com/docs/access?context=cmdb-third-party-integrations&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

[KB0747679: Pre/Post Processing Scripts for patterns](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0747679)

[Application patterns for the Agent Client Collector](../../agent-client-collector/concept/application-patterns-acc.md)

[Certificate Inventory and Management patterns](../../discovery/reference/cert-invt-mgmt-patterns.md)

