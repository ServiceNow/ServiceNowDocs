---
title: Enable Oracle Wallet authentication for discovery
description: Enable Oracle Wallet authentication to use credentials stored on the target server during Oracle database discovery on UNIX systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/enable-oracle-wallet-authentication.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-05-25"
reading_time_minutes: 2
keywords: [Oracle Wallet, Oracle discovery, system property, wallet authentication]
audience: administrator
breadcrumb: [Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Enable Oracle Wallet authentication for discovery

Enable Oracle Wallet authentication to use credentials stored on the target server during Oracle database discovery on UNIX systems.

## Before you begin

-   Verify that the configured Discovery user can connect via SSH to the host.
-   Configure Oracle Wallet on the target server for the Discovery user. For more information, see [Using Oracle Wallet authentication for Oracle Discovery on Unix/Linux \[KB3059862\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3059862).
-   Verify that the following applications are up to date:
    -   Visibility Content starting with version 6.32.0
    -   Discovery and Service Mapping Patterns starting with version 1.31.0
    -   For Oracle GLAS discovery: Data Collection for Oracle Global Licensing and Advisory Services starting with version 1.12.0

Role required: discovery\_admin

## About this task

Oracle Wallet stores database credentials directly on the target server. When the **glide.discovery.oracle\_wallet\_authentication** property is set to true, discovery reads credentials from Oracle Wallet instead of from applicative credentials stored on the instance. The property is set to false by default.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the **Name** column, search for `glide.discovery.oracle_wallet_authentication`.

3.  Select the **glide.discovery.oracle\_wallet\_authentication** system property.

4.  In the **Value** field, enter `true`.

    To switch back to applicative credentials, set the value to `false`.

5.  Select **Update**.


## What to do next

To apply the changes, run discovery.

**Parent Topic:**[Discovery patterns used by ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/c_MappingPatternsCustomization.md)

**Previous topic:**[Configure Server CI creation during cloud discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/configure-server-ci-cloud-disc.md)

**Next topic:**[AI Agent Topology Mapping reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/ai-agent-topology-mapping-reference.md)

**Related topics**  


[Oracle database discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/c_OracleDatabaseDiscovery.md)

[Oracle pluggable database and container database discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/oracle-cdb-pdb-discovery.md)

[Oracle GLAS data collection using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/oracle-glas-discovery.md)

