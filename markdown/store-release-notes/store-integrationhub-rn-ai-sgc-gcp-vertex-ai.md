---
title: AI Service Graph Connector for GCP Vertex AI release notes
description: Version history for the ServiceNow AI Service Graph Connector for GCP Vertex AI application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-ai-sgc-gcp-vertex-ai.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# AI Service Graph Connector for GCP Vertex AI release notes

Version history for the ServiceNow® AI Service Graph Connector for GCP Vertex AI application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 1.1.0 - June 2026**
    -   New:
        -   Introduce Model Configuration Items \(CIs\) for AI assets with Asset-CI relationships linking each asset to its corresponding Model CI. For AI systems that utilize multiple models, CI-CI relationships are established to represent interdependencies between models and the AI system.
        -   Enhance record matching accuracy by replacing the coalesce field from name to external\_ref\_id, providing a more stable and unique identifier for the tool.
        -   Enhance the transform map scoping during scheduled job execution to process only managed assets, ensuring unmanaged assets are excluded from scheduled runs.
    -   Changed: The GCP credential store has been updated from gcp\_credentials to google\_cloud\_credentials.
    -   Fixed: The "Run As" Field is set to empty to the scheduled Imports instead of set to "System Administrator".
-   **Version 1.0.5 - April 2026**
    -   New:
        -   Discover the Model registry
        -   Connection can now be created by uploading a JSON file through the MID Server
-   **Version 1.0.4 - March 2026**
    -   New:
        -   AI Service Graph Connector integrates with Google Vertex AI and allows discovery and inventory of workflows with AI agents,related models, sub-agents, prompts, and tool information.
        -   The AI Control Tower \(AICT\) imports the discovered artifacts into its AI inventory, where the AI steward and Product Owner can access and review them.
-   **Version 1.0.3 - March 2026**

    This integration connects AI Control Tower’s AI Discovery capabilities with Google Vertex AI, enabling automated discovery and governance of AI assets across the enterprise Google environment.


**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

