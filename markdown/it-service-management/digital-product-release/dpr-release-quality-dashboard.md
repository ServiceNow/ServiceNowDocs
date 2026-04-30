---
title: Release Quality dashboard
description: The Release Quality dashboard provides insights into the quality of a release based on the software quality scan summaries and test summaries.
locale: en-US
release: zurich
product: Digital Product Release
classification: digital-product-release
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Release dashboards, Explore, Digital Product Release, IT Service Management]
---

# Release Quality dashboard

The Release Quality dashboard provides insights into the quality of a release based on the software quality scan summaries and test summaries.

**Note:** The Release Quality dashboard is available only for the product releases.

The software quality scan summaries give an overview of the code, highlighting any potential bugs or vulnerabilities that might impact the release. The test summaries provide a comprehensive view of the testing process, including the number of tests executed, passed, and failed.

## Configuration required for tracking release quality

The data displayed on the **Quality** tab is pulled from the pipeline execution, task execution, and their associated test summaries and software quality summaries. You must configure pipelines through the external tools configuration before you can see the metrics from various data sources on the Release Quality dashboard.

For more information, see [Integrate external tools from Digital Product Release Workspace](../task/dpr-integrate-external-tool.md).

## Access the Release Quality dashboard

To open the Release Quality dashboard, navigate to **Workspaces** &gt; **Digital Product Release Workspace**. Select the releases icon \(![Releases icon.](../image/dpr-icon-release.png)\) and then select a release from the Releases list. Select the **Quality** tab on the release record.

**Note:** The **Quality** tab only appears for ongoing releases.

![Animated gif showing Build, Artifact, and Package tabs on the Release Quality dashboard.](../image/dpr-quality-dashboard.gif "Build, Artifact, and Package tabs on the Release Quality dashboard")

## Data in Quality metrics

The data on the Quality dashboard is organized into two sections to summarize the software code quality and test results. You can filter the quality and test results using the following options:

-   **Build**: This option shows all pipelines for the product associated with the release from the sn\_devops\_pipeline table.

    The **Build summary** list includes build numbers that represent pipeline executions from the sn\_devops\_pipeline\_execution\_list table.

    For an active release, **Build summary** shows all the pipeline executions of the selected pipeline within the past 30 days. For a completed release, **Build summary** shows pipeline executions up to 30 days before the actual end date of the release.

-   **Artifact**: This option shows all the artifacts data from the sn\_devops\_artifact table.

    The **Artifact version** list shows all the artifact versions generated within the past 30 days for the artifact. If the artifact's **Use latest version** option is selected, the semantic versions are listed. For more information on the artifact version, see [Manage artifacts in a release](../task/dpr-work-release-artifact.md).

-   **Package**: This option shows all the artifact versions associated with the latest package. The artifact version data comes from the sn\_devops\_m2m\_artifact\_version\_package table and the package data comes from the sn\_devops\_package table. However, if a package is marked as a release candidate, that package is used even if it's not the latest.

**Note:** The Artifact and Package options appear only when the release has an artifact and package associated with it.

-   **Quality summary section**

    The Quality summary section shows you a summary of the scans that are run on the pipelines. The source of data on these widgets is the Software Quality Scan Summary related to Task Execution. This section contains the following metrics:

<table id="table_jdf_b3v_1bc"><thead><tr><th>

Widget

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Vulnerabilities

</td><td>

Total number of security vulnerabilities for the selected build.This data comes from the **Vulnerabilities** category in the Software Quality Scan Details.

Use the **VulnerabilitiesTypeMapping** system property to normalize each type of vulnerability, mapping the custom values with the standard values. For more information, see [Digital Product Release properties](../reference/digital-product-release-properties.md#prop_vulnerabilities).

</td></tr><tr><td>

Overall coverage

</td><td>

Percentage of code covered by your test cases.This data comes from the **Coverage \(%\)** category in the Software Quality Scan Details.

If there are multiple software quality summary results, then the percentage isn’t available.

Total number of lines of code and lines covered for all software quality summary results is shown on this widget.

</td></tr><tr><td>

Bug count

</td><td>

Total number of bugs and average ratings of reliability and maintainability data for all the software quality summary results.This data comes from the **Bugs** category in the Software Quality Scan Details.

</td></tr><tr><td>

Code smells

</td><td>

Total number of code smells and total number of technical debts and duplications for all the software quality summary results.This data comes from the **Code Smells** category in the Software Quality Scan Details.

</td></tr></tbody>
</table>-   **Test summary section**

    The Test summary section shows you a summary of the test run results. The source of data on these widgets is the Test Summary related to Task Execution. The section contains the following metrics:

    |Widget|Description|
    |------|-----------|
    |Unit tests|Total number of unit tests run across all task executions in a pipeline execution, including number of tests passed, failed, skipped, and blocked.|
    |Functional tests|Total number of functional tests run across all task executions in a pipeline execution, including number of tests passed, failed, skipped, and blocked.|
    |Performance tests|Total number of performance tests run across all task executions in a pipeline execution, including number of tests passed, failed, skipped, and blocked.|


**Parent Topic:**[Digital Product Release dashboards](dpr-dashboard-release.md)

**Related topics**  


[Release Overview dashboard](dpr-release-overview-dashboard.md)

[Release dashboard for a multi-product release](dpr-release-dashboard-multi.md)

[Release Overview dashboard for a multi-product release](dpr-release-overview-dashboard-multi.md)

[Quality metrics dashboard](../../enterprise-dev-ops/concept/devops-insights-dboard-ws.md#)

