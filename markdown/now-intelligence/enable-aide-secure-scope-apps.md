---
title: Enabling access to protected scope applications for AI Data Explorer and Query Generation
description: AI Data Explorer and Query Generation require additional security configuration to access tables in protected scopes such as Human Resources or Employee Profile scopes.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-30"
reading_time_minutes: 2
keywords: [AI Data Explorer, Query Generation, protected scope, ACL, RCA]
breadcrumb: [Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Enabling access to protected scope applications for AI Data Explorer and Query Generation

AI Data Explorer and Query Generation require additional security configuration to access tables in protected scopes such as Human Resources or Employee Profile scopes.

Protected scopes in ServiceNow restrict access to sensitive data, ensuring that only authorized users can view or interact with specific tables. When AI Data Explorer and Query Generation attempt to access tables within these protected scopes, additional security measures must be configured to enable proper functionality.

Outside of protected scopes, AI Data Explorer and Query Generation use standard Access Control Lists \(ACLs\) shipped with the plugin. These ACLs are sufficient for unprotected scopes where normal security rules apply. However, protected scopes introduce additional restrictions that help prevent even administrators from accessing certain data without explicit authorization.

When a table is linked to a protected scope, the scope takes ownership of security decisions for that table. This means that the standard ACLs shipped with AI Data Explorer and Query Generation are no longer sufficient. The protected scope requires its own set of ACLs that mirror the functionality that the plugin’s standard ACLs provide.

Additionally, when Query Generation attempts to fetch data from protected scope tables through API calls, the system creates Restricted Caller Access \(RCA\) records. These records must be approved by administrators with appropriate scope permissions before the data access can proceed. This approval process ensures that cross-scope data access is explicitly authorized and monitored.

Without proper ACL configuration, users cannot create or read records in AI Data Explorer for protected scope tables. Without approved RCA records, Query Generation cannot fetch data or generate insights for protected scope tables, resulting in error messages and limited functionality.

The security configuration process involves two main components: creating scope-specific ACLs that call a public script include provided by the AI Data Explorer plugin, and approving RCA records that enable Query Generation to access protected scope data through API calls. Both components are necessary for full functionality with protected scopes.

1.  [Create ACLs for AI Data Explorer and Query Generation protected scope access](../task/create-acls-protected-scope-access.md)  
Create Access Control Lists \(ACLs\) in protected scopes to enable AI Data Explorer and Query Generation to access tables within those scopes.
2.  [Approve RCA records for AI Data Explorer and Query Generation protected scope access](../task/create-rca-records-protected-scope-access.md)  
Approve automatically generated Restricted Caller Access \(RCA\) records to enable AI Data Explorer and Query Generation to fetch data from tables in protected scopes through API calls.

**Parent Topic:**[Configuring Query Generation](configuring-query-generation.md)

