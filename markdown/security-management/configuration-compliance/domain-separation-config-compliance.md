---
title: Domain separation and Configuration Compliance
description: Domain separation is supported in Configuration Compliance. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Reference, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Domain separation and Configuration Compliance

Domain separation is supported in Configuration Compliance. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## How domain separation works in Configuration Compliance

With domain separation you can standardize \(Configuration Compliance\) procedures, across the customer base you serve, with lowered operational costs and a higher quality of service.

Separate customer work spaces for workflows, dashboards, reports, and so on, ensures that customer data is separated and never exposed to other clients.

|Release|Support level|Notes|
|-------|-------------|-----|
|Orlando|Standard| |
|Paris|Standard| |
|Quebec|Standard| |
|Rome|Standard| |
|San Diego|Standard| |
|Tokyo|Standard| |
|Utah|Standard| |
|Vancouver|Standard| |

Domain separation for the Configuration Compliance application covers the following product functionality:

-   Ingests the test results from third-party scanners \(Qualys\) in the correct domain.

    The data ingests in the same domain as that of the integration user, whose credentials are used for integration.

-   Re-scans specific hosts from Configuration Compliance in the domain from which it was requested.
-   Uses the CMDB CI lookup process to ensure that the CI information from the scanners matches the CIs in CMDB of the integration user’s domain.
-   Calculates risk scores at the test result level as per the risk score calculator defined in the same domain as that of the integration user.
-   Remediation Task rule\(s\) can be defined, assigned, and stay in, the same domain as the domain of the integration user.
-   Remediation tasks created using the doc remediation task rules stay in the same domain as where the remediation task rules are created.
-   Deferral workflow goes through the approval process in the same domain for which the deferral is requested.
-   Reports and dashboards display the test result states such as age of test results, open test results by CI, test results by impact in the domain to which it belongs.
-   Knowledge from third-party scanners \(Qualys\) can be ingested in the global domain and data can be shared across multiple clients.

**Note:** In all the above cases the overarching principles of visibility in separated domains separation in the NOW Platform apply.

## Use cases

The Configuration Compliance application manages the life cycle of a test result end to end. The following use cases are domain-separation aware:

-   **Ingest** test results from Qualys
    -   Ingest data from multiple instances
    -   De-duplicate the test results
    -   Match up with CMDB CI
-   **Enrichment** of test results with risk scores
    -   Asset enrichment \(CMDB\)
    -   Risk score
-   **Group** test results and assign the remediation task
    -   Automatically group the test results
    -   Automatically assign the remediation task
-   **Remediate**
    -   Remediation task assigned as a remediation task
    -   Comprehensive remediation life cycle
    -   Deferral workflow
-   **Measure** the security posture of the organization and compliance management program
    -   Results trend, by compliance, category, criticality and technology
    -   Status and distribution on policies, tests, hosts, test results, and risk score

## Setup

Setting up domain separation for Configuration Compliance does not require any additional steps. All Configuration Compliance tables acquire the Domain column after the instance is domain separated. You can direct test result integration import data to specific domains. For more information, see [Create domain-separated imports for an integration](../../vulnerability-response/task/create-domain-separated-imports.md). For more information on additional precautions and settings, see [Additional settings for domain separation](../../vulnerability-response/reference/ds-additional-config.md).

## Domain-separated data

Data can be domain separated, which means:

-   Test results ingested from third-party scanners stays in the same domain as the domain of the integration user, and is not accessible from any other domain.
-   Test results or hosts in one domain cannot be viewed from other domains.
-   The risk scoring algorithm and the test results group rules cannot be viewed by anyone outside the domain.
-   Deferral workflows created in one domain are not visible in another domain.
-   All email notifications are contained within the domain they belong to.

## How compliance analysts manage their own application data

-   Analysts create their own application installation, multi-source application management, and CI lookup rules.
-   Analysts can configure specific integrations exclusively for use within the domain.
-   Analysts can create their own deferral and change management workflows.
-   Analysts can create their own remediation task rules, risk-scoring logic to accurately prioritize results, auto-assign remediation tasks and assign to the correct assignment group.
-   Domain users create a manual remediation task and then close it.

## Business logic and processes that can be domain-separated by instance owner

-   Configuration Compliance users and groups
-   Configuration Compliance integrations \(starting with the Madrid release\)
-   Complete setup configuration \(user and group management, application installation, multi-source application management, CI lookup rules, remediation task rules, risk calculators, etc.\)
-   Complete remediation life cycle including deferral

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

