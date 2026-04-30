---
title: Discovery identifiers
description: After Discovery classifies a configuration item \(CI\), it uses identifiers to determine if the device already exists in the CMDB.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-24"
reading_time_minutes: 5
breadcrumb: [Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery identifiers

After Discovery classifies a configuration item \(CI\), it uses identifiers to determine if the device already exists in the CMDB.

Discovery launches special identity probes that accumulate identification data for each device and feed that data into the identifiers, which determine the action that Discovery must take for each device. Identifiers accurately determine the identity of the device to avoid the creation of duplicate CIs. This identification step only takes place for the Configuration item type of discovery, not for the other types of discovery.

The identity probe in the base Discovery system can be configured to ask the device for information such as its serial numbers, name, and network identification. The results of this scan are processed by an identity sensor, which then passes the results to the identifier. The identifier then attempts to find a matching device in the CMDB. If the identifier finds a matching CI, the identifier either updates that CI or does nothing. If the identifier cannot find a matching CI, it either creates a new CI or does nothing. If Discovery is configured to continue, the identifier launches the exploration probes configured in the classification record to gather additional information about the device. Exploration probes can be multiprobes or simple probes.

**Important:** Serial numbers are necessary for accurate asset tracking. If you modified baseline probes, sensors, or patterns, verify that they still discover serial numbers. In addition, do not configure sensors or patterns to modify the serial number syntax, such as adding a custom prefix. Non-standard serial numbers can lead to inaccurate asset tracking.

This diagram shows the processing flow for classifying and probing devices with identifiers configured.

![Discovery identifiers](../image/DiscoveryIdentifiersDiagram.png)

## CMDB identifier tables

|Table|Description|
|-----|-----------|
|Identifier \[cmdb\_identifier\]|Stores all identifier rules.|
|Identifier Entry \[cmdb\_identifier\_entry\]|Stores all the identifier attributes.|

## Identifier rules

The default Discovery system contains these identifier rules, each of which is associated with a specific CI type \(the **sys\_class\_name** field on the CI record\) or the table in the **Applies to** field and contains the appropriate attributes for discovering CIs from the specified table. Where necessary to discover all possible occurrences of an attribute, tables from related lists \(**Search on** tables\) are included in the rule. For more information, see [Create or edit a CI identification rule](https://www.servicenow.com/docs/access?context=t_CreateCIIdentificationRule&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

<table id="table_r2p_1ql_lt"><thead><tr><th>

Rule

</th><th>

Applies to table/attributes

</th><th>

Search on table/attributes

</th></tr></thead><tbody><tr><td>

ESX Server Rule

</td><td>

ESX Server \[cmdb\_ci\_esx\_server\]: correlation\_id

</td><td>

none

</td></tr><tr><td>

Hardware Rule

</td><td>

Hardware \[cmdb\_ci\_hardware\]-   serial\_number
-   serial\_number\_type
-   name
-   ip\_address
-   mac\_address

</td><td>

-   Serial Number \[cmdb\_serial\_number\]
    -   serial\_number
    -   serial\_number\_type
-   Network Adapter \[cmdb\_ci\_network\_adapter\]
    -   ip\_address
    -   mac\_address

</td></tr><tr><td>

Storage Server Rule

</td><td>

Storage Server \[cmdb\_ci\_storage\_server\]-   cim\_object\_path
-   name
-   serial\_number
-   serial\_number\_type
-   mac\_address
-   ip\_address

</td><td>

-   Serial Number \[cmdb\_serial\_number\]
    -   serial\_number
    -   serial\_number\_type
-   Network Adapter \[cmdb\_ci\_network\_adapter\]
    -   ip\_address
    -   mac\_address

</td></tr><tr><td>

WBEM Service Rule

</td><td>

WBEM Service \[cmdb\_ci\_wbem\_service\]: cim\_object\_path

</td><td>

none

</td></tr></tbody>
</table>## Matching strategy for the hardware rule

The **sys\_class\_name** cannot be an attribute for independent rules, such as cmdb\_ci\_hardware. If your Discovery identification strategy depends on matching a CI with a specific class, you must create a rule for each class you want to use for matching and specify that class in the **Applies to** field of the Identifier form.

For example, you can create an identifier for a Linux server with different attributes than the Hardware Rule. You might want to use the machine name, IP address, and MAC address for identification. This is a solution for networks that use NIC bonding or teaming to increase available bandwidth. Bonded interfaces appear to be the same physical device and share the same IP and MAC addresses. The use of the **name** attribute allows Discovery to differentiate between the individual interfaces in the bonded channel.

**Important:** If you create an identifier with the **name** attribute, avoid changing adapter names. Discovery will be unable to resolve existing CIs for renamed adapters. Discovery labels the Install Status of that CI as "Absent" and creates another CI.

Your new rule would look like this:

![Linux identifier rule](../image/linux-identifier-rule.png "Linux identifier rule")

## Evaluation order for Discovery identifiers

Custom identifiers must have different Order values than those of the default identifiers. Discovery parses identifiers and attributes in sequence from low order numbers to high. You can create identifiers to run before or after the default identifiers, or mixed in with the identifiers from the base system. To avoid any identifier or rule from running, disable it by clearing the **Active** check box. The evaluation order for CMDB identifiers is established within each rule and only controls the parsing order of the attributes in that rule.

![CMDB identifier rules](../image/cmdb-identifier-rule-order.png "Evaluation order in CMDB identifier rules")

## Properties for processing duplicate CIs

You can control how Discovery handles duplicate CIs with properties installed with Identification and Reconciliation. Use the `glide.identification_engine.skip_duplicates` and `glide.identification_engine.skip_duplicates.threshold` properties. For more information, see [Properties for Identification and Reconciliation](https://www.servicenow.com/docs/access?context=properties-id-reconciliation&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

## Properties that control identifier versions

All instances use identifiers from the CMDB Identification and Reconciliation framework. Upgrades from pre-Geneva versions still preserve the legacy identifiers, but you can switch to the new identifiers using a property: `glide.discovery.use_cmdb_identifiers`. If you upgraded from a pre-Geneva version, you must manually add this property and set it to `true` to use the new identifiers. If you upgraded from Geneva or later releases, this property is available in the System Properties \[sys\_properties\] table. To preserve functionality in custom legacy identifiers, convert them to the new CMDB identifier rules format before enabling this property. The system does not reconfigure your custom identifiers to the new framework automatically.

**Note:** When Service Mapping is active, the new identifiers from the CMDB Identification and Reconciliation framework are always used regardless of the property value.

-   **[How Discovery identifiers work](c_HowDiscoveryIdentifiersWork.md)**  
When Discovery has determined the device's class, it launches an identity probe that is configured to run one or more commands with a single authentication.
-   **[Configure Discovery identity probes](../task/t_ConfigureDiscoveryIdentityProbes.md)**  
Identity probes are multi-probes, which contain one or more simple probes configured to extract specific information from manageable devices. You can create your own identity multi-probe to identify CIs that Discovery does not already identify.
-   **[Configure Discovery identity sensors](../task/t_ConfigDiscoIdentSens.md)**  
If you customize an identify multi-probe, you can also configure a multi-sensor for it.
-   **[Serial number types for identification](../reference/r_SerialNumberTypes.md)**  
As Discovery finds CIs, their serial numbers are listed in the Serial Number \[cmdb\_serial\_number\] table so they are easy to identify. Serial number types vary depending on the CI, as described in the following examples.

**Parent Topic:**[Configuring Discovery](c_DiscoveryConfiguration.md)

