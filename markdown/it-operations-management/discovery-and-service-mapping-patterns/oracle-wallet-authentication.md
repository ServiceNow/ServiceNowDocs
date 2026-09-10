---
title: Oracle Wallet authentication for database discovery
description: With Oracle Wallet authentication, Discovery reads database credentials directly from the target server. This approach keeps credentials within the target environment instead of storing them on the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/oracle-wallet-authentication.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2026-08-26"
reading_time_minutes: 2
keywords: [Oracle Wallet, Oracle Database discovery, Discovery credentials]
breadcrumb: [Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Oracle Wallet authentication for database discovery

With Oracle Wallet authentication, Discovery reads database credentials directly from the target server. This approach keeps credentials within the target environment instead of storing them on the ServiceNow AI Platform.

## How Oracle Wallet authentication works

Oracle database discovery uses SQL queries that require database credentials to authenticate against the target Oracle instance. By default, Discovery uses applicative credentials, which uses a database username and password stored on the ServiceNow AI Platform. Oracle Wallet authentication is supported on UNIX and Windows as an alternative to applicative credentials.

Oracle Wallet stores credentials in a wallet on the target server. Discovery reads credentials from the wallet at runtime rather than passing them from the ServiceNow AI Platform. Credentials remain in the target environment and are managed through the native Oracle mechanism.

|OS|Minimum Visibility Content version|Minimum Discovery and Service Mapping Patterns version|Minimum Data Collection for Oracle Global Licensing and Advisory Services version|
|---|----------------------------------|------------------------------------------------------|---------------------------------------------------------------------------------|
|UNIX|6.32.0|1.31.0|1.12.0|
|Windows|6.35.0|1.35.0|1.13.0|

For information on enabling Oracle Wallet authentication, see [Enable Oracle Wallet authentication for discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/enable-oracle-wallet-authentication.md).

## Supported discovery types

Oracle Wallet authentication is supported for the following Oracle database discovery types:

-   Standard Oracle database discovery. For more information, see [Oracle database discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/c_OracleDatabaseDiscovery.md).
-   Container and pluggable database \(CDB/PDB\) discovery. For more information, see [Oracle pluggable database and container database discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/oracle-cdb-pdb-discovery.md).
-   Oracle Global Licensing and Advisory Services \(GLAS\) discovery. For more information, see [Oracle GLAS data collection using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/oracle-glas-discovery.md).

-   **[Enable Oracle Wallet authentication for discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/enable-oracle-wallet-authentication.md)**  
Enable Oracle Wallet authentication to use credentials stored on the target server during Oracle database discovery.

**Parent Topic:**[Discovery patterns used by ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/c_MappingPatternsCustomization.md)

**Previous topic:**[Configure Server CI creation during cloud discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/configure-server-ci-cloud-disc.md)

**Next topic:**[Enable Oracle Wallet authentication for discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/enable-oracle-wallet-authentication.md)

