---
title: API Service Graph Connector for Apigee X release notes
description: Version history for the API Service Graph Connector for Apigee X application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-cmdb-api-sgc-agipgee-x.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# API Service Graph Connector for Apigee X release notes

Version history for the API Service Graph Connector for Apigee X application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.4.1 - June 2026**

    Security fix.

-   **Version 2.4.0 - April 2026**
    -   New:
        -   Enhanced security controls
        -   Added mapping for API type
    -   Fixed: Improved quality checks and performance
-   **Version 2.3.0 - December 2025**
    -   Changed:
        -   Updated upgrade requirements. Updates to source native keys impact the Source \[sys\_object\_source\] table records and coordination with Now Support is required to prevent duplicate record creation.Important: Existing customers on production instances must contact Now Support before upgrading to the API Service Graph Connector for Apigee X v 2.3.0.
        -   Updated the mapping of the Base URL attribute in the Managed API \[cmdb\_ci\_managed\_api\] table.
        -   Updated the process to store host values in DNS Alias \[cmdb\_ci\_dns\_alias\] table and added new relationships.
        -   Mapped Life Cycle Stage and Life Cycle Stage Status attributes in the Managed API \[cmdb\_ci\_managed\_api\] table records.
    -   Fixed: Performance improvements for minimizing API calls to Apigee X.
-   **Version 2.2.2 - October 2025**

    Changed:

    -   Setting resource manager roles for organization, folder, and project-level queries is now optional.
    -   API front end naming conventions have been updated to use the environment name as a prefix to improve readability.
    -   Leaving the Expand HTTP methods property blank results in a single API front end being created with the ALL method.
    Fixed: Performance improvements.

-   **Version 2.1.0 - September 2025**
    -   New:
        -   Added an exclusion filter for environments during import. This allows more control over which APIs are imported. For example, only import APIs deployed to a production environment.
        -   New field mappings like the proxy description are now mapped into the Managed API description.
        -   Additional option to expand methods when none are defined on a proxy. For example, create a GET, POST, and so on in the API frontend record when "ALL" would otherwise exist.
        -   Performance improvements.
    -   Changed: Naming of the method value removed the proxy endpoint addition and is only one of the expected HTTP verbs now.
-   **Version 2.0.1 - May 2025**
    -   Use the ServiceNow CMDB as your normalized source of truth for APIs deployed on Apigee X. Having your API inventory in the CMDB enables other workflows to be used in managing your API estate, including Security Operations, IT Service Management, IT Operations Management, Integrated Risk, and more. The ServiceNow API Insights workspace also provides a way for teams to interact with the API data so that certain stakeholders can analyze the data without requiring direct access to Apigee X.
    -   Configuring this API Service Graph Connector will retrieve the following objects from an Apigee project in GCP:
        -   Apigee X gateway
        -   API proxies
        -   Proxy and target endpoints
        -   Target servers
        -   Deployments
        -   API Products
        -   Apps
        -   Developers
        -   Usage metrics

