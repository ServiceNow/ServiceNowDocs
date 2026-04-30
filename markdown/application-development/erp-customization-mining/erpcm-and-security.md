---
title: ERP-CM and security
description: In addition to role-based security and access control, ERP Semantic Mining \(ERP-CM\) protects personally identifiable ERP \(Enterprise Resource Planning\) data in other ways.
locale: en-US
release: yokohama
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring ERP Semantic Mining, ERP Semantic Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# ERP-CM and security

In addition to role-based security and access control, ERP Semantic Mining \(ERP-CM\) protects personally identifiable ERP \(Enterprise Resource Planning\) data in other ways.

Personally identifiable data is secured with Zero Copy Connector for ERP and ERP-CM in several ways.

-   You can customize ERP models and remote tables to exclude personal data in a specified field, such as email address.
-   All remote tables are secured using access control rules \(ACLs\). If you have a remote table that contains sensitive data, use ACLs to restrict that table from ServiceNow users. For more information, see [ServiceNow® access control](https://www.servicenow.com/docs/access?context=c_SNCAccessControl&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

**Parent Topic:**[Configuring ERP Semantic Mining](configuring-ecm.md)

