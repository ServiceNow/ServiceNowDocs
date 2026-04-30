---
title: Resolve licenses to components in the Software Bill of Materials Workspace
description: Resolve \(assign\) classified licenses to specific components with the Component License Resolution feature. Assign licenses to components with missing information or incorrect license information or create new licenses so your overall license compliance can be calculated.
locale: en-US
release: yokohama
product: SBOM Core
classification: sbom-core
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Classifying licenses and resolving component licenses in the Software Bill of Materials workspace, Uploading and viewing your SBOM files in the SBOM Workspace, Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# Resolve licenses to components in the Software Bill of Materials Workspace

Resolve \(assign\) classified licenses to specific components with the Component License Resolution feature. Assign licenses to components with missing information or incorrect license information or create new licenses so your overall license compliance can be calculated.

## Before you begin

Role required: sn\_sbom\_response.licenseresolver

## Procedure

1.  Navigate to **Workspaces** &gt; **SBOM Workspace** &gt; **License administration** &gt; **Component License Resolution**.

    **Note:** Unless you also have the sn\_sbom\_response.managelicense role, only the Component License Resolution tab is visible.

    This page tracks the total number of unique licenses and an at-a-glance view of license totals that have been detected from the SBOM files you’ve uploaded. Licenses displayed on this page fall under two broad categories as they relate to components.

    -   All instances of the component agree on a license.
    -   There is a disagreement on a single license and there is more than one license for a component.
    In the second case, you must reconcile these licenses so a single license is resolved to a single component. License compliance is calculated based on one resolved license per component.

    The licenses on this page are filtered into the following categories to help you resolve them.

    |Value|Description|
    |-----|-----------|
    |Components with unresolved licenses|No license is assigned to the component and it requires resolution. `(empty)` is displayed in the Resolved license column for these components. Both missing and multiple licenses totals are listed as part of this category.|
    |Components with missing licenses.|Components with missing license information that require resolution.|
    |Components with multiple licenses|Components that are visible across multiple entities which have different licenses and require resolution.|
    |All components|Total list of components tracked in your organization. You can change licenses from this filtered list.|

2.  Select a card.

3.  Choose one to resolve a license.

<table id="choicetable_b3f_2f1_zcc"><thead><tr><th align="left" id="d402300e180">

Option

</th><th align="left" id="d402300e183">

Description

</th></tr></thead><tbody><tr><td id="d402300e189">

**Assign an existing license to a component.**

</td><td>

1.  Double-click a field in the Resolved license column for a component.
2.  Select one license from the Resolved License list.
3.  Your edit is saved and the associated card at the top is updated.
4.  Alternatively, select the record from the Name column to open it. It opens in a new tab.
5.  Click the **BOM entities** tab to see where the component is being used.
6.  Select one from the Resolved License list.
7.  Enter a justification.
8.  Select **Save**.
9.  Refresh the page to update it.


</td></tr><tr><td id="d402300e235">

**Change a license for a component that already has one.**

</td><td>

You might choose this option if you determine a license has been incorrectly assigned to a component or needs to change.

 1.  Select the **All components** card.
2.  Locate the component you want to modify.
3.  Select the record from the list to open it.
4.  Select one from the Resolved License list.
5.  Select **Save**.
6.  Refresh the page to update it.


</td></tr><tr><td id="d402300e275">

**Create a license.**

</td><td>

You might use this option if you know a specific license is used in your organization, but a record was not detected from a previous SBOM upload and there is no record for it listed in the License Classification module. 1.  Select **New** on the License Classification tab and fill out the fields.
2.  Name- Unique name for this license.

**Note:** The display name is based on the ID field. If the ID field is not defined, the display name is based on the Name field. If the Name field is not defined, the display name is based on the Expression field.

3.  Classification. Select one:
    -   Unclassified - License requires review and classification.
    -   Banned - License usage is not permitted.
    -   Restricted - License is not permitted in specific use cases.
    -   Permitted - License usage is permitted without restriction.
4.  License type. This information is not used by the system or for a workflow. This information is provided to help you store additional information and categorize your licenses.
5.  URL: Website for license source. This is not used by a workflow or a system.
6.  Expression: Arithmetically combine licenses. For example, `MIT AND Apache-2.0 WITH GPL-2.1-or-later` are combined for an expression. License combinations or expressions are treated as one license in the ServiceNow AI Platform.
7.  Attachments. Add attachment or worknotes.
8.  Select **Save**. This license is added to your database, is displayed on the License Classification page, and can now be detected on components during SBOM uploads.


</td></tr><tr><td id="d402300e345">

**Upload multiple licenses and classifications.**

</td><td>

You might choose this option if you have a file with multiple licenses and classifications that you want to create records for. You can upload files in the specified format and store it in the SBOM license \[sn\_sbom\_license\] table.

 1.  Navigate to the SBOM license \[sn\_sbom\_license\] table.
2.  Select the **More options** menu from any column.
3.  Select **Import**.

On the page that is displayed, either upload an existing compatible template or download the template generated by the Platform \(**Create Excel template**\).

You load the data into this template that is inserted into the table.

4.  **Choose file** and locate your file.
5.  Select **Upload**.

Your file is uploaded, and the records are created in the SBOM license \[sn\_sbom\_license\] table and viewable in the SBOM Workspace on the License Classification page.

</td></tr></tbody>
</table>4.  Navigate to the Home page in the SBOM Workspace to see what percentage of the components you are using are out of compliance in the License classification of components visualization.

    The data for this visualization is updated daily by the License breakdown of BOM components scheduled job. This job is part of the SBOM Reports Data Collector scheduled job that runs daily.


