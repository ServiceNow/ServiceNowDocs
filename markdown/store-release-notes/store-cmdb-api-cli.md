---
title: Customer Data Models for B2B2C release notes
description: Version history for the Customer Service Management Customer Data Models for B2B2C on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-cmdb-api-cli.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\) version history release notes, ServiceNow Store - ServiceNow AI Platform Capabilities version history release notes, ServiceNow Store version history release notes]
---

# Customer Data Models for B2B2C release notes

Version history for the Customer Service Management Customer Data Models for B2B2C on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.3.5 - September 2026**
    -   Changed:
        -   Query range access control on consumer tables: Query range ACLs on the consumer account and consumer tables now require specific roles. Users who don't hold an applicable role can no longer run range queries on these tables. A fix script applies these changes automatically on upgrade.
        -   Plugin renaming:Customer Data Models for B2B2C \(com.sn\_csm\_b2b\_consumers\) plugin is renamed to CRM B2B2C Entities \(com.sn\_csm\_b2b\_consumers\) plugin
-   **Version 2.2.0 - March 2026**
    -   New: Granular admin roles: Added new granular admin roles to enable targeted permission assignments based on functional responsibilities, replacing broad admin access.
    -   Changed: Enhanced Customer Data Viewer role: The Customer Data Viewer \(sn\_customerservice.customer\_data\_viewer\) role includes expanded access to additional data tables and menu items. These enhancements enable users to view a broader range of customer data while maintaining read-only access restrictions. With this enhancement, you can extend access to additional tables for the customer data viewer role. You can inherit household role in customer data viewer role and can explore additional menu items now accessible to the customer data viewer role.
-   **Version 1.0.1 - July 2021**

    New: Automation across the enterprise requires customers to move processes away from visual interface and instead leverage CLI/API to script critical operations. With the introduction of the CMDB Application CLI and API app, customers now have a robust API and CLI framework they can leverage. With the initial release, customers can use CLI/API to register an application service, create an application service, and find an application service as well as connect higher level constructs such as business application and business service offering. Future releases will add additional functionality all through the CLI/API App, without being completely tied to SN platform release.


