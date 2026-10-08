---
title: Palo Alto Prisma AIRS AI Service Graph Connector
description: The AI Service Graph Connector \(SGC\) for Palo Alto Prisma AIRS integrates ServiceNow with Palo Alto Networks Prisma AIRS to discover AI models and import critical metrics related to AI security findings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/palo-alto-prisma-airs-ai-sgc.html
release: australia
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 2
keywords: [Palo Alto Prisma AIRS, AI Service Graph Connector, AI models, vulnerability scans, red teaming]
breadcrumb: [Integrate, Unified Security Exposure Management, Security Operations]
---

# Palo Alto Prisma AIRS AI Service Graph Connector

The AI Service Graph Connector \(SGC\) for Palo Alto Prisma AIRS integrates ServiceNow with Palo Alto Networks Prisma AIRS to discover AI models and import critical metrics related to AI security findings.

The connector imports three categories of data:

-   AI model inventory – models discovered by Prisma AIRS
-   Vulnerability scan result metrics – model security scans and their rule or policy violations
-   Red teaming result metrics – adversarial attack-simulation jobs, individual attacks, and compliance-framework mappings \(for example, OWASP and MITRE ATLAS\)

## Imported data overview

Each data category is imported on its own schedule and surfaced in a different part of ServiceNow:

-   AI model records are stored as AI assets in the CMDB and are visible in AI Discovery and AI Control Tower asset inventory views, with a linked digital asset record created for application lifecycle management \(ALM\) tracking.
-   Vulnerability scans and their violations are stored in dedicated tables and summarized as teaser metrics on the AI Security Operations dashboard.
-   Red teaming scans, attacks, and compliance mappings are stored in dedicated tables and summarized as teaser metrics on the AI Security Operations and Model Validation dashboards.
-   With this AI service graph connector, AI stewards can see the security metrics related to vulnerabilities and validation results in AI control tower. However, to be able to view individual security finding records for further investigation or workflow management, AI security exposure management and the [Palo Alto Prisma AIRS integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/prisma-airs-integration.md) must be installed and configured.

-   **[Install the AI Service Graph Connector for Palo Alto Prisma AIRS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/palo-alto-prisma-airs-ai-sgc-install-configure.md)**  
Configure the AI Service Graph Connector to integrate ServiceNow with Palo Alto Networks Prisma AIRS and import AI model inventory and security findings.
-   **[Palo Alto Prisma AIRS to ServiceNow data mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/palo-alto-prisma-airs-ai-sgc-mapping.md)**  
Prisma AIRS API fields map to ServiceNow fields for AI models, vulnerability scans, red teaming scans, and compliance data.

**Parent Topic:**[Unified Security Exposure Management integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/integrating-usem.md)

