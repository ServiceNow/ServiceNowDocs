---
title: Using Telecommunications Service Operations Management
description: Leverage Telecommunications Service Operations Management \(TSOM\) to proactively monitor telecom services, validate data integrity, and reconcile discrepancies across network inventory and discovery sources. TSOM enables operations teams to maintain an accurate telecom-aware CMDB and act on real-time network insights.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Telecommunications Service Operations Management]
---

# Using Telecommunications Service Operations Management

Leverage Telecommunications Service Operations Management \(TSOM\) to proactively monitor telecom services, validate data integrity, and reconcile discrepancies across network inventory and discovery sources. TSOM enables operations teams to maintain an accurate telecom-aware CMDB and act on real-time network insights.

## Common operational tasks of TSOM

Once TSOM is configured, you can use its capabilities to:

-   Run Telecom Discrepancy audits: Identify inconsistencies in network relationships and configurations by running certification audits based on discovered data and reconciliation rules.
-   Validate attribute value mismatches in CMDB 360: Use the Attribute Value Discrepancy feature in CMDB 360 to compare attribute values across different discovery sources and detect conflicts or outdated records.
-   Use Telecom Discovery Patterns: Apply Telecom Discovery Patterns to accurately discover and populate telecom-specific Configuration Items \(CIs\) and their relationships.
-   Run and verify import jobs from service graph connectors: Manually trigger import schedules \(e.g., for the Nokia Altiplano connector\) to verify that topology and device data is successfully imported into the CMDB and mapped to the correct CI classes.

These tasks help ensure that your telecom network is continuously synchronized, accurate, and operationally visible within ServiceNow.

-   **[Use Telecom Discovery patterns](using-telecom-discovery-patterns.md)**  
Use Telecom Discovery patterns to identify and classify network functions \(xNFs\) from vendor devices such as Cisco, Juniper, routers, or switches. Leverage pattern-based discovery to map telecom resources into the CMDB.
-   **[Run and verify import for Nokia Altiplano Service Graph Connector](../task/run-and-verify-import-for-nokia-altiplano-service-graph-connector.md)**  
Manually execute a configured import schedule for the Nokia Altiplano Service Graph Connector. You can also execute the import to validate the connector setup, run ad-hoc imports, or test newly configured connection aliases. This task helps ensure that data from Altiplano is successfully imported or updated in the CMDB.
-   **[Run and verify an import schedule for Fortinet SGC](../task/run-and-verify-import-for-fortinet-sd-wan.md)**  
Manually run a configured import schedule for the Fortinet Service Graph Connector \(SGC\) to verify that data from Fortinet was successfully imported or updated in the Configuration Management Database \(CMDB\). You can also perform the import to validate the connector setup, run one-off imports, or test newly configured connection aliases.
-   **[Run and verify an import schedule for Cisco Meraki SGC](../task/run-and-verify-import-for-cisco-meraki-sd-wan-service-graph-connector.md)**  
Manually run a configured import schedule for the Cisco Meraki Service Graph Connector \(SGC\) to verify that data from Cisco Meraki was successfully imported or updated in the Configuration Management Database \(CMDB\). You can also perform the import to validate the connector setup, run one-off imports, or test newly configured connection aliases.
-   **[Validating JSON payloads using TSOM Schema Validator](validating-json-payloads-using-tsom-schema-validator.md)**  
Use the TsomSchemaValidator utility class to validate JSON payloads against TSOM schemas before importing data. This helps identify errors early, reduce ETL failures, and confirm data quality.
-   **[Run Telecom Discrepancy audit](../task/run-audits.md#)**  
The Telecom Discrepancy Audit validates the integrity of configuration items \(CIs\) and relationships across your telecom inventory using the CMDB Compliance framework.
-   **[Generate reports for attribute value discrepancies](../task/use-attribute-value-discrepancy-in-cmdb-360.md)**  
Use CMDB 360 to generate reports that highlight discrepancies in attribute values between different discovery sources or between a discovery source and the CMDB baseline.

