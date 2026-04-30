---
title: Edit or delete a library element
description: You can add artifacts to a library element, or convert a library element back to project-based artifacts. You can also edit the data definitions of artifacts in a library element.Each KPI Composer library element has the following properties. You need the sn\_kpi\_composer.admin or admin role to edit them.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Cross-project library elements, Design your Performance Analytics solution with KPI Composer, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Edit or delete a library element

You can add artifacts to a library element, or convert a library element back to project-based artifacts. You can also edit the data definitions of artifacts in a library element.

## Before you begin

Role required: sn\_kpi\_composer.admin or admin for full editing functions

## Procedure

1.  Open the Analysis tab of a KPI Composer project.

2.  Select the root artifact of one of the library elements in the KPI tree to open its properties.

    Bookmark icons \(![](../image/kpi-comp-bookmark-icon-sm.png)\) identify the artifacts that are in a library element. The root artifacts, or parent artifacts, are the most top-level artifacts in each library element.

    ![A KPI tree with two root artifacts, for each of two library elements.](../image/kpi-comp-root-artifacts.png)

3.  To delete a library element, select **Unlink element from library**.

    ![Artifact properties for an artifact in a library element, showing Unlink element from library link.](../image/kpi-comp-unlink-element.png)

    The artifacts are no longer members of that library element. However, every KPI tree that contained that library element still contains those artifacts, only now they are a separate set of ordinary artifacts in each tree.

4.  To edit a library element, select **Open library element**.

    **Note:**

    -   You can open a library element from any artifact in that element, not only the root artifact.
    -   If you have the sn\_kpi\_composer.admin or admin role, you can instead navigate to **KPI Composer** &gt; **Library** and open a library element from a set of library element tiles.
5.  To add an artifact to the library element, follow the instructions in [Add artifacts to a KPI tree](../concept/design-kpi-tree.md#).

    **Note:**

    -   You do not need to click **Add this element to the library** in the properties of the new artifact. If you click this link, you add the new artifact to a new library element that is nested inside this library element.
    -   Instead of adding a new artifact, you can add another library element, which is then nested inside this library element. For more information, see [Use a library element](use-library-element.md).
6.  To add indicator and report definitions to the artifacts in a library element, open the Data Definition tab and follow the instructions in [Defining indicators and reports](../concept/designing-indicators.md).

7.  Select the information icon \(![](../image/kpi-comp-info-icon-sm.png)\) to view or edit the library element properties, such as whether the library element is global or personal in scope.

    You need the sn\_kpi\_composer.admin or admin role to edit properties. Otherwise, they are read-only.


**Parent Topic:**[Cross-project library elements](../concept/cross-project-artifact-libraries.md)

## Library element properties

Each KPI Composer library element has the following properties. You need the sn\_kpi\_composer.admin or admin role to edit them.

<table id="table_p4n_z4d_mjb"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique, meaningful name

</td><td>

By default, the name is the same as the name of the root artifact, such as Improve Customer Service Quality.

</td></tr><tr><td>

Description

</td><td>

A detailed description of the artifact to help others understand its purpose and to prevent redundancy

</td><td>

Total monetary cost from when an incident is raised until it is resolved, including estimated salary and opportunity costs

</td></tr><tr><td>

Objective

</td><td>

The future performance improvement you want from Performance Analytics. If you do not yet have a quantitative target score for an indicator, describe the target qualitatively.

</td><td>

A 10% reduction every month until a final value of 40 is reached.

</td></tr><tr><td>

Global Yes \| No

</td><td>

When Yes, all users can add this library element to their KPI trees. When No, this library element is personal and only the user who created it can use it. Default: No

</td><td>

N/A

</td></tr><tr><td>

Knowledge Articles

</td><td>

Articles in the knowledge base that contain further explanations about the library element.Specify any of the following details:-   Knowledge articles that contain further explanation about the artifact. You can link any number of knowledge articles.
-   Artifact owners
-   Contact persons

</td><td>

KB0000006 Dealing with Spyware and Viruses

</td></tr><tr><td>

Responsible

</td><td>

A responsible user has full editing privileges but also is expected to be responsible for maintaining the library element. For more information, see [Access to KPI Composer](../concept/access-to-kpi-composer.md).

</td><td>

Abel Tuter

</td></tr><tr><td>

Contacts

</td><td>

A person who is not responsible for the library element but is an interested party or a relevant subject matter expert to consult.

</td><td>

Abraham Lincoln

</td></tr></tbody>
</table>