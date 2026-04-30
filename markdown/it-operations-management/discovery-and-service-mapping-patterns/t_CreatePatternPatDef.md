---
title: Create or customize patterns
description: Create or modify a discovery pattern and define its basic attributes.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2024-02-01"
reading_time_minutes: 4
breadcrumb: [Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Create or customize patterns

Create or modify a discovery pattern and define its basic attributes.

## Before you begin

Make sure that the application for which you want to create a pattern, has a corresponding configuration item \(CI\) type and a CI classification. If the CI type you require is not in the list, create it as described in [Create CI types for Service Mapping and Discovery](t_CreateCITypeForSM.md).

If your ServiceNow instance uses domain separation and you have access to the global domain, log in to the relevant domain. The selected domain must be a domain without any child domains.

Role required: pd\_admin

Basic knowledge of programming is desirable.

## About this task

Patterns can be of the infrastructure or application type. Infrastructure patterns are used only by Discovery for creating lists of devices. Application patterns serve both Service Mapping and Discovery, which use the same application patterns for their purposes.

## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Discovery Patterns**.

2.  Click **New** or select the relevant pattern from the list.

3.  Define the basic pattern attributes on the **Basic** tab.

<table id="table_wvm_h2p_ls"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Pattern type**

</td><td>

-   Select **Application** for an application pattern. It can be used both for top-down discovery performed by Service Mapping and horizontal discovery performed by Discovery.
-   Select **Infrastructure** for an infrastructure pattern used for the horizontal host discovery performed by Discovery.


</td></tr><tr><td>

**Name**

</td><td>

Enter the pattern name. This name must be unique to this pattern. Use self-explanatory names such as `Apache on Unix pattern`.

</td></tr><tr><td>

**CI type**

</td><td>

Select the [CI type](t_CreateCITypeForSM.md) which you want this pattern to discover.**Note:** Discovery can find multiple CIs that belong to the same CI type.

</td></tr><tr><td>

**Operating system** \[Application patterns only\]

</td><td>

Select the operating system that the selected CI runs:-   Click **All** if the CI runs on more than one operating system.

Or

-   Select the relevant operating systems from the list.


</td></tr><tr><td>

**Run Order** \[Application patterns only\]

</td><td>

For an application pattern used by Service Mapping, define when the pattern runs1.  Select the order in which this pattern always runs:
    -   **Before**
    -   **After**
2.  Then select the other applicable pattern. This field is only relevant if a particular pattern can be confused with another pattern.
For example, both IIS and MS Exchange applications have an HTTP entry point. However MS Exchange uses some of the components of IIS. Therefore, if the IIS pattern ran first, discovery might incorrectly identify MS Exchange as IIS. To prevent this error, in the **Run Order** field in the MS Exchange pattern definition, select **Before** and **IIS**.

</td></tr><tr><td>

**Description**

</td><td>

Provide a description for this pattern.

</td></tr></tbody>
</table>4.  When creating an application pattern, make the MID Server run this pattern only if the process identified on a CI matches the classification criteria for this pattern, select **Enforce Process Classification**.

    All simplified patterns created from generic applications, have this attribute enabled. For more information about creating process classification, see [Discovery classifiers](../../discovery/concept/discovery-classifiers.md).

5.  Define a set of identification steps for every incoming connection of a configuration item \(CI\) as described in [KB1698521: Create or customize patterns](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1698521).

6.  If necessary, create more identification sections.

7.  Save the pattern.

8.  To test the pattern, select **Debug Mode** and enter the IP address of the host.

9.  Upload the updated set of patterns onto the MID Server:

    1.  Navigate to **Discovery** &gt; **MID Servers**.

    2.  Alternatively, navigate to **Service Mapping** &gt; **MID Servers**.

    3.  Click **Pattern Sync to Mid**.


## What to do next

For application type patterns, continue with creating a connection section as described in the KB article [KB1698521: Create or customize patterns](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1698521).

**Parent Topic:**[Discovery patterns used by ITOM Visibility](../concept/c_MappingPatternsCustomization.md)

**Previous topic:**[Create entry point types for Service Mapping](t_CreateEntryPoint.md)

**Next topic:**[Discover related items together with the main CI](add-related-cis-to-the-main-ci-pattern.md)

**Related topics**  


[Discovery for cloud environment](../../discovery/concept/cloud-discovery-wizard.md)

[KB0747679: Pre/Post Processing Scripts for patterns](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0747679)

[KB0854603: Pattern Debugger Session Timed Out](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0854603)

