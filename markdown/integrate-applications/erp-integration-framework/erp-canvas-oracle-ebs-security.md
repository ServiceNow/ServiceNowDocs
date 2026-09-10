---
title: Security for Oracle E-Business Suite connections
description: Oracle E-Business Suite \(EBS\) connections in Zero Copy Connector for ERP use role-based access control, encrypted transport, and token-based authentication to protect ERP data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-canvas-oracle-ebs-security.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-08-24"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, oracle, ebs, security, acl, role, authentication]
breadcrumb: [Connecting to Oracle EBS, Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Security for Oracle E-Business Suite connections

Oracle E-Business Suite \(EBS\) connections in Zero Copy Connector for ERP use role-based access control, encrypted transport, and token-based authentication to protect ERP data.

## Role-based access to Oracle EBS data

Access control lists \(ACLs\) grant the sn\_erp\_integration.erp\_user role read access to the Oracle EBS tables, model operations, and configuration records. Users without this role can't read Oracle EBS data, even when the connection is healthy.

Oracle EBS follows the same ACL pattern as the SAP and Workday tables. For the full role list, see [Zero Copy Connector for ERP roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-roles.md).

The ACLs cover the tables that store WADL service catalog, endpoint, and schema cache records.

## Authentication

For the authentication methods supported across Oracle REST connections generally, see [Authentication methods for Oracle REST connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-rest-authentication-methods.md).

