---
title: Telecom Discovery
description: ServiceNow AI Platform Telecom Discovery helps you gain comprehensive visibility into your telecom network infrastructure by extending the capabilities of ITOM Visibility to support telecom-specific use cases.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Telecommunications Service Operations Management]
---

# Telecom Discovery

ServiceNow AI Platform Telecom Discovery helps you gain comprehensive visibility into your telecom network infrastructure by extending the capabilities of ITOM Visibility to support telecom-specific use cases.

Built for communication service providers \(CSPs\), this solution enables the discovery and mapping of network elements across multi-vendor environments using standardized protocols and integration with network management systems.

By combining Telecom Discovery plugins with the power of Service Graph Connectors and Discovery Patterns, you can automatically populate and maintain accurate records of your telecom resources in the Configuration Management Database \(CMDB\), providing a unified view of both IT and network infrastructure.

**Note:** Telecom Discovery is part of the TSOM Visibility subscription and aligns with the TM Forum Autonomous Network Operations \(ANO\) framework.

With Telecom Discovery, you can:

-   Discover physical and logical telecom network resources across domains and vendors.
-   Integrate with Element Management Systems \(EMS\), Network Management Systems \(NMS\), and SDN Controllers.
-   Automatically populate and update CMDB/TNI records based on real-time network data.
-   Discover standalone xNFs using SNMP and Command-Line Interface \(CLI\).
-   Enrich CMDB data using Service Graph Connectors and specialized discovery patterns.
-   Identify discrepancies between discovered network data and inventory records.
-   Support automation use cases through consistent and accurate infrastructure visibility.

## Integration with ITOM Visibility

Telecom Discovery is designed to complement existing ITOM Visibility features. You can:

-   Leverage Horizontal Discovery and ITOM capabilities alongside TSOM plugins.
-   Maintain consistent discovery practices for IT and telecom resources.
-   Use the same CMDB data model to manage cross-domain service visibility.

This integration confirms unified asset management, faster issue resolution, and streamlined operations across both IT and network domains.

## Customization with low-code/no-code tools

Provides intuitive design tools to extend discovery logic without writing code. You can:

-   Build or modify custom Service Graph Connectors.
-   Extend Telecommunications Discovery Patterns to match vendor-specific requirements.
-   Accelerate onboarding of new device types and network domains.

This approach enables CSPs to stay agile and reduce time to value when expanding their discovery footprint.

## Key components

-   Telecommunication Discovery Patterns\(sn\_tsom\_patterns\): Provides patterns for SNMP-based discovery of standalone routers, switches, and xNFs. Includes Cisco and Juniper-specific discovery logic.
-   Service Graph Connector for Nokia Altiplano\(sn\_sgc\_altiplano\_connector\): Enables data collection from the Nokia Altiplano Access SDN Controller via REST APIs.
-   Telecom Core\(sn\_tsom\_core\): Delivers foundational capabilities such as discrepancy identification, remediation logic, and shared telecom discovery features.

**Related topics**  


[Configure Telecom Visibility](../task/configuring-tsom-visibility.md)

[Use Telecom Discovery patterns](using-telecom-discovery-patterns.md)

