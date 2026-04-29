---
title: Platform security granular admin roles
description: Use granular admin roles to verify access management by assigning roles that define user permissions and responsibilities.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Granular admin roles, platform security admin roles, ServiceNow security admin roles, security admin, security roles, access management, security assigning roles, maintain security, enforce conformance]
breadcrumb: [Granular admin roles]
---

# Platform security granular admin roles

Use granular admin roles to verify access management by assigning roles that define user permissions and responsibilities.

**Tip:** Use the search field to filter the granular admin role by entering keywords related to the role name or product.

<table id="Platform-Security-granular-admin-roles" class="custom-rows"><thead><tr><th>

Product

</th><th>

Role required

</th><th>

Role description

</th></tr></thead><tbody><tr><td>

Access Analyzer

</td><td>

access\_analyzer\_admin

</td><td>

Role required to access the Access analyzer to compare user records and access, simulate user access, and view access insights. To learn more, see [Access Analyzer](../../../integrate/identity/concept/access-analyzer.md).

</td></tr><tr><td>

Adaptive Authentication

</td><td>

adaptive\_auth\_admin

</td><td>

Role required to configure adaptive authentication policies. To learn more, see [Adaptive authentication](../../../integrate/authentication/concept/adaptive-authentication.md).

</td></tr><tr><td>

Authentication Factors

</td><td>

auth\_factors\_admin

</td><td>

Role required to configure authentication for voice agent environments, with the factors that first identify the caller, then authenticate them before granting access.

</td></tr><tr><td>

API Access Policies, API Auth Scopes, Processor Access Policies

</td><td>

-   api\_service\_admin
-   adaptive\_auth\_policy\_admin

</td><td>

Role required to enable users to configure non-oauth related functionality like REST or SOAP policies, inbound authentication profiles, token based auth, processors.

</td></tr><tr><td>

Custom URL

</td><td>

custom\_url\_admin

</td><td>

Role required to configure custom URL, view datacenters jobs in read-only mode, and select portal and SSO records. To learn more, see [Custom instance URLs](../../../integrate/authentication/concept/custom-url.md).

</td></tr><tr><td>

E-signature with SSO

</td><td>

-   sso\_config\_admin
-   script\_include\_admin
-   ui\_page\_admin

</td><td>

Role required to configure E-signature with SSO \(SAML or OIDC\) only and not required if using local database login. To learn more, see [E-signature for Multi-Provider SSO](../../../integrate/authentication/concept/e-signature-for-multi-provider-sso.md).

</td></tr><tr><td>

Encryption

</td><td>

security\_admin

</td><td>

Role required to perform security operations as an admin.

</td></tr><tr><td>

Encryption

</td><td>

sn\_kmf.admin

</td><td>

Role required to have admin and security admin access to be sn\_kmf.admin. Can assign sn\_kmf.cryptographic\_manager or sn\_kmf.cryptographic\_auditor role to other users and has read, write, and execution permissions for key operations.

</td></tr><tr><td>

Encryption

</td><td>

sn\_kmf.cryptographic\_auditor

</td><td>

Role required to have read permission for key operations.

</td></tr><tr><td>

Encryption

</td><td>

sn\_kmf.cryptographic\_manager

</td><td>

Role required to have read, write, and execution permissions for key operations.

</td></tr><tr><td>

Federated ID

</td><td>

iamsync\_admin

</td><td>

Role required to manage the Federated ID and read or write Federated ID related property. To learn more, see [Global Identity](../../../integrate/identity/concept/global-identity.md).

</td></tr><tr><td>

Identity AI Agent

</td><td>

ai\_user\_admin

</td><td>

Role required to manage AI user identities within the instance. They can create,edit,delete AI users, and assign or remove roles associated with them.

</td></tr><tr><td>

Identity AI Agent

</td><td>

agent\_role\_config\_admin

</td><td>

Role required to configure and manage AI agent access during agentic workflow execution. You can mask roles for AI agents using the Agent Access Role Configurations table helping protect sensitive data and enforce role-based restrictions.

</td></tr><tr><td>

Identity AI Agent

</td><td>

agent\_role\_config\_viewer

</td><td>

Role required to view existing records on the Agent Access Role Configurations table.

</td></tr><tr><td>

Identity and Access audit

</td><td>

identity\_access\_audit\_viewer It contains:

-   role\_viewer
-   group\_viewer

</td><td>

Role required to view the User Trails, Group Trails, Role Trails, ACL Trails and Audit results.

</td></tr><tr><td>

Identity and Access audit

</td><td>

security\_admin

</td><td>

Role required to:-   Configure Retention Period, Configure Tables &amp; Fields.
-   Change identity security audit feature property.

</td></tr><tr><td>

Identity Center

</td><td>

user\_login\_history\_viewer

</td><td>

Role required to view login history details in the Identity Center, including login timestamps, browser information,IP address, and login status. Supports security investigations by enabling filtered views of login actions and helps identify suspicious activity. To learn more, see [Identity Center for users](../../../integrate/identity/concept/identity-center-for-user.md).

</td></tr><tr><td>

Identity Center

</td><td>

privileged\_role\_config\_admin

</td><td>

