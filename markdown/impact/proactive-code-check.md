---
title: Proactive Code Check for the Impact Store Application
description: Developers scan update sets for leading practice violations in non-production instances before promoting to production and Platform Owners gain insight into technical debt and stability of both non-production and production instances, resulting in improved code quality, reduced errors, and compliance verification.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Platform Health, Using Impact, Impact]
---

# Proactive Code Check for the Impact Store Application

Developers scan update sets for leading practice violations in non-production instances before promoting to production and Platform Owners gain insight into technical debt and stability of both non-production and production instances, resulting in improved code quality, reduced errors, and compliance verification.

## Proactive Code Check key features

**Note:** Starting with Impact Zurich version 6.0.8 ServiceNow Store release, Proactive Code Check is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Proactive Code Check can be used to perform a code review in your instances.

**Important:** Proactive Code Check single instance scanning is supported with the ServiceNow Washington DC release and later. Synchronizing between instances and viewing results on the dashboard are features supported with the ServiceNow Yokohama release and later.

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

**Note:** For the complete list checks performed by a Proactive Code Check scan, see [Proactive Code Check scan suite matrix for the Impact Store Application](proactive-code-check-scan-suite.md).

