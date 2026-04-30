---
title: Enhance patterns without changing their identification sections
description: Enable patterns to search for additional attributes and modify pattern discovery logic defined in identification sections by using extension sections. Each extension section contains a preconfigured set of discovery steps referred to as a shared library.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Enhance patterns without changing their identification sections

Enable patterns to search for additional attributes and modify pattern discovery logic defined in identification sections by using extension sections. Each extension section contains a preconfigured set of discovery steps referred to as a shared library.

## Before you begin

If your ServiceNow instance uses domain separation and you have access to the global domain, log in to the relevant domain. The selected domain must be a domain without any child domains.

Basic knowledge of programming is desirable.

Role required: pd\_admin

## About this task

Patterns can be of the infrastructure or application type. Infrastructure patterns are used only by Discovery for creating lists of devices. Application patterns serve both Service Mapping and Discovery, which use the same application patterns for their purposes. Each pattern including its identification and connection sections is an individual file. There are also reusable sequences of discovery steps referred to as shared libraries. Each shared library is an individual file, but it is always part of the infrastructure or application pattern and is not used as a standalone pattern. Records for both patterns and shared libraries reside in the Discovery Patterns \[sa\_pattern\] table.

To modify the discovery logic in identification sections without changing the identification sections themselves, you can add extension sections to the pattern. Every extension section consists of a shared library, either new or existing.

![Adding an extension section to a pattern.](../image/PatternExtensionSections.png "Adding an extension section to a pattern")

When you create or modify a shared library in the extension section, you save changes only to the shared library, not to the pattern containing this extension section.

**Warning:** The changes to the shared library affect all patterns using this shared library.

The MID Server runs extension sections after identification sections and only if at least one identification section completes successfully.

If there are more than one extension sections associated with this pattern, define the order in which the MID Server runs these extension sections.

You can deactivate shared libraries, so that patterns using them, skip steps in deactivated shared libraries. For more information, see [Discovery Configuration Console](../../discovery/concept/c_DiscoveryConfigurationConsole.md#). If a precondition defined for a shared library step is not fulfilled, the pattern skips all steps belonging to this shared library. For example, if the file, to which the variable points, does not contain "test", the pattern does not run the shared library steps 1-1 to 1-5. The precondition exists only for the pattern within which you created it. The precondition does not affect other patterns using this shared library.

![Precondition for a shared library step](../image/shared-library-precondition.png "Library Reference operation form")

## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Discovery Patterns** and open the required pattern from the pattern list.

    The pattern can be of the Infrastructure or Application type.

2.  To create an extension section and define discovery steps for its shared library.

    1.  Click **New** under **Extension section**.

    2.  Enter the name of this extension section.

    3.  Click **Done**.

        The pattern form displays the new section under **Extension section**.

    4.  Click the name of the new extension section.

        The Pattern Designer opens showing the Steps tree on the left.

        If no discovery steps have been identified for this pattern, the **Untitled Step** appears in the Steps tree in the left pane of the window.

    5.  Define discovery steps.

    6.  Click **Save** to save the extension section and make Service Mapping and Discovery use it.

        You do not publish extension sections.

3.  To use an existing shared library for the new extension section:

    1.  Click **Add** under **Extension section**.

    2.  Select the shared library from the name list.

4.  If there are more than one extension sections, define the order in which the MID Server runs the extension section.

    1.  Select the check box next to the extension section.

    2.  Click **Edit** under **Extension section**.

    3.  Enter a number that determines the order in the **Order** field.

        If there is only one extension section, its order is **1** by default.

        The section with the lowest order number is used first.

    4.  Click **Done**.


## What to do next

Click **Debug** to run the newly created extension section. Pattern Designer runs extension sections after running identification sections.

**Parent Topic:**[Discovery patterns used by ITOM Visibility](../concept/c_MappingPatternsCustomization.md)

**Previous topic:**[Discover related items together with the main CI](add-related-cis-to-the-main-ci-pattern.md)

**Next topic:**[Fine-tune patterns using traffic-based discovery](connection-section-traffic-based.md)

