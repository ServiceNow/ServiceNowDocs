---
title: Configuration Compliance reference information
description: Several types of components are installed with activation of the Configuration Compliance application, including tables, scheduled jobs, and user roles.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configuration Compliance reference information

Several types of components are installed with activation of the Configuration Compliance application, including tables, scheduled jobs, and user roles.

The following topics provide you with reference information, troubleshooting, in addition to field data on the forms and records found in Configuration Compliance.

-   [Components installed with Configuration Compliance](installed-with-config-compliance.md)
-   [Test Results fields](test-results-fields.md)
-   [Resolving Configuration Compliance import issues](../concept/vuln-config-compl-troubleshooting.md)
-   [Modify Qualys PC Results start date](../task/modify-test-results-startdate.md)

-   **[View Configuration Compliance test groups](../task/view-vuln-config-compl-policies.md)**  
Once you have imported the results of a third-party scan into your instance, you can see your test compliance at the test group level. Use this view before an audit of that test group and any associated test records.
-   **[View Configuration Compliance authoritative sources](../task/view-vuln-config-compl-auth-sources.md)**  
Use this module to view summary information about each authoritative source and to research the source publications that were used to create the record.
-   **[View Configuration Compliance technologies](../task/view-vlun-config-compl-technologies.md)**  
Use this module to view summary information about each authoritative sources and citation \(also known, in Qualys, as a framework\). You can research the source publications that were used to create the record.
-   **[View Configuration Compliance tests](../task/view-vuln-config-compl-tests.md)**  
Use this module to research detailed information about these tests. Included are the expert source citations that were used when creating them, the third-party configuration policies in which they are used, and the results obtained from the scan.
-   **[View Configuration Compliance test results](../task/view-vuln-config-compl-test-results.md)**  
View Configuration Compliance test results for auditing and remediation. The test results are automatically created during third-party vulnerability integration imports.
-   **[View a remediation task](../task/view-cc-tr-group.md)**  
You can view, or, alternatively, create a remediation task and perform remediation.
-   **[Test result and remediation task state transitions in the Configuration Compliance application](../concept/cc-state-transition.md)**  
The states of configuration test records and their associated remediation tasks \(RTs\) are impacted if test result records are deferred, resolved, reopened, and transferred to other remediation efforts \(REs\).
-   **[State synchronization between change requests and remediation tasks](../task/cc-cr-state-synch.md)**  
There is a synchronized relationship between the State fields of remediation tasks and the State fields of change requests \(CHGs\) in the Configuration Compliance application.
-   **[Domain separation and Configuration Compliance](../concept/domain-separation-config-compliance.md)**  
Domain separation is supported in Configuration Compliance. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Test Results fields](test-results-fields.md)**  
Test results are automatically created during third-part vulnerability integration imports.
-   **[Configuration Compliance criticality maps](../concept/vuln-config-compl-critmaps.md)**  
Configuration Compliance criticality mapping transforms criticality fields from the source to fields in Configuration Compliance.
-   **[Configuration Compliance states](../concept/vuln-config-compl-states.md)**  
With Configuration Compliance, you can see a state model to learn what the status of the remediation task is at any given time. The remediation task states control the test result states by precedence.
-   **[Resolving Configuration Compliance import issues](../concept/vuln-config-compl-troubleshooting.md)**  
Resolve issues with third-party integration import.
-   **[CI lookup rules for Microsoft Defender for Cloud Integration for Security Operations and Palo Alto Prisma Cloud](cloud-ci-look-up-for-ms-paloalto.md)**  
You can use the configuration item \(CI\) lookup rules for the Microsoft Defender for Cloud Integration and Palo Alto Prisma Cloud integrations to find a correct match to commonly used resource types in the Configuration Management Database \(CMDB\).

**Parent Topic:**[Configuration Compliance](vr-config-compliance-landing.md)