Role required to grants full access to manage role configurations in the Identity Center, including adding, deleting, creating, reading, and viewing reports in the **sys\_icenter\_role\_config** table. To learn more, see [Identity Metrics for administrators](../../../integrate/identity/concept/identity-center-for-admin.md).

</td></tr><tr><td>

Identity Center

</td><td>

role\_viewer

</td><td>

Role required to only view the records in the **sys\_icenter\_role\_config** table. To learn more, see [Identity Center for users](../../../integrate/identity/concept/identity-center-for-user.md).

</td></tr><tr><td>

Instance operator

</td><td>

instance\_operatorIt contains:

-   identity\_access\_audit\_viewer
-   user\_role\_history\_viewer

</td><td>

Role required to manage perform specific role related operations and know about identity access audits.

</td></tr><tr><td>

Machine Identity Console

</td><td>

mi\_admin

</td><td>

Role required to manage identities that interact with systems and data. To learn more, see [Machine Identity Console](../../../integrate/machine-identity/concept/machine-identity-console.md).

</td></tr><tr><td>

Password policy

</td><td>

password\_policy\_admin

</td><td>

Role required to configure password policy-related items. To learn more, see [Local authentication](../../../integrate/authentication/concept/local-authentication.md)

</td></tr><tr><td>

Role delegation

</td><td>

role\_delegator\_admin

</td><td>

Role required for role delegation.

</td></tr><tr><td>

Roles

</td><td>

user\_role\_history\_admin It contains:

-   user\_role\_history\_viewer
-   role\_viewer

</td><td>

Role required to manage perform specific role related operations.

</td></tr><tr><td>

SCIM

</td><td>

scim\_admin

</td><td>

Role required to configure and manage SCIM provisioning, including creating customization properties, supported and extension schema, and ETL definitions for user and group data. To learn more, see [System for Cross-domain Identity Management \(SCIM\)](../../../integrate/authentication/concept/scim.md).

</td></tr><tr><td>

SCIM custom schema

</td><td>

scim\_config\_admin

</td><td>

Role required to configure SCIM custom schema and system properties. To learn more, see [SCIM customization properties and schemas](../../../integrate/authentication/concept/scim-customization-properties-and-schemas.md).

</td></tr><tr><td>

SCIM Client

</td><td>

scim\_client\_config\_admin

</td><td>

Role required to configure SCIM Client. To learn more, see [SCIM Client](../../../integrate/authentication/concept/scim-client-app.md).

</td></tr><tr><td>

SCIM Provider

</td><td>

scim\_admin

</td><td>

Role required to configure SCIM Provider. To learn more, see [SCIM Provider](../../../integrate/authentication/concept/scim-provider.md).

</td></tr><tr><td>

Self-Register to ServiceNow instance

</td><td>

external\_user\_self\_registration\_admin

</td><td>

Role required to on-board a large volume of external users to your instance. To learn more, see [Self-register to ServiceNow instance](../../../integrate/authentication/concept/external-user-self-registration.md).

</td></tr><tr><td>

ServiceNow Vault

</td><td>

sn\_vault\_console.vault\_console\_admin

</td><td>

Role required to have a collection of Data Classification admin, Data Privacy admin, and CA Admin roles to execute a template flow and monitor sensitive data. To learn more, see [Configuring ServiceNow Vault](../../vault/concept/configuring-servicenow-vault.md)

</td></tr><tr><td>

ServiceNow Vault

</td><td>

sn\_vault\_console.vault\_console\_auditor

</td><td>

Role required to have a collection of Data Discovery Auditor, Data Classification Auditor, Data Privacy Auditor, and Continuous Auth Auditor roles to view the policies and metrics related to ServiceNow Vault.

</td></tr><tr><td>

SSO \(SAML and OIDC\)

</td><td>

-   sso\_config\_admin
-   business\_rule\_admin
-   script\_include\_admin

</td><td>

Role required to configure SSO configuration \(SAML or OIDC\). To learn more, see [Multi-Provider single sign-on \(SSO\)](../../../integrate/single-sign-on/concept/c_MultipleProviderSingleSignOn.md).

</td></tr><tr><td>

System OAuth

</td><td>

oauth\_admin

</td><td>

Role required to configure all OAuth related functionality. To learn more, see [OAuth Inbound and Outbound authentication](../../../integrate/authentication/concept/api-inbound-and-outbound.md).**Note:** You must assign the following roles for the following configurations:

-   The **admin** role for non out of the box properties.
-   The **script\_include\_admin** to change existing scripts \(JWT, and so on\).

</td></tr><tr><td>

Time limited role

</td><td>

user\_admin

</td><td>

Role required to assign a role to a user temporarily, usually if the user must perform a one-time action that is normally not permissible by their role.

</td></tr><tr><td>

User Impersonation

</td><td>

user\_impersonation\_history\_viewer

</td><td>

Role required to see the user impersonation history table.

</td></tr><tr><td>

Security Center

</td><td>

sn\_vsc.security\_center\_admin

</td><td>

Role required to access Security Center consoles and tools. Users with this role can also create and manage security tasks.

</td></tr></tbody>
</table>**Parent Topic:**[Granular admin roles](granular-admin-roles.md)

