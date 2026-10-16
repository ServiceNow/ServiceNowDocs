---
title: AI Service Graph Connector for GCP Vertex AI release notes
description: Version history for the ServiceNow AI Service Graph Connector for GCP Vertex AI application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-ai-sgc-gcp-vertex-ai.html
release: store
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Integration Hub version history release notes, ServiceNow Store - ServiceNow AI Platform Capabilities version history release notes, ServiceNow Store version history release notes]
---

# AI Service Graph Connector for GCP Vertex AI release notes

Version history for the ServiceNow® AI Service Graph Connector for GCP Vertex AI application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 1.4.1 - October 2026**
    -   New:
        -   Implement user-friendly functional error messaging across GCP SGC data source APIs
        -   Import Gemini Enterprise App Agents
        -   Import  Gemini Enterprise App Agents Usage
        -   Import the following additional attributes
            -   Platform Name information
            -   Owner / Created by - critical for classification and accountability
            -   Project / Resource ID
            -   Identity / Access information
            -   Original Creation Date
        -   Import the tags of the AI agent to "cmdb\_key\_value" table
    -   Changed: Add UX changes for Beta API usage for Gemini Enterprise App
    -   Fixed:
        -   The connector creates a Consumes::Consumed by relationship between AI Function CIs instead of Depends on::Used by. PRB2086636
        -   Staging table inserts are processed sequentially, causing slow performance when discovering large numbers of Vertex AI assets. PRB2075641
        -   The Gemini Enterprise discovery pipeline creates AI Function-to-Model relationships using the Consumes::Consumed by relationship type instead of Depends on::Used by. PRB2089225
        -   If a single AI asset fails to insert during discovery, the remaining assets in the same discovery run aren't processed. PRB2089224
        -   The Test IAM Permission action doesn't work correctly for connections configured with the JSON key file upload method. PRB2090569
        -   Test Connection fails with an unhandled error, instead of returning a clear error message, when run against an invalid or missing connection. PRB2089222
        -   If a data source template has a missing or deleted data source reference, provisioning stops and the remaining templates aren't provisioned. PRB2089221
-   **Version 1.3.3 - September 2026**
    -   New:
        -   Google Multi-region support with parallel data loading
        -   Domain support on all staging tables
    -   Changed: Plugin name: AI Service Graph Connector for Google and SourceSystem updated to Google Agent Platform
    -   Fixed: Improved pre-validation checks for AI connection permissions and fields within playbooks in the AI Control Tower Workspace.
-   **Version 1.2.4 - August 2026 \(Australia\)**

    Changed: The Service Graph Connector for GCP Vertex AI now displays as "AI Connector for Google" to align with the AI Connector naming convention. The connector’s functionality remains unchanged.

-   **Version 1.2.3 - August 2026 \(Zurich\)**

    Changed: The Service Graph Connector for GCP Vertex AI now displays as "AI Connector for Google" to align with the AI Connector naming convention. The connector’s functionality remains unchanged.

-   **Version 1.1.1 - July 2026**

    Fixed: Corrected GCP Vertex AI discovery to properly handle unmanaged asset classification during transformation processing.

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


**Parent Topic:**[ServiceNow Store - Integration Hub version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

