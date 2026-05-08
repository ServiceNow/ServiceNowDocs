---
title: Automatic CI field population
description: Discovery generic attributes can automatically set configuration item \(CI\) field values during discovery. Attributes follow a scope hierarchy, where more specific scopes override broader ones, enabling you to define defaults at the schedule level and apply precise values at the range level.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 3
breadcrumb: [Discovery generic attributes, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Automatic CI field population

Discovery generic attributes can automatically set configuration item \(CI\) field values during discovery. Attributes follow a scope hierarchy, where more specific scopes override broader ones, enabling you to define defaults at the schedule level and apply precise values at the range level.

## Benefits

Using generic attributes to populate CI fields provides the following benefits:

-   Eliminate the need to create separate Discovery schedules for each location or group of CIs that require different field values.
-   Set CI field values at the schedule, range set, or IP address range level, providing precise control over location data, asset tags, and other fields.
-   Reduce manual CI updates after discovery by automatically populating fields during the discovery process.
-   Use the attribute hierarchy to define broad defaults at the schedule level and override them with more specific values at the range set or range level as needed.

## How it works

Previously, CI field values such as location could only be set globally on a Discovery schedule. This meant that all CIs discovered within a schedule inherited the same value, even when more specific information was available for individual IP addresses or range sets.

Generic attributes solve this problem by enabling you to define field values at multiple levels of granularity. When discovery runs, it evaluates the attributes defined at each scope level and applies the most granular matching attribute to each discovered CI.

## Scope levels

You can define generic attributes to populate CI fields at the following scope levels. Each level represents a different degree of granularity.

|Scope|Description|
|-----|-----------|
|Schedule|Applies the attribute value to all CIs discovered within the entire schedule.|
|Range set|Applies the attribute value to all CIs discovered within a specific range set associated with the schedule.|
|Range|Applies the attribute value to all CIs discovered within a specific IP network, IP address range, or IP address list.|

## Attribute hierarchy

When attributes are defined at multiple levels, Discovery applies the most granular value to the resulting metadata, which can influence both CMDB field population and Discovery runtime behavior. The scope hierarchy from least to most granular is: schedule, range set, IP address range. A range-level attribute overrides a range set-level attribute, which overrides an IP network-level attribute, and so on. Additionally, attributes can target specific CMDB CI classes. When attributes with the same key exist for different classes within the same class hierarchy, the more specific class takes precedence. If no attribute is defined at a more granular scope or specific class, the CI inherits the value from the next available level.

For example, set the **Location** field to Maryland at the schedule level, Baltimore at the range set level, and a specific street address at the range level. A CI discovered from an IP address in that range inherits the street address. A CI discovered from a different IP address in the same range set inherits Baltimore, because no range-level location is defined.

## Field value types

Discovery generic attributes support two types of field values.

|Type|Description|
|----|-----------|
|Reference|A value that references a record in another table. For example, the Location field references a record in the Location \[cmn\_location\] table.|
|Static|A string value that you enter directly. For example, you can set the Asset tag field to a custom string value.|

## Target table filtering

Each attribute includes a Target Table field that specifies which CI class the attribute applies to. You can set the target table to the base Configuration Item \[cmdb\_ci\] table to apply the attribute to all discovered CIs. To restrict the attribute to a specific class and its child classes, select a more specific class, such as Linux Server \[cmdb\_ci\_linux\_server\].

## Example

The following example illustrates how the attribute hierarchy works across three scope levels.

A Discovery schedule contains a range set with two IP address ranges. You define the following attributes:

-   **Schedule level: Location** = Maryland \(applies to all CIs in the schedule\)
-   **Range set level: Location** = Baltimore \(target table: Linux Server\)
-   **IP address \(10.0.0.52\): Location** = 123 Main St, Baltimore
-   **IP address \(10.0.0.117\): Asset tag** = tag-test \(static value\)

After discovery runs:

-   The CI discovered at 10.0.0.52 has its **Location** field set to **123 Main St, Baltimore** because the range-level attribute is the most granular.
-   The CI discovered at 10.0.0.117 has its **Asset tag** field set to **tag-test**. Because no range-level **Location** attribute is defined for this IP, the CI inherits **Baltimore** from the range set-level attribute.

