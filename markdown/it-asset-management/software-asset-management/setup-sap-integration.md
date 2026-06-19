---
title: Set up SAP integration to establish a connection with SAP
description: Configure and set up SAP integration to establish a connection between your Software Asset Management application and SAP.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/setup-sap-integration.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-05-20"
reading_time_minutes: 1
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Set up SAP integration to establish a connection with SAP

Configure and set up SAP integration to establish a connection between your Software Asset Management application and SAP.

Follow these steps to configure SAP integration, users, roles, and authorizations that are required to establish a connection between your Software Asset Management application and SAP.

1.  [Deploy the ABAP program for SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/import-abap-program-sap.md)
2.  [Create a WSDL for the SAP service definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/create-wsdl-sap-service.md)
3.  [Create SAP users, roles, and authorizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/create-sap-users-roles-auth.md)
4.  [Select SAP clients to import data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/select-sap-clients-import.md)
5.  [Activate OData services and assign a system alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/activate-odata-services-sap.md)
6.  [Create a system user for OAuth authentication in SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/create-system-user-oauth-sap.md)
7.  [Configure an OAuth client in SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/configure-oauth-client-sap.md)
8.  [Configure roles and authorizations for the OAuth user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/configure-roles-auth-oauth-user.md)

## SAP jobs that must be scheduled

You must schedule the following program as a weekly job in the central system where the SAP transports are installed and the roles are configured:

Program name: `/NOW/SAMP_ENGINES_PROG`

Frequency: Weekly \(every Thursday\)

