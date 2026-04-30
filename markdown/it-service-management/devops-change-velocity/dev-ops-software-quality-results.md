---
title: Software Quality Results
description: Software Quality Results display scan details from SonarQube scans configured on your GitHub Actions, Jenkins, Azure DevOps, or Harness pipelines.Software Quality Summaries shows you a summary of the scans that are run on the pipelines with SonarQube scans on the DevOps app on your ServiceNow AI Platform instance.The Software Quality Scan Details related list \(for each Scan ID\) displays software quality subcategories that you can configure for results of the Vulnerabilities and New Vulnerabilities categories from the scan results.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Reference, DevOps Change Velocity, IT Service Management]
---

# Software Quality Results

Software Quality Results display scan details from SonarQube scans configured on your GitHub Actions, Jenkins, Azure DevOps, or Harness pipelines.

## Software Quality Results

You can configure SonarQube scan results from your GitHub Actions, Jenkins, Azure DevOps, and Harness pipelines to be fetched into ServiceNow DevOps. SonarQube notifications create inbound events which are then processed by base system subflows associated with all inbound events with Software Quality capability.

After you have configured SonarQube scans on your pipelines and configured the corresponding plugins, run the pipelines to fetch software quality scan results into ServiceNow DevOps. You can view the scan results by Scan ID for each SonarQube scan that was part of your build or release pipeline execution steps.

**Note:** For Harness pipelines, you can configure SonarQube scans only through the generic Docker Container Image. For more information, [Implement custom actions for pipelines using generic Docker container image](servicenow-custom-actions-for-gitlab.md). For GitHub Actions, Jenkins, and Azure DevOps, you can either use the corresponding plugins from the marketplace or the Docker container image.

**Parent Topic:**[DevOps Change Velocity reference](../reference/devops-change-velocity-reference.md)

## Software Quality Summaries

Software Quality Summaries shows you a summary of the scans that are run on the pipelines with SonarQube scans on the DevOps app on your ServiceNow AI Platform instance.

### Software Quality Summaries

1.  Navigate to **Software Quality Results** &gt; **Software Quality Summaries**.
2.  Click a **Scan ID** record to view scan details.

    The following Software Quality Scan Summary Details appear for the Scan ID.

    |Field|Value|
    |-----|-----|
    |Number|The Scan record number in the CMDB.|
    |Initiated By|The user who initiated the scan|
    |Scan ID|The unique Scan ID|
    |Project Name|The SonarQube project name or key.|
    |Last Scanned|Date Time stamp of the last scan|
    |Scan URL|The SonarQube project URL you configured in the extension task.|
    |Scanner name|The code quality scanner tool name.|
    |Domain|The domain name in which the scans are configured in the instance.|
    |Tool|The name of the SonarQube tool you created.|

    **Note:** The scanID, lastScannedBy, and initiatedBy details are not retrieved when you onboard Sonar using a non-admin user.


The Software Quality Scan Details related list \(for each Scan ID\) displays for the following categories with a corresponding value signifying the count value against the scan result category.

Software Quality categories for Overall Code metrics:

-   Coverage
-   Bugs
-   Reliability
-   Rating
-   Code
-   Smells
-   Duplications
-   Security Rating
-   Lines of Code
-   Vulnerabilities
-   Security hotspots
-   Maintainability rating

Software Quality categories for New Code metrics:

-   Duplications
-   New Duplications
-   Vulnerabilities
-   New Vulnerabilities
-   Technical Debt
-   New Technical Debt
-   Maintainability rating
-   New Maintainability rating
-   Bugs
-   New Bugs
-   Lines to Cover
-   New Lines to Cover
-   Lines of Code
-   New Lines of Code
-   Coverage
-   New Coverage
-   Reliability Rating
-   New Reliability Rating
-   Code Smells
-   New Code Smells
-   Security Rating
-   New Security Rating
-   Security Review
-   New Security Review
-   Security Hotspots
-   New Security Hotspots

## Software Quality subcategories

The Software Quality Scan Details related list \(for each Scan ID\) displays software quality subcategories that you can configure for results of the **Vulnerabilities** and **New Vulnerabilities** categories from the scan results.

### Software Quality subcategories- Vulnerabilities and New Vulnerabilities

Use seeded subcategories or create new categories to prioritize and list your scan results of category type- Vulnerabilities and New Vulnerabilities.

1.  Navigate to **DevOps** &gt; **Integrations** &gt; **Software Quality Sub Categories**.

    The Software Quality Sub Categories form displays with the following base-system subcategories:

    -   Blocker
    -   Critical
    -   Major
    -   Minor
    -   Info
    ![Software Quality Sub Category](../image/software-quality-sub-categories.png)

2.  Click the **New** button to create custom sub categories.
3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Label|A unique label for the sub category.|
    |Domain|The domain in which the DevOps app is running.|
    |Name|A unique name for the sub category.|
    |Category|Select a category from the seeded base-system categories from the lookup list.|

4.  Click **Submit**.

    You have successfully created a custom sub category.


To view the Software Quality Scan Detail and the Software Quality Category Details related list &gt; Sub category, follow these steps:

-   View scan details as part of Task Executions. View details of all the Sonar scans that are part of the task execution mapped to a build or release pipeline execution step.

    1.  Navigate to **DevOps** &gt; **Orchestrate** &gt; **Task Execution** click a relevant Task Execution record.
    2.  Click the Software Quality Summary related list.
    3.  Click a relevant Scan ID record.
    The Software Quality Scan Summary and Scan Details are displayed.

-   View scan details as part of Change Request. View all the scans that were part of this build/release pipeline in the **Software Quality Results** &gt; **Software Quality Summary** related list.

    1.  Navigate to **DevOps** &gt; **Orchestrate** &gt; **Pipeline Change Requests**
    2.  Click the Software Quality Summary related list.
    3.  Click a relevant Scan ID record.
    The Software Quality Scan Summary and Scan Details are displayed.


