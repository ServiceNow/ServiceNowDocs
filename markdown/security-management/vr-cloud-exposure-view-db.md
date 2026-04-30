---
title: Viewing the Cloud Exposure View dashboard
description: The Cloud Exposure View is a module that is supported by Security Exposure Management workspace. Select interactive visualizations and filter aggregated data for your cloud assets by category to view findings for your security exposures. Cloud security teams can monitor and act on all their cloud-related security findings from multiple vendors across their cloud environments from within the workspace.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-12-03"
reading_time_minutes: 4
breadcrumb: [Security Exposure Management Workspace, Explore, Unified Security Exposure Management, Security Operations]
---

# Viewing the Cloud Exposure View dashboard

The Cloud Exposure View is a module that is supported by Security Exposure Management workspace. Select interactive visualizations and filter aggregated data for your cloud assets by category to view findings for your security exposures. Cloud security teams can monitor and act on all their cloud-related security findings from multiple vendors across their cloud environments from within the workspace.

## Locating the Cloud Exposure View

To view the dashboard, navigate to **Workspaces** &gt; **Security Exposure Management** &gt; **Cloud Exposure View**.

Roles required:

-   sn\_sec\_exception.read to view the workspace
-   sn\_vul\_cmn.usem\_admin to configure workspace rules
-   For vulnerability findings remediation by product:

See [Security Exposure Management Workspace Roles](../../security-exposure-management-workspace/reference/sem-new-roles-installed.md)

## Top-level filters

Locate and organize findings based on the following top-level filters to help you focus your search:

-   **Finding type** - View security exposure findings for your cloud service accounts, cloud regions, and cloud resources with this filter.

    **Note:** Finding types are listed by product. You must install the corresponding applications before you can view the imported data for the following finding types:

    -   **Host**Vulnerability Response supports findings for vulnerabilities in virtual machines and servers.
    -   **Misconfiguration** Configuration Compliance supports findings for misconfigurations in cloud resource services such as S3 and EC2. Configuration Compliance also supports findings for `Issues`, such as assets that are involved in toxic combinations of vulnerabilities and misconfigurations.
    -   **Container** - Container Vulnerability Response supports container vulnerability findings.
-   **Source** - View security exposures organized by the third-party scanner product integrations you have installed in your instance.
-   **Risk rating** - View security exposures by their criticality \(Critical, High, or Medium\). Multi-select is supported.

    **Note:** Select the Settings ![Gear icon that opens configuration options.](../../vulnerability-response/image/vr-gear-icon.png) \(gear icon\). With **Filters** selected you can include findings with **Low** criticality and no imported criticality \(**None**\). You might prefer to keep the criticality in its default setting to limit your import and help you focus on your most important findings. If you modify this filter, findings that match your settings are imported with the next daily data import for all your finding types.


## Needs attention

Select the totals on the cards to open a list in a new browser tab. View your most critical records organized by the applications that you have installed for the following categories.

-   Unassigned findings
-   Overdue findings
-   Remediation due in 14 days
-   Findings in review
-   Select the total numbers in the cards to view a list of records.

Select a card and then select the filters on the new tabs that are displayed to view lists of findings by product: **Host**, **Misconfiguration**, and **Container**.

## Cloud Security Overview

-   View breakdowns of totals of active findings across cloud resource types that are categorized by provider and severity for the following assets:
    -   Compute
    -   Network
    -   Storage
    -   Other - Resources that don't fall under the other categories.
    -   Select the total numbers in the cards, a provider icon, or the data visualizations to view corresponding lists of records that display total findings for each asset.
-   Select **Base images** or **Other image types** to view the five findings that have the most security exposures \(Top\) for the following categories:

    -   Top base images with active findings
    -   Top base images by risk
    -   Select the total number in the card.
    Container findings are color-coded for Critical, High, and Medium:

    -   Red
    -   Orange
    -   Yellow
    Select a data visualization graph or a colored pill to view a list of up to 1,000 records.

-   Select **Accounts** or **Regions** to view the top five findings that have the most security exposures.

    Findings are grouped by Host, Misconfigurations \(Test results\), Toxic combinations \(Issues\), and Container \(Container vulnerabilities\) and are color-coded for Critical, High, and Medium:

    -   Red
    -   Orange
    -   Yellow
    View records for your least compliant accounts under **Non compliant framework**. If no data is imported, this column remains unpopulated.

    Select a colored pill or **View more** to view a list of up to 1,000 records.

-   Select from **Resources** or **Resources - Externally Exposed** to view the top five findings that have the most critical security exposures.

    Findings are grouped by Misconfiguration \(Test results\) and Toxic combinations \(Issues\), are and Container findings and are color-coded for Critical, High, and Medium:

    -   Red
    -   Orange
    -   Yellow
-   View toxic combinations and assets with the least compliant scores that have the most security exposures due to failed configurations. Both misconfigurations and issues are populated on test results in Configuration Compliance. This data is imported by the [Understanding the Wiz Vulnerability Response Integration](../../secops-integration-vr/wiz-host-vuln-integration/concept/vr-wiz-exploring-host-cf.md), and this data is not displayed unless Configuration Compliance and the Wiz Vulnerability Response Integration are installed.

    Findings with failed test results are color-coded. You can select the date range for the last 7 days or the last 30 days.

    -   Red
    -   Orange
    -   Yellow
    Select **View more** to view a list of up to 1,000 records.


