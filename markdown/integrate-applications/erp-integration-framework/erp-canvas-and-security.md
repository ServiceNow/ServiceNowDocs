---
title: Protecting personally identifiable data in Zero Copy Connector for ERP
description: Learn how Zero Copy Connector for ERP protects personally identifiable data from your ERP systems, beyond role-based security and access control.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/erp-integration-framework/erp-canvas-and-security.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [security, zero copy connector for erp, erp data security, personally identifiable information, pii, data privacy, role-based access control]
breadcrumb: [Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Protecting personally identifiable data in Zero Copy Connector for ERP

Learn how Zero Copy Connector for ERP protects personally identifiable data from your ERP systems, beyond role-based security and access control.

Personally identifiable data is secured with Zero Copy Connector for ERP \(Enterprise Resource Planning\) in several ways.

-   You can customize models and remote tables to exclude personal data in a specified field, such as email address.
-   All remote tables are secured using access control rules \(ACLs\). If you have a remote table that contains sensitive data, use ACLs to restrict that table from ServiceNow users. For more information, see [ServiceNow® access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_SNCAccessControl.md).

