---
title: ERP Semantic Mining and security
description: In addition to role-based security and access control, ERP Semantic Mining protects personally identifiable ERP \(Enterprise Resource Planning\) data in other ways.
locale: en-US
release: australia
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, ERP Semantic Mining overview, Workflow Data Fabric]
---

# ERP Semantic Mining and security

In addition to role-based security and access control, ERP Semantic Mining protects personally identifiable ERP \(Enterprise Resource Planning\) data in other ways.

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

Personally identifiable data is secured with Zero Copy Connector for ERP in several ways.

-   You can customize models and remote tables to exclude personal data in a specified field, such as email address.
-   All remote tables are secured using access control rules \(ACLs\). If you have a remote table that contains sensitive data, use ACLs to restrict that table from ServiceNow users. For more information, see [ServiceNow® access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_SNCAccessControl.md).

**Parent Topic:**[Configuring ERP Semantic Mining](configuring-ecm.md)

