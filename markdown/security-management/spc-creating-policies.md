---
title: Creating your own policies in the Security Posture Control application
description: You can create your own custom policies to monitor data that is specific to the assets in your environment. You base these policies on data you will import from the various Service Graph Connectors you have installed and activated.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-08-18"
reading_time_minutes: 6
breadcrumb: [Policies, Explore, Security Posture Control, Security Operations]
---

# Creating your own policies in the Security Posture Control application

You can create your own custom policies to monitor data that is specific to the assets in your environment. You base these policies on data you will import from the various Service Graph Connectors you have installed and activated.

## How to start

You can clone existing policies and add more conditions to them or create a policy from scratch. For your custom policies, you can include criteria for common CMDB properties populated by various Service Graph Connectors.

Alternatively, you can use a base policy as a starting point and include conditions for approved exceptions with polices for the Governance, Risk, and Compliance \(GRC\) application, for example. These exceptions are for assets that you don’t want to monitor and include in your asset counts.

For your custom policies, you can include conditions for metadata such as OS, OS version, and FQDN, for example to help you monitor assets with older software. Note that these properties are common CMDB properties populated by various Service Graph Connectors for any given asset.

See [Policies included with the Security Posture Control application](../concept/spc-polices-included.md) for more information about top-level Asset Types and their relationships in the policy condition builder for you policies.

For example policies, see [Examples of base, child, and cloned policies for Security Posture Control](../concept/spc-policy-examples.md).

See [Create and activate custom policies for Security Posture Control](spc-create-policy.md) for more information about the steps required to create a policy.

## Using the AND, OR decorators in the condition builder

You navigate from the top-level asset types for hardware and software to their secondary entities by using the condition builder in the Policies and findings module in the workspace. Depending on your choices, fields are displayed for you and you modify or add criteria.

The AND, OR decorators in the condition builder permit you to set up the logic for the returned data you want returned for the policy.

|Decorator|Description|Number referenced in the image|
|---------|-----------|------------------------------|
|Select **AND** next to the top-most Connection and Entity fields for new set of conditions.|Adds a logical AND between the current Connection-Entity criteria, and new criteria from another Connection-Entity.|1|
|Select **AND** to the right of a Criteria or Property field for new set of Criteria and Property conditions.|Adds a logical AND between the current Connection-Entity criteria, and a new criteria under the same Connection-Entity.|2|
|Select **OR/AND** to the right of a Property field for new set of Property conditions.|Adds a logical OR/AND between current Property, and a new Property from the same Connection-Entity-Criteria.|3|
|Select **+ New condition set** for a new set of conditions.|Adds a logical OR between the Condition Set of all current Criteria, and a new Condition Set.|4|

![Decorators in the security posture control policy builder](../image/spc-decorators.png)

## Using base policies, cloning, and child policies

You can use multiple policies to evaluate your assets and create your own custom insights. You have the following options to help you create custom or edit existing policies quickly:

-   Clone policy - Create a copy of a policy. The name of the policy and its conditions are displayed with a ‘copy’ in the title. The conditions are displayed, and you can edit them. See [Edit an activated policy in Security Posture Control](spc-edit-policy.md).
-   Create child policy - The name of the policy you started from is displayed as the “Base policy” on the new record. Conditions of your base policy are inherited in the new policy, and a new, empty condition set is displayed. See [Clone a policy or create a child policy in Security Posture Control](spc-clone-policy.md).
-   Exclusion policies – Add policies to your custom policies so that asset findings from the policies you select are excluded from your results. See [Create and activate custom policies for Security Posture Control](spc-create-policy.md).

## Metadata and CMDB filtering

It might be important for your security teams to monitor assets with older software. You can specify policy criteria starting with the Connection ‘With CMDB Metadata’ after the Hardware Asset type to include the common properties listed below. This is not an all-inclusive list. In order to gather this metadata, the properties must be available from the CMDB Metadata connection populated by your service graph connectors.

-   RAM
-   Host name
-   Serial number
-   OS Domain
-   OS Version
-   Disk Space
-   Last seen
-   OS
-   First seen
-   CPU Count
-   MAC Manufacturer
-   NIC
-   IP Address
-   Location
-   FQDN
-   Netmask
-   IP Version
-   Serial Number Type
-   OS Service Pack

Starting with v3.0 of Security Posture Control:

The Connection ‘With CMDB Metadata’ permits you to add the Host name Property and use the matches regex Operator to help you type in regular expressions in your conditions for the Hardware Asset type. For example, if you enter ‘lp’, you can look for all laptops with 'lp' as the second and third characters in the host name.

'First seen': Assets that have been discovered for the first time by any source within the time frame you select with the 'First seen' timestamp Property.

'Last seen': Assets that were 'Last seen Within the last n days' by any source. Enter the number of days up to 30 as a Value. For example, enter 3 as a Value to monitor assets by 'last logon' from Active Directory in the last three days.

Software Asset type: Look for software publishers or use SGCs you have installed that import software data and metadata you want if you start with the Connection ‘With software details’.

For Hardware asset types, you can use the Connection ‘Has model info’ with the Connection ‘With CMDB Metadata’ for devices based on specific models and model information.

Hardware Asset types also permits you to search for all assets reported by a Source, Qualys, for example, but that are not reported by ServiceNow ITOM Discovery.

See [Policies for Security Posture Control](../concept/spc-policies-overview.md) for more information about the Security Posture Control policy schema.

## Exceptions with the Governance, Risk, and Compliance \(GRC\) application

An Integrated Risk Management \(IRM\) exception is an asset with an approved exception from the Governance, Risk, and Compliance \(GRC\) product. You have the option in a policy to add a condition for an exception so you don’t monitor these assets and include them in your counts.

For example, some assets might have exceptions approved for certain control objectives with IRM. To reduce your returned matches, information security teams might want to exclude those assets from monitoring for security controls with IRM exceptions that are already approved.

