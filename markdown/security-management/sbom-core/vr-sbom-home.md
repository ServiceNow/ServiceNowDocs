---
title: Review the Home page in the Software Bill of Materials Workspace
description: Uploaded data is rolled up to the visualizations on the landing \(Home\) page in the Software Bill of Materials \(SBOM\) Workspace. Data is modified after you upload files so vulnerability analysts can see trends and review current information about your components.
locale: en-US
release: zurich
product: SBOM Core
classification: sbom-core
topic_type: task
last_updated: "2025-09-09"
reading_time_minutes: 4
breadcrumb: [Reviewing reports and dashboards, Use, Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# Review the Home page in the Software Bill of Materials Workspace

Uploaded data is rolled up to the visualizations on the landing \(Home\) page in the Software Bill of Materials \(SBOM\) Workspace. Data is modified after you upload files so vulnerability analysts can see trends and review current information about your components.

## Before you begin

Roles required: sn\_sbom\_resp.sbom\_analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **SBOM Workspace**.

    By default, the landing page \(Home\) is displayed.

    What you can see in the module depends on the applications you have installed.

    Imported data is not calculated and populated by live queries. Scores on the Home and Components pages are updated once daily with performance enhancements for reporting. This enhancement might provide you with faster load times for the scorecards on the Home and Components modules in the SBOM Workspace.

    These enhancements have no impact on how or where data is stored.

<table id="table_bh2_4rs_ydc"><thead><tr><th>

Installed application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

If you have installed SBOM Core

</td><td>

All BOM entities. The list includes the Name, Classifier \(Application, Container, Library, and so on\) and the component count for each entity. A BOM entity refers to the root level component in an SBOM file for which an SBOM document was generated and uploaded.

 Navigate to the Home page in the workspace to view the list of BOM entities.

</td></tr><tr><td>

If you have installed SBOM Response

</td><td>

The following data visualizations are displayed.-   All BOM Entities - A breakdown of BOM entities by type: Application, Container, Library, and Others. A BOM entity refers to the root level component in an SBOM file for which an SBOM document was generated and uploaded.
-   BOM Entities with Vulnerabilities - Entities that have a vulnerability associated with any component that they depend on. If an entity dependency has one **Critical** vulnerability, the entity's severity is considered critical.
-   Active AVIs - The trend for the number of application vulnerable items \(AVI\)s created each day.
The data visualizations display data for the last 30 days. The 30-day range isn’t editable. This data is available after you've reviewed and set up the creation rules for application vulnerable items. For more information, see [Creating rules for application vulnerable items in the Software Bill of Materials Workspace](../task/vr-sbom-config-sbom-response.md).

</td></tr></tbody>
</table>2.  Select a data visualization card to see its list of records.

3.  Select the **Home** tab to return to the landing page.

4.  Alternatively, select a record under the **BOM Entities** list.

    The entity name and version is displayed at the top of the record, for example, `SNC-SECOPS-SIR2.0`.

    **Note:** With the License administration module, the entity-license relationship is not displayed on this list. To view the entities where a component is used, navigate to the components module and open a component record. On the component record, you can view the State: Unresolved or Unclassified.

5.  Select the tabs on the entity record to review the data.

    1.  If not selected, select the **Overview** tab.

        Review the data. If a field isn’t populated on this record, the data wasn’t included with the SBOM files you uploaded.

        |Name|Description|
        |----|-----------|
        |Name|Entity name.|
        |Classifier|Entity type, for example, an application, component, or library.|
        |Version|Version number of the entity.|
        |Supplier|The product that supplied the entity.|
        |Product model|If there’s no existing product model or if you don't include one at the time of your SBOM upload via the API, one is created. The name of the entity is used for the product model record, for example `SNC-SECOPS-SIR2.0`.|

    2.  Select the **Depends on** tab.

        All the dependencies of this entity are listed as well as classifiers, for example, `Library`. The version number, `Licenses`, and other information are displayed.

        Selecting a link on this list opens a record. Its tab is displayed below the Home and entity record tabs. The record you open might include the following related lists you can review: Overview, Hashes, BOM Entities, Vulnerabilities, and application vulnerable items \(AVITs\).

        The BOM Entities related list displays all the entities that this displayed item is used in.

    3.  Select the **Vulnerabilities** tab to see the vulnerabilities associated with a dependency of this entity.

        For more information about the vulnerabilities displayed for an entity, see [View upload status for Software Bill of Materials files](../task/vr-sbom-bom-queue.md).

    4.  Select the **AVIs** tab to see if there are application vulnerable items for this entity.

6.  After you review records, you can delete one or more BOM Entity records if you determine you no longer need them.

    **Note:** Deleting BOM entity records permanently removes them and their component relationships. Any application vulnerable items \(AVIT\)s that are associated with the BOM entities transition to **Closed**. If you decide later that you want the records and component relationships you delete back on the BOM entities list and available in the workspace, you must upload these BOM entities again.

    1.  If not on the Home page, select the **Home** tab to return to it.
    2.  Select the records\(s\) under the **BOM Entities** list that you want to delete.
    3.  Select **Delete**.

