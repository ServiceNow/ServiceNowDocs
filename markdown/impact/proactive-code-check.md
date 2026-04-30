---
title: Impact Proactive Code Check
description: Developers scan update sets for leading practice violations in non-production instances before promoting to production and Platform Owners gain insight into technical debt and stability of both non-production and production instances, resulting in improved code quality, reduced errors, and compliance verification.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-02-25"
reading_time_minutes: 2
breadcrumb: [Impact Platform Health, Using Impact Store Application, Impact Store Application, Impact]
---

# Impact Proactive Code Check

Developers scan update sets for leading practice violations in non-production instances before promoting to production and Platform Owners gain insight into technical debt and stability of both non-production and production instances, resulting in improved code quality, reduced errors, and compliance verification.

## Proactive Code Check key features

**Important:** Proactive Code Check single instance scanning is supported with the ServiceNow Washington DC release and later. Synchronizing between instances and viewing results on the dashboard are features supported with the ServiceNow Yokohama release and later.

Proactive Code Check can be activated to perform a code review in your instances.

-   **Update set scanning**
    -   Scans code and configuration changes against predefined ServiceNow leading practices and compliance standards for the specific update set.
    -   Detects security vulnerabilities, performance issues, and coding inefficiencies early in the development lifecycle.
    -   Improve code quality, reduce errors, and verify compliance before promoting to production.
-   **Real-time feedback**
    -   Provides actionable insights and recommendations for resolving identified issues.
    -   Delivers results in real time, enabling developers to address problems without delays.
-   **Instance-specific integration**
    -   Scans run directly within your instance, ensuring data security and compliance.
    -   Findings are saved locally for easy access and reporting.
-   **Comprehensive reporting**
    -   Findings are categorized by priority, allowing users to focus on critical issues.
    -   Reports include trend analysis and delta comparisons to track improvement over time.
    -   Gain insight into technical debt and the stability of instances to easily monitor the status of issue remediation efforts using performance reports
-   **Synchronize scan results to production**

    Code review reports on update sets in non-production instances can be synced for review in a configured production instance

    View scan results on the Platform Health dashboard


## Proactive Code Check scan categories

Proactive Code Check performs leading practice checks related to the categories in the following table.

|Category|Description|
|--------|-----------|
|Manageability|Measures the extent to which ServiceNow instances, applications, or infrastructure can be effectively upgraded, monitored, and maintained.|
|Performance|Measures the efficiency of a ServiceNow instance, encompassing aspects such as speed, responsiveness, resource utilization, and overall dependability.|
|Security|Measures implementation of protocols across a ServiceNow instance to prevent unauthorized access, data breaches, cyber attacks, and potential vulnerabilities.|
|Upgradeability|Assesses the ease of enhancing a ServiceNow instance or application with new features, improvements, security patches, or compatibility adjustments.|

**Note:** For the complete list checks performed by a Proactive Code Check scan, see [Proactive Code Check scan suite matrix](proactive-code-check-scan-suite.md).

-   **[Use Proactive Code Check scanning](install-proactive-code-check.md)**  
Developers can identify issues and prevent defects before they are deployed to production.
-   **[Proactive Code Check analytics](review-address-proactive-code-check-findings.md)**  
Platform Owners use Proactive Code Check to track compliance against coding best practices and organizational standards. Owners can review detailed findings and audit the status of issues that were uncovered during the scan. Historical data is available up to six months.
-   **[Proactive Code Check scan suite matrix](proactive-code-check-scan-suite.md)**  
Refer to the Proactive Code Check \(PCC\) scan suite matrix for details on the checks performed during a PCC scan.

**Parent Topic:**[Impact Platform Health](impact-healthscan-store-app.md)

