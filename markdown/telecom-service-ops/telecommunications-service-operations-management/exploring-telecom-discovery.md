---
title: Telecom Discovery
description: ServiceNow AI Platform Telecom Discovery provides visibility into your telecom network infrastructure by extending ITOM Visibility to support telecom-specific use cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/exploring-telecom-discovery.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Telecom Visibility, Explore, Telecommunications Service Operations Management]
---

# Telecom Discovery

ServiceNow AI Platform Telecom Discovery provides visibility into your telecom network infrastructure by extending ITOM Visibility to support telecom-specific use cases.

Built for communication service providers \(CSPs\), this solution enables the discovery and mapping of network elements across multi-vendor environments using standardized protocols and integration with network management systems.

By combining Telecom Discovery plugins with the power of Service Graph Connectors and Discovery Patterns, you can automatically populate and maintain accurate records of your telecom resources in the Configuration Management Database \(CMDB\), providing a unified view of both IT and network infrastructure.

With Telecom Discovery, you can:

-   Discover physical and logical telecom network resources across domains and vendors.
-   Integrate with Element Management Systems \(EMS\), Network Management Systems \(NMS\), and software-defined networking \(SDN\) controllers.
-   Automatically populate and update CMDB and TNI records based on real-time network data.
-   Discover standalone xNFs using SNMP and Command-Line Interface \(CLI\).
-   Enrich CMDB data using Service Graph Connectors and specialized discovery patterns.
-   Identify discrepancies between discovered network data and inventory records.
-   Support automation use cases through consistent and accurate infrastructure visibility.

## Integration with ITOM Visibility

Telecom Discovery complements existing ITOM Visibility features. You can:

-   Use Horizontal Discovery and ITOM capabilities alongside TSOM plugins.
-   Maintain consistent discovery practices for IT and telecom resources.
-   Use the same CMDB data model to manage cross-domain service visibility.

This integration supports unified asset management, faster issue resolution, and streamlined operations across both IT and network domains.

## Customization with low-code and no-code tools

Telecom Discovery provides design tools to extend discovery logic without writing code. You can:

-   Build or modify custom Service Graph Connectors.
-   Extend Telecommunications Discovery Patterns to match vendor-specific requirements.
-   Accelerate onboarding of new device types and network domains.

This approach helps CSPs adapt and reduce onboarding time when expanding their discovery coverage.

## Key components

-   Telecommunication Discovery Patterns \(sn\_tsom\_patterns\): Provides patterns for SNMP-based discovery of standalone routers, switches, and xNFs. Includes Cisco and Juniper-specific discovery logic.
-   Service Graph Connector for Nokia Altiplano \(sn\_sgc\_altiplano\_connector\): Enables data collection from the Nokia Altiplano Access SDN Controller via REST APIs.
-   Telecom Core \(sn\_tsom\_core\): Delivers foundational capabilities such as discrepancy identification, remediation logic, and shared telecom discovery features.

**Related topics**  


[Configure Telecom Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configuring-tsom-visibility.md)

[Use Telecom Discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/using-telecom-discovery-patterns.md)

