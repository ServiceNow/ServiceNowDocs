---
title: Discover related items together with the main CI
description: Add related items to the patterns to perform horizontal discovery of configuration items with all their related items: CIs or non-CIs, like ports or serial numbers.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Discover related items together with the main CI

Add related items to the patterns to perform horizontal discovery of configuration items with all their related items: CIs or non-CIs, like ports or serial numbers.

## Before you begin

1.  \(Optional\) Check if the CI is dependent: The system uses the identification rules to identify the CI independently of other CIs. Refer to [Create or edit a CI identification rule](https://www.servicenow.com/docs/access?context=t_CreateCIIdentificationRule&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
2.  \(Optional\) To understand the model better, check dependent relationship rules which define the dependency structure of the CI types and the relationship types in these service definitions. For example, you can discover a Tomcat server with Tomcat WARs belonging to it. For more information, refer to [Dependent relationship rules](https://www.servicenow.com/docs/access?context=c_ServiceRulesMetadata&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    ![Checking hosting rules under Metadata Editor](../image/metadata-rules-tomcat-war-eg.png "Example of the Containment rule for Tomcat WAR")

3.  To add a non-CI to the pattern, add it as a related item for the CI type to which the main CI belongs. For more information on adding related items for the CI type, see [Configure references to other CIs or non-CIs as related items for the CI type](t_CreateCITypeForSM.md#configure-ci-related-items).

Role required: pd\_admin

## About this task

Related items, both CIs and non-CIs, serve as a reference and provide additional information about the CI. For example, you can define a serial number, a port and an network APR table as related items for a hardware server. The system does not use these items for identification. After you configure related items for the CI type, you can use horizontal discovery for CIs of this type together with their related items.

**Note:** Non-CIs are items that do not extend the Configuration Item \[cmdb\_ci\] table. Examples of non-CIs are ports, serial numbers, or Network ARP tables.

Pattern Designer displays attributes of related CI types, which you added to the pattern in the CI attributes pane. You can view and use these attributes while creating or modifying the main CI pattern.

## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Discovery Patterns**.

2.  Select the relevant pattern.

3.  On the pattern form, select the relevant identification section.

4.  Make sure that you are not in Debug mode.

5.  On the **CI Attributes** pane, click the **Manage related CIs** icon.

    ![Add related CIs icon.](../image/PatDefRelatedCIs.png)

6.  Select the relevant related CI type.

    You can use the search box to locate a specific CI type.

7.  Click the Plus icon.

    The new related CI type is added to the list.

8.  Add other related CI types.

9.  Click **OK**.

    New tabs for related CI types you added appear under the tab for the main CI:

    ![Related CI types appear under additional tabs.](../image/PatDefRelatedCIsAdded.png)


## What to do next

Continue editing the pattern by adding more steps as necessary. To view or use attributes of a related CI type, click the relevant tab in the **CI Attributes** pane.

**Parent Topic:**[Discovery patterns used by ITOM Visibility](../concept/c_MappingPatternsCustomization.md)

**Previous topic:**[Create or customize patterns](t_CreatePatternPatDef.md)

**Next topic:**[Enhance patterns without changing their identification sections](modify-pattern-using-extensions.md)

