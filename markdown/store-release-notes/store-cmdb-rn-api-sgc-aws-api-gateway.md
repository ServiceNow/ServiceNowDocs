---
title: API Service Graph Connector for AWS API Gateway release notes
description: Version history for the API Service Graph Connector for AWS API Gateway application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-cmdb-rn-api-sgc-aws-api-gateway.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# API Service Graph Connector for AWS API Gateway release notes

Version history for the API Service Graph Connector for AWS API Gateway application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.3.1 - June 2026**

    Security fix.

-   **Version 2.3.0 - January 2026**

    Fixed: Multiple security and quality improvements.

-   **Version 2.2.0 - September 2025**
    -   New: Added support for custom domains.
    -   Fixed: Improved processing of dynamic payloads that previously caused errors during Extract Transform Load \(ETL\) operations.
-   **Version 2.1.0 - August 2025**
    -   Use the ServiceNow CMDB as your normalized source of truth for APIs deployed on an AWS API Gateway service. Having your API inventory in the CMDB enables other workflows to be used in managing your API estate, including Security Operations, IT Service Management, IT Operations Management, Integrated Risk, and more. The ServiceNow API Insights workspace also provides a way for teams to interact with the API data so that certain stakeholders can analyze the data without requiring direct access to AWS.
    -   Configuring this API Service Graph Connector will retrieve the following objects from an AWS API Gateway:
        -   AWS API Gateway \(region + account\)
        -   API \(REST and v2\)
        -   Resources / Routes
        -   Integrations
        -   Deployments
        -   Usage plans
        -   Usage metrics \(Cloudwatch\)

**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)

