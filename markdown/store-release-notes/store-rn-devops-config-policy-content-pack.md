---
title: DevOps Config Policy Content Pack release notes
description: Version history for the ITSM DevOps Config Policy application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-devops-config-policy-content-pack.html
release: store
topic_type: reference
last_updated: "2023-11-02"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - DevOps release notes, ServiceNow Store release notes]
---

# DevOps Config Policy Content Pack release notes

Version history for the ITSM DevOps Config Policy application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.6.0 - November 2023**
    -   New: 11 policies available by default to validate Red Hat OpenShift configuration.
    -   Changed: Minor changes and bug fixes.
-   **Version 1.5.0 - August 2023**
    -   New: 21 policies available by default to validate Kubernetes configuration
    -   Changed: Minor changes and bug fixes
-   **Version 1.4.0 - April 2023**
    -   New: A new set of policies have been added, including:

        -   dockerImageRegistryValidator
        -   dockerImageFormatValidator
        -   dockerNetworkValidator
        -   genericListValidator
        -   memoryLimitValidator
        -   sameKeyValue
        -   uniqueKeyValue
        -   detectUnusedVariable
    -   Fixed: Performance improvements and bug fixes.
    -   Changed: Variables are now excluded when validating the configuration data.
-   **Version 1.2.0 - November 2022**
    -   Changed:
        -   A new set of 7 policies that are data model focused have been added to the content pack, including:
            -   correctHostRegex
            -   differentKeyNamesSameValues
            -   keyNamingConvention
            -   keyPathValidator
            -   listComparator
            -   nodesKeyComparator
            -   nodesValueComparator
    -   For details on each policy and how to get started using them, refer to the DevOps Config product documentation.
-   **Version 1.1.0 - August 2022**
    -   The DevOps Config Policy Content Pack is an optional plugin that contains curated policies that the DevOps Config team created for you to leverage out-of-the-box so you can get right to validating your configuration data before customizing them or adding your own policies.
    -   Tenets of the DevOps Config Policy Content Pack:
        -   All policies are provided as-is. If users want to make adjustments to the policies to fit their requirements, they can make a copy of the policy to do so.
        -   ServiceNow will only make updates to the policies on the condition where the policy has been found not to work as intended per ServiceNow's testing requirements
        -   ServiceNow may choose, at any time, to add/remove policies from the default set as appropriate
    -   Note: if you install this plugin first, you will get DevOps Config and all dependencies automatically installed as well. If you choose to install the product via this route, ensure to install DevOps Config Insights immediately after so that you are not hit with an error upon entering the DevOps Config workspace.

**Parent Topic:**[ServiceNow Store - DevOps release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-devops-highlight.md)

