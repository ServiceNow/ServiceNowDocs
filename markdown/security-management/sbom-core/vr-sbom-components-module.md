---
title: Reviewing the Components module in the Software Bill of Materials Workspace
description: The Components module in the Software Bill of Materials \(SBOM\) Workspace displays current information about vulnerable, stale, abandoned, and high-risk combinations for the components you import.
locale: en-US
release: australia
product: SBOM Core
classification: sbom-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Viewing reports and dashboards in the Software Bill of Materials workspace, Use, Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# Reviewing the Components module in the Software Bill of Materials Workspace

The Components module in the Software Bill of Materials \(SBOM\) Workspace displays current information about vulnerable, stale, abandoned, and high-risk combinations for the components you import.

## Viewing the Components module

Role required: sn\_sbom\_resp.sbom\_analyst

Navigate to **Workspaces** &gt; **SBOM Workspace** &gt; **Components**.

What you can see in the module depends on the applications you have installed.

Imported data is not calculated and populated by live queries. Scores on the Home and Components pages are updated once daily with performance enhancements for reporting. This enhancement might provide you with faster load times for the scorecards on the Home and Components modules in the SBOM Workspace.

These enhancements have no impact on how or where data is stored.

<table><thead><tr><th>

Installed application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

If you have installed SBOM Core

</td><td>

An inventory of all uploaded components that includes the following information:-   Name
-   Description
-   Version
-   BOM entity count

</td></tr><tr><td>

If you have installed SBOM Response

</td><td>

Select a graph or a number on the graph to view a list of associated records.-   **All Components**

The list of **Stale** and **Abandoned** components, as well as those with at least one vulnerability in your total component count. These counts can help you identify components that require your attention. These subsets of components might not match your total component count because all of your components might not fit into these categories.

    -   A stale component's version is more than two major versions behind the latest version and two years behind the latest version.
    -   An abandoned component has not been updated for more than two years.
    -   Vulnerable components are components that have any vulnerabilities with a severity of **High** or greater.
-   **High-risk combinations**

High-risk components might require your immediate attention. The Deps.dev integration, which is installed when you install the SBOM Response application, provides the packages intelligence for components in the **Stale** and **Abandoned** states.

Imported, high-risk combinations are comprised of stale and abandoned components with at least one severe \(**Critical** or **High**\) vulnerability that you can fix with updates, replacement, or another type of repair. The **Completely fixable** status means that a component has an available version that can fix it. The percentage of the total number of high-risk components that have fixable versions is noted.

-   **Fixibility of vulnerable components**

Totals and breakdowns of the components with **Critical**, **High**, **Medium**, and **Low** vulnerabilities and if some or all of their vulnerabilities can be fixed. If a component has more than one vulnerability, the most critical vulnerability takes precedence.

The fixability status:

    -   Complete - There are fix versions for all the vulnerabilities associated with the current version of the component.
    -   Partial - There is a fix version for at least one but not all of the vulnerabilities associated with the current version of the component.
-   **License classification of components**

Totals and breakdowns of components by their license classifications.


The Component List under the visualizations enables you to see the name, description, version, and entity counts. In the right panel, you can view a version history. The current version is highlighted in the version history. The Common Vulnerabilities and Exposure \(**CVE**\) and **Fixability** columns are also displayed.

</td></tr></tbody>
</table>## Assessing your risk with vulnerability intelligence

See [Checking a Software Bill of Materials entity for vulnerabilities](../task/vr-sbom-check-vulnerability-use-case.md) for more information about how to review vulnerability intelligence data in the workspace.

## Assessing your risk with license compliance

See [Classifying licenses and resolving component licenses in the Software Bill of Materials workspace](vr-sbom-license-overview.md) for more information about how to license data your import with your components and viewing your over-all license compliance in the workspace.

