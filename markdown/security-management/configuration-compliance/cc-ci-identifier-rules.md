---
title: CI Lookup Rules for identifying configuration items from Configuration Compliance third-party vulnerability integrations
description: When data is imported from a third-party integration, Configuration Compliance automatically uses host data to search for matches in the Configuration Management Database \(CMDB\). It does this using CI Lookup Rules. These rules are used to identify configuration items \(CIs\) and add them to the test result record to aid in remediation.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2026-04-03"
reading_time_minutes: 4
breadcrumb: [Explore, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# CI Lookup Rules for identifying configuration items from Configuration Compliance third-party vulnerability integrations

When data is imported from a third-party integration, Configuration Compliance automatically uses host data to search for matches in the Configuration Management Database \(CMDB\). It does this using **CI Lookup Rules**. These rules are used to identify configuration items \(CIs\) and add them to the test result record to aid in remediation.

As assets are imported, a lookup is performed first on the **Discovered Items** list using third-party IDs to find matches to configuration item \(CIs\) from prior imports. When a host ID match is found, it is used as the **Configuration item** field in the test result record.

You can see how imported assets are mapped to CIs using the **Discovered Items** list. If a match is not found, or the cmdb\_ci field is empty, the rules use the other host information to attempt to correctly identify the CI. If a match is still not found, a placeholder CI is created and is designated as an **Unmatched CI**. See [Discovered Items for Configuration Compliance](../../vulnerability-config-compliance/concept/cc-cj-discovered-items.md) for more information on how those CIs are handled.

A new discovered item is created and mapped to this CI.

**Note:** CI lookup rules are available only for the Qualys Integration for Security Operations.

CI lookup rules can be domain separated and are source-specific. Each source can have multiple deployments. Qualys can have multiple deployments of the Qualys Integration. Each deployment has its own set of CI Lookup Rules.

**Note:** CI lookup rules are shared by all deployments of the vulnerability integration. If a rule is deleted or modified, the deletion or changes affect all deployments of the vulnerability integration.

When attempting a match, the first step is a vendor ID lookup for an exact match across source, source\_instance, and vendor ID. Then, lookup rules are run in order, from lowest to highest and stop when a rule returns just a single CI as a match. If a rule is created in such a way that it returns more than one CI, only the first match is used.

**Note:** To avoid matching on low-level networking elements, if a matched CI is one of `dscy_switchport`, `cmdb_ci_network_adapter`, `cmdb_ci_nic`, or `cmdb_ci_ip_address`, the parent CI is returned.

A system property to exclude CI classes is available. This property is not available with upgrade. See [Ignore CI classes](../task/ignore-CI-classes.md) for upgrade information and instructions on setting the property.

To make it easier to find matching issues, when a match is found, the CI lookup rule used to find it is added to the Discovered Item record in the **CI matching rule** field. Lookup rules are evaluated by lowest **Order** value first.

Some of the Qualys CI lookup rules shipped with the base system are:

-   QUALYS HOST ID
-   FQDN
-   NetBIOS
-   DNS
-   IP

Some of the Microsoft Defender CI lookup rules shipped with the base system are:

-   S3 Bucket
-   Name
-   Resource Id

Some of the Palo Alto Prisma Cloud CI lookup rules shipped with the base system are:

-   S3 Bucket
-   Name
-   Resource Id

Importing test results data can be taxing on an instance and performance issues with resources can occur if rules are not carefully constructed. The logic used to iterate through and perform matching within the CMDB can result in lengthy processing times. To avoid any potential degradation of resources or performance complications, test any custom-written CI Lookup Rules or modifications to pre-defined **CI Lookup Rules**. See [Steps to help prevent duplicate or orphaned records after running Vulnerability Response CI lookup rules](ci-identifier-rules-impl-test.md) for more information on preventing duplicate orphan records, deleting data, and cleaning up data.

## Reapplying updated CI lookup rules

When you change a CI lookup rule, click **Apply Changes** on the CI Lookup Rules list page to rerun all the rules on the discovered items that:

-   Were matched by the updated rules
-   Are not matched by any rule

If the configuration item \(CI\) changes after reapplying the lookup rules, the discovered items are updated with the new CI. The test results are also updated. For more information, see [CI changes for discovered items for Configuration Compliance](../../vulnerability-config-compliance/concept/reapply-discovered-items-ci-changes-cc.md).

