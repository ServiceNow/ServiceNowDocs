---
title: Security for Oracle E-Business Suite connections in Zero Copy Connector for ERP
description: Learn how access control lists \(ACLs\) protect Oracle E-Business Suite \(EBS\) data in Zero Copy Connector for ERP, and which authentication methods Oracle EBS connections support.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/erp-integration-framework/erp-canvas-oracle-ebs-security.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [oracle, ebs, security, acl, zero copy connector for erp, oracle e-business suite, oracle ebs security, oracle ebs acl, access control list, oracle ebs authentication]
breadcrumb: [Connecting to Oracle EBS, Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Security for Oracle E-Business Suite connections in Zero Copy Connector for ERP

Learn how access control lists \(ACLs\) protect Oracle E-Business Suite \(EBS\) data in Zero Copy Connector for ERP, and which authentication methods Oracle EBS connections support.

## Role-based access to Oracle EBS data

Access control lists \(ACLs\) grant the sn\_erp\_integration.erp\_user role read access to the Oracle EBS tables, model operations, and configuration records. Users without this role can't read Oracle EBS data, even when the connection is healthy.

Oracle EBS follows the same ACL pattern as the SAP and Workday tables. For the full role list, see [Zero Copy Connector for ERP roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-canvas-roles.md).

The ACLs cover the tables that store WADL service catalog, endpoint, and schema cache records.

## Authentication

For the authentication methods supported across Oracle REST connections generally, see [Authentication methods for Oracle REST connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-rest-authentication-methods.md).

