---
title: Set up SAP integration to establish a connection with SAP
description: Configure SAP integration to establish a connection between your Software Asset Management application and SAP.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/setup-sap-integration.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management, Asset Management]
---

# Set up SAP integration to establish a connection with SAP

Configure SAP integration to establish a connection between your Software Asset Management application and SAP.

Configure SAP integration, users, roles, and authorizations that are required to establish a connection between your Software Asset Management application and SAP.

1.  [Deploy the ABAP program for SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/import-abap-program-sap.md)
2.  [Create a WSDL for the SAP service definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/create-wsdl-sap-service.md)
3.  [Create SAP users, roles, and authorizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/create-sap-users-roles-auth.md)
4.  [Upload the license ruleset for SAP S/4HANA Private Cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/upload-license-ruleset-sap-private-cloud.md)
5.  [Export the Root CA certificate from SAP for Private Cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/export-root-ca-cert-sap-private-cloud.md)
6.  [Select SAP clients to import data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/select-sap-clients-import.md)
7.  [Activate OData services and assign a system alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/activate-odata-services-sap.md)
8.  [Create a system user for OAuth authentication in SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/create-system-user-oauth-sap.md)
9.  [Configure an OAuth client in SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/configure-oauth-client-sap.md)
10. [Configure roles and authorizations for the OAuth user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/configure-roles-auth-oauth-user.md)

**Note:** The steps to upload the license ruleset and export the Root CA certificate apply only to SAP S/4HANA Cloud, Private Edition deployments. On-premises SAP deployments do not require these steps.

## SAP jobs that must be scheduled

You must schedule the following program as a weekly job in the central system where the SAP transports are installed and the roles are configured:

Program name: `/NOW/SAMP_ENGINES_PROG`

Frequency: Weekly \(every Thursday\)

-   **[Deploy the ABAP program for SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/import-abap-program-sap.md)**  
Deploy the Advanced Business Application Programming \(ABAP\) program to establish a connection between your SAP system and your ServiceNow instance. Deploying the ABAP program allows data to be shared between SAP and your ServiceNow instance.
-   **[Create a WSDL for the SAP service definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/create-wsdl-sap-service.md)**  
Generate a Web Services Description Language \(WSDL\) URL for the SAP service definition to use when creating SAP connections on your ServiceNow instance.
-   **[Create SAP users, roles, and authorizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/create-sap-users-roles-auth.md)**  
Create the SAP user, roles, and authorization objects required for the Software Asset Management integration with the central and satellite SAP systems.
-   **[Upload the license ruleset for SAP S/4HANA Private Cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/upload-license-ruleset-sap-private-cloud.md)**  
Upload the license ruleset file to your SAP system to enable Full Usage Equivalent \(FUE\) user classification for SAP S/4HANA Cloud, Private Edition.
-   **[Export the Root CA certificate from SAP for Private Cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/export-root-ca-cert-sap-private-cloud.md)**  
Export the Root CA certificate from your SAP system and upload it to your ServiceNow instance to establish a trusted HTTPS connection for SAP S/4HANA Cloud, Private Edition integration.
-   **[Select SAP clients to import data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/select-sap-clients-import.md)**  
Select the Remote Function Call \(RFC\) connections that the SAP ABAP program uses to import data from your SAP clients into the central system and then into your ServiceNow instance.
-   **[Activate OData services and assign a system alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/activate-odata-services-sap.md)**  
Activate the OData services and assign a system alias to support OAuth 2.0 authentication for integration with the Software Asset Management application.
-   **[Create a system user for OAuth authentication in SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/create-system-user-oauth-sap.md)**  
Create a dedicated system user in SAP to serve as the OAuth 2.0 client ID for the Software Asset Management integration.
-   **[Configure an OAuth client in SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/configure-oauth-client-sap.md)**  
Register and configure an OAuth 2.0 client in SAP using the system user created for OAuth authentication, to enable secure data exchange with your ServiceNow instance.
-   **[Configure roles and authorizations for the OAuth user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/configure-roles-auth-oauth-user.md)**  
Create a role in SAP and assign the required authorization objects to the OAuth system user to support OData service access and background job execution for integration with the Software Asset Management application.

**Parent Topic:**[Software Asset Management publisher pack for SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/sap-publisher-pack.md)

**Related topics**  


[SAP publisher pack integration architecture]()

[Tables installed with the SAP publisher pack]()

[Establish an SAP connection using basic authentication]()

[Establish an SAP connection using OAuth 2.0]()

[Create software models for SAP]()

[Create entitlements for SAP]()

[Create a custom SAP named user type]()

[Map a role to a named user type]()

[Create custom SAP price lists]()

[Import custom SAP named user types]()

[Import custom SAP price lists]()

[SAP USMM-based optimization]()

[User transaction activity for named user types]()

[Self-declaring SAP engine license usage]()

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic]()

[Publisher overview for SAP in the Software Asset Workspace]()

