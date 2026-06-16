---
title: DevOps Config Exporter Content Pack release notes
description: Version history for the ITSM DevOps Config Exporter Content Pack on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-devops-config-exporter-content-pack.html
release: store
topic_type: reference
last_updated: "2023-08-03"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - DevOps release notes, ServiceNow Store release notes]
---

# DevOps Config Exporter Content Pack release notes

Version history for the ITSM DevOps Config Exporter Content Pack on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.3.0 - August 2023**

    Fixed: returnDataForNodeName Added the includeNodeInOutput argument to return the node data after excluding the node name.

-   **Version 2.2.0 - February 2023**

    Fixed: returnDataForNodeName and fixed an issue with incorrect data being returned

-   **Version 2.1.0 - November 2022**

    Changed: Added support for multiple keys as an input for returnValueforUniqueKeyName exporter

-   **Version 2.0.0 - August 2022**
    -   The DevOps Config Exporter Content Pack is an optional plugin that contains curated exporters that the DevOps Config team created for you to leverage out-of-the-box so you can export the configuration data from your snapshots in the way you need it.
    -   Tenets of the DevOps Config Exporter Content Pack:
        -   All exporters are provided as-is. To modify an exporter to fit your requirements, make a copy and update the copy.
        -   ServiceNow will only make updates to the exporters on the condition where the exporter has been found not to work as intended per ServiceNow's testing requirements.
        -   ServiceNow may choose, at any time, to add/remove exporters from the default set as appropriate
    -   Note: If you install this plugin first, you will get DevOps Config and all dependencies automatically installed as well. If you choose to install the product via this route, ensure to install DevOps Config Insights immediately after so that you are not hit with an error upon entering the DevOps Config workspace.

