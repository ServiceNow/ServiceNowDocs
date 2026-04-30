---
title: Access control
description: The access control category audits the process of protecting resources from unauthorized access through granting and denying requests based on a permission model. This includes ensuring an entity accessing a resource holds valid credentials to do so, creating and protecting a well-defined set of roles or permissions and ensuring role or permission controls are protected from replay and tampering.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 12
breadcrumb: [Hardening settings, Platform Security]
---

# Access control

The access control category audits the process of protecting resources from unauthorized access through granting and denying requests based on a permission model. This includes ensuring an entity accessing a resource holds valid credentials to do so, creating and protecting a well-defined set of roles or permissions and ensuring role or permission controls are protected from replay and tampering.

Access controls determine whether access to a particular resource should be granted or denied. It only allows access to resources to those users permitted to use them.

-   **[Anti-CSRF token validation time \[New in Security Center 1.3\]](sc-anti-csrf-token-validation-time.md)**  
The **glide.security.csrf\_previous.time\_limit** property specifies the time in seconds for a secure token to expire.
-   **[Apply domain separation on dot walked fields \[Updated in Security Center 1.3, 1.5, and 2.0\]](sc-apply-domain-separation.md)**  
The **glide.sys.domain.include\_domain\_condition\_on\_join** property controls whether join queries are given domain separated conditions or not in order to ensure they apply domain separation functionality for dot walked fields.
-   **[Enable scoped admin application ACLs \[Updated in Security Center 1.3\]](sc-administer-scoped-admin-application-acls.md)**  
The **glide.security.scoped\_administration.honor\_global\_acl** determines whether an application administration app can inherit global access control list \(ACL\) rules.
-   **[Enable work order management query rules for service organizations \[New in Security Center 1.5 and updated in 2.0\]](sc-enable-work-order-management-query-rules.md)**  
Use the **sn\_fsm.use\_query\_rules** property to apply rules and filters to the Field Service Management tables.
-   **[Block access for delegated developers](sc-block-access-for-delegated-developers.md)**  
This configuration affects access for delegated developers that are updating user roles through script. When the configuration is compliant, the developer will not be able to update or insert records into the sys\_user\_has\_role table without also having the user\_admin role.
-   **[Block Expired Anti-CSRF Tokens \[Updated in Security Center 1.5\]](sc-block-expired-csrf-tokens.md)**  
Block expired CSRF tokens to prevent cross-site request forgery attacks.
-   **[Check UI action conditions before execution](sc-check-ui-action-conditions-before-execution.md)**  
Use the **glide.security.strict.actions** property to enable checking of UI actions conditions in forms and lists before they execute. When you set this property to true, it adds an extra layer of validation on the table UI actions before they are executed.
-   **[Configure event management assignment group admin roles \[New in Security Center 1.5\]](sc-configure-event-management-assignment-group-admin-roles.md)**  
Use the **evt\_mgmt.connector\_assignment\_group\_admin\_roles** property to set which roles are authorized for admin access over the assignment group field in connector instances.
-   **[Configure Service Portal Widgets Allow List \[New in Security Center 2.0\]](sc-configure-service-portal-widgets-allow-list.md)**  
Learn how to configure the glide.service\_portal.widget.allow\_list property securely so that the access control lists \(ACLs\) for the tables do not expose sensitive information.
-   **[Configure Service Portal Widgets Table Allow List \[New in Security Center 2.0\]](sc-configure-service-portal-widgets-table-allow-list.md)**  
Learn how the **glide.service\_portal.widget.table\_allow\_list** property enhances security by listing tables accessible to unauthenticated users through Service Portal widgets, dependent on additional checks and specific glide property settings.
-   **[Deny internal access to explicit external roles \[Updated in Security Center 1.3 and 1.5\]](../../security/reference/sc-enable-explicit-roles-internal-denylist.md)**  
Use system properties to determine whether external users can be assigned the snc\_internal role.
-   **[Deny unauthorized access to request items \[Updated in Security Center 1.3\]](sc-deny-unauthorized-access-to-request-items.md)**  
The **glide.sc.req\_for.roles.default** property defines a default behavior for the retrieveAddress API.
-   **[Enable Anti-CSRF token \[New in Security Center 1.3, updated in 1.5, and removed in 2.0\]](sc-anti-csrf-token.md)**  
Use the **glide.security.use\_csrf\_token** property to ensure the use of a secure token to identify and validates incoming requests, which in turn are used to prevent these attacks.
-   **[Ensure archive table ACLs are checked \[New in Security Center 1.3 and updated in 1.5\]](sc-ensure-archive-table-acls-are-checked.md)**  
The **glide.security.enable\_archive\_table\_acls** property controls whether access control lists \(ACLs\) of the original table, the table the archive table was created from, are evaluated to false.
-   **[Enforce ACL on HR Lifecycle Events Data \[New in Security Center 2.0\]](sc-enforce-acl-on-hr-lifecycle-events-data.md)**  
Learn how to prevent unauthorized access to data in the Human Resources Lifecycle Events application by verifying that the **glide.enforce\_security\_scope.sn\_hr\_le property** is set to the secured value.
-   **[Enforce application specific ACLs only for application data](sc-enforce-application-specific-acls-only-for-application-data.md)**  
Avoid unauthorized or undesired access to application data by enforcing application-specific access control lists \(ACLs\) only for application data.
-   **[Enable contextual security plugin \[Updated in Security Center 1.3\]](sc-contextual-security-plugin.md)**  
Activate the Contextual Security Plugin \(**com.glide.role\_management**\) plugin to enable contextual security, which secures a record/information using create, read, write, and delete functionality.
-   **[Enforce security scope license and permit playbook \[New in Security Center 1.5 and updated in 2.0\]](sc-enforce-security-scope-license-and-permit-playbook.md)**  
Use this property to determine if only the access control lists \(ACLs\) within the License and Permit plugin will be used in determining access to the scope, or if ACLs from all scopes will be considered.
-   **[Enforce Security Scope for Agent Workspace for HR Case Management \[New in Security Center 1.5 and updated in 2.0\]](sc-enforce-security-scope-for-agent-workspace-hr-case.md)**  
Configure the Agent Workspace for HR Case Management plugin so that data in scope master tables can only be accessed by users with the correct permissions, enforcing the principle of least privilege.
-   **[Prevent Users From Accepting Warning To Bypass CSRF Validation \[Updated in Security Center 1.3 and 1.5\]](sc-csrf-strict-validation.md)**  
Use the **glide.security.csrf.strict.validation.mode** property to enable CSRF token strict validation. If the CSRF token doesn't match, it prevents resubmission of the request.
-   **[Enforce ACL on HR Core Data \[New in Security Center 2.0\]](sc-enforce-acl-on-hr-core-data.md)**  
Learn how to configure the **glide.enforce\_security\_scope.sn\_hr\_core** property so that the Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin does not expose sensitive data to access control lists \(ACLs\) from all other scopes.
-   **[Enforce ACL on HR Virtual Agent Data \[New in Security Center 2.0\]](sc-enforce-acl-on-hr-virtual-agent-data.md)**  
Discover how to set the **glide.enforce\_security\_scope.sn\_hr\_va** property to a secure value, preventing data leakage from the Virtual Agent Conversations scoped application.
-   **[Enforce Read Roles for Catalog Variable Search](sc-enforce-read-roles-for-catalog-variable-search.md)**  
Use system properties to ensure that only catalog variables with an empty read role are indexed for search.
-   **[Enforce Security Scope for Service Application Information \[New in Security Center 2.0\]](sc-enforce-security-scope-for-service-application-information.md)**  
Use the **glide.enforce\_security\_scope.sn\_svc\_appl** property to ensure that the data in master scope tables is secured.
-   **[Enable Cross Scope Privilege Checks on Service Portal Form](sc-enable-cross-scope-privilege-checks-on-service-portal-form.md)**  
Use a system property to enforce cross scope privilege checks on the Service Portal form widget and prevent unauthorized retrieval of forms and table data between scopes.
-   **[Restrict delegated developers read access \[Updated in Security Center 1.3\]](sc-delegated-developers-read-access-allowlist.md)**  
If **com.glide.dd\_allow\_global\_access\_tables** does not contain the recommended value of wf\_activity, wf\_activity\_definition, wf\_workflow, wf\_workflow\_version, sp\_portal, sp\_widget, and sp\_page, then those tables could be read by a delegated developer. This could provide the delegated developer read access to sensitive information.
-   **[Disable inbound emails for locked out users](sc-disable-inbound-emails-locked-out-users.md)**  
Use the **glide.pop3.process\_locked\_out** property to control inbound email actions for locked out, active users.
-   **[Display recommendations for high risk UI pages](sc-display-recommendations-for-high-risk-ui-pages.md)**  
Decrease the likelihood of authorization errors, and unintended information disclosure by displaying recommendations for high risk UI pages.
-   **[Double check inbound transactions \[Updated in Security Center 1.3\]](sc-double-check-inbound-transactions.md)**  
Use the **glide.security.strict.updates** property to enable double-checking of security on inbound transactions during form submission. When you set this property to **true**, it adds an extra layer of table validation before a form renders in the browser.
-   **[Enable ACLs to Control Live Profile Details \[Updated in Security Center 1.3\]](sc-enable-acls-to-control-live-profile-details.md)**  
Use the **glide.live\_profile.details** property to designate whether a user should be able to view all detail fields, such as company name and phone numbers, in a live profile.
-   **[Enable ACLs for Encoded Query in Simple List Widget \[New in Security Center 2.0\]](sc-enable-acls-for-encoded-query-in-simple-list-widget.md)**  
Learn how to set the **glide.service\_portal.enable\_acls\_for\_encoded\_query\_in\_list** property to the secure value to prevent users from bypassing access control list \(ACL\) evaluations on a query condition in the Simple List Widget.
-   **[Enable URL allowlist for cross-origin iframe communication](sc-enable-url-allowlist-for-cross-origin-iframe-communication.md)**  
Use the **glide.ui.concourse.onmessage\_enforce\_same\_origin** property to enable cross-origin communication between `iframes`.
-   **[Enforce application scope restrictions \[New in Security Center 1.3 and removed in 1.5\]](sc-enforce-application-scope-restrictions.md)**  
Use the **glide.record.legacy\_cross\_scope\_access\_policy\_in\_script** property to control the permissions of scoped apps.
-   **[Enforce security rules to sharing dashboards \[New in Security Center 1.3\]](sc-enforce-security-rules-to-sharing-dashboards.md)**  
Use the **glide.cms.dashboards.sharing\_with\_secure\_search** property to control whether users can share dashboards.
-   **[Enforce scope security for public sector digital services \[New in Security Center 1.3\]](sc-enforce-scope-security-for-public-sector-digital-services.md)**  
Use the **glide.enforce\_security\_scope.sn\_gsm** property to control how the application data from the Public Sector Digital Services application is accessed.
-   **[Enforce scoped ACL access for information request playbooks \[New in Security Center 1.3 and updated in 1.5\]](sc-enforce-scoped-acl-access-for-information-request-playbooks.md)**  
Use the **glide.enforce\_security\_scope.sn\_gsm\_info\_req** property to control access to playbook data for the Information Request playbooks feature.
-   **[Enforce strict elevate privilege \[New in Security Center 1.3\]](sc-enforce-strict-elevate-privilege.md)**  
Use the **glide.security.strict\_elevate\_privilege** property to control whether roles marked as privileged must be manually elevated for the user to be granted the role's capabilities.
-   **[Require AJAXGlideRecord ACL checking \[Updated in Security Center 1.3\]](sc-enabling-ajaxgliderecord-acl-checking.md)**  
Use the **glide.script.secure.ajaxgliderecord** property to perform access control rule \(ACL\) validation when server-side records, such as tables, are accessed using GlideAjax APIs within a client script.
-   **[Enforce field level ACLs in GlideRecordSandbox](sc-enforce-field-level-acls-in-gliderecordsandbox.md)**  
Manage field level ACLs in GlideRecordSandbox on your instance.
-   **[Enforce GroupBy ACLs](sc-enforce-groupby-acls.md)**  
Configure your instance to conduct ACL checks on groupby columns.
-   **[Ensure dashboards creation/deletion requires access check \[New in Security Center 1.3 and updated in 2.0\]](sc-ensure-dashboards-creation-deletion-requires-access-check.md)**  
The **glide.processors.check\_access\_before\_process** property enables access control list \(ACL\) enforcement for creating or deleting dashboards when a user is logged in.
-   **[Enforce oauth state parameter validation](sc-enforce-oauth-state-parameter-validation.md)**  
Configure the **glide.oauth.state.parameter.required** property to prevent your instance from cross-site request forgery \(CSRF\) attacks.
-   **[Enforce Strict User Image Upload](sc-enforce-strict-user-image-upload.md)**  
Use the **glide.security.strict.user\_image\_upload** property to enable Access Control for the upload/update of a profile picture when performed on a user record.
-   **[Exclude Sensitive Tables and Fields from Data Generation](sc-exclude-sensitive-tables-and-fields-from-data-generation.md)**  
Use system properties to exclude tables and fields from Data Generation, which is used to generate fake data sets based on existing data. Tables and fields that are added to these exclusion lists can't be used for Data Generation feature.
-   **[Restrict email domains for external user registration \[Updated in Security Center 1.3, 1.5, and 2.0\]](sc-external-user-registration-email-domain-allowlist.md)**  
Use the **sn\_ext\_usr\_reg.allowed\_email\_domains** property to list acceptable external email domains.
-   **[Enable High Security Plugin \[Updated in Security Center 1.3\]](sc-high-security-plugin.md)**  
When you activate the High Security plugin, it creates or updates hundreds of different configurations to control the level of security on your instance. These configurations mitigate many of the top OWASP attacks by enabling strict access control, input validation, and output encoding.
-   **[Honor Admin Override ACLs](sc-honor-admin-override-acls.md)**  
The **glide.security.admin.override.accessterm** property controls admins to be unable to override ACL evaluation even where the override should be in effect.
-   **[Prevent inactive users from logging in \[New in Security Center 1.5\]](sc-prevent-inactive-users-from-logging-in.md)**  
Configure this property to control if inactive users can authenticate on your instance.
-   **[Prevent Unauthenticated Access to Virtual Agent Embedded Web Client](sc-publicly-exposed-virtual-agent-embedded-web-client.md)**  
Learn how to configure the **sn\_va\_web\_client\_app\_embed** table to block unauthenticated users from accessing embedded web clients.
-   **[Restrict JSONP requests to trusted URLs \[Updated in Security Center 1.3\]](sc-jsonp-request-inclusion-list.md)**  
Specify trusted URLs for the AngularJS $http service to allow or reject JSONP requests.
-   **[Disable raw database query execution \[Updated in Security Center 1.3 and removed in 2.0\]](sc-operation-level-access-control-requirements.md)**  
Control whether a user can perform raw SQL queries on the database.
-   **[Hide user comments on articles \[New in Security Center 1.3\]](sc-hide-user-comments-on-articles.md)**  
Use the **glide.knowman.show\_user\_feedback** property to control whether feedback comments are visible.
-   **[Require authentication by default for client-callable script includes \[Updated in Security Center 1.3\]](sc-privacy-on-client-callable-script-includes.md)**  
By default, client-callable script includes that do not explicitly set visibility, are public. If needed, add the **glide.script.ccsi.ispublic** property to enable privacy control over all client-callable script includes accessed by public pages.
-   **[Enforce production instance behavior \[Updated in Security Center 1.3 and 1.5\]](sc-production-instance-behavior.md)**  
Configure whether your instance should be handled like a production or non-production instance.
-   **[Restrict access to background script \[Updated in Security Center 1.3 and 2.0\]](sc-restrict-access-to-background-script.md)**  
Configure the **glide.script\_processor.admin** property to set the role required for accessing the Script Background module.
-   **[Restrict access to emails with empty target table](sc-restrict-access-to-emails-with-empty-target-table.md)**  
Activate the **glide.email.email\_with\_no\_target\_visible\_to\_all** property to restrict user access to emails, unless they were the one who sent the email or have an admin role.
-   **[Restrict access to specific IP ranges plugin \[Updated in Security Center 1.3\]](sc-restrict-access-to-specific-ip-ranges-plugin.md)**  
Use the **com.snc.ipauthenticator** plugin to restrict access to specific IP ranges. Unless public access is intended for the instance, administrators should limit access to their assigned IP net blocks.
-   **[Restrict knowledge bases access \[New in Security Center 1.3\]](sc-restrict-knowledge-bases-access.md)**  
The **glide.knowman.block\_access\_with\_no\_user\_criteria** property is used to control the read/write access of users on knowledge based articles.
-   **[Restrict permissions for CMDB model \[Updated in Security Center 1.3 and 1.5\]](sc-restrict-permissions-cmdb-model.md)**  
Use the **csm\_cmdb\_model.customer\_visible\_flag** system property to limit customer access to data in the Product Models table as an additional access control to the CMDB model.
-   **[Restrict unauthenticated access to attachments](sc-restrict-unauthenticated-access-attachments.md)**  
Use the **glide.image\_provider.security\_enabled** property to control the security settings for images. If set to **true**, images are visible only to authenticated and authorized users. If set to **false**, images are visible to anyone with a URL to the attachment.
-   **[Restrict access to custom journal entries \[Updated in Security Center 1.3 and removed in 2.0\]](sc-secure-custom-journal-entries.md)**  
Use the **glide.live\_feed.custom\_journal.acl\_check\_enabled** property to respect ACL's on custom journal fields.
-   **[Restrict flow context read access \[New in Security Center 1.5\]](sc-restrict-flow-context-read-access.md)**  
Use the **com.snc.process\_flow.reporting.require\_flow\_access** property to enforce if an additional access check is required for a user to read a flow check.
-   **[Restrict Impersonation to Admin \[New in Security Center 2.0\]](sc-restrict-impersonation-to-admin.md)**  
The **glide.sys.permissive.impersonate** property can be used to prevent non-admin roles from impersonating other users.
-   **[Enable security jump start plugin \(ACL Rules\) \[Updated in Security Center 1.3\]](sc-security-jump-start-plugin-acl-rules.md)**  
Activate the Security Jump Start \(ACL Rules\) \(com.snc.system\_security**com.snc.system\_security**\) plugin to create several important ACLs that validate the Access Controls on some of the key system tables within the ServiceNow AI Platform.
-   **[Use of secure insert multiple operation within import set API \[New in Security Center 1.3\]](sc-use-of-secure-insert-multiple-operation-within-import-set-api.md)**  
Use the **com.glide.import\_set\_api.insert\_multiple\_optimize** property to control whether GlideRecordSecure or GlideRecord is used for the Insert Multiple operation within the Import Set API.
-   **[Enforce SOAP request strict security \[Updated in Security Center 1.3\]](sc-soap-request-strict-security.md)**  
Use the **glide.soap.strict\_security** property to enforces web service security.
-   **[Required jms connection factories \[New in Security Center 1.3 and updated in 1.5 and 2.0\]](sc-required-jms-connection-factories-plugin-applicability-mid-server.md)**  
The **mid.property.jms.command.allowed\_factory\_names** property controls the Java Messaging Service \(JMS\) connection factories that the MID Server can use.
-   **[Restrict Global App Development by Role \[New in Security Center 2.0\]](sc-restrict-global-app-development-by-role.md)**  
Use the **sn\_g\_app\_creator.allow\_global** property to control which users can create applications in the global scope using the Guided Application Creator.
-   **[Review extraneous explicit role access control conditions \[Removed in Security Center 1.5\]](sc-review-extraneous-explicit-role-access-control-conditions.md)**  
The Explicit Roles plugin is recommended to mandate that all users have either the snc\_internal role to access internal resources, or the snc\_external role to access external resources.
-   **[Set guest user for soap requests \[Updated in Security Center 1.3 and 2.0\]](sc-set-guest-user-for-soap-requests.md)**  
Configure this property to control the level of access of unauthenticated SOAP requests.
-   **[Disable public access to favorites \[Updated in Security Center 1.3 and 2.0\]](../../security/reference/public-access-favorites.md)**  
Use the **glide.ui.magellan.favorites.allow\_public** to specify whether unauthenticated users are allowed to see **Favorites** in the navigator.
-   **[Enable SNC access control plugin \[Updated in Security Center 1.3\]](sc-snc-access-control-plugin.md)**  
Activate the SNC Access Control \(com.snc.snc\_access\_control\) plugin to control access to your instances by Customer Service and Support personnel.
-   **[Prevent users from accepting warning to bypass CSRF validation](sc-prevent-users-from-accepting-warning-to-bypass-csrf-validation.md)**  
Reduce the risk of Cross-Site Request Forgery \(CSRF\) by preventing users from accepting warning to bypass CSRF validation.
-   **[Prevent impersonating user from viewing application data](sc-prevent-impersonating-user-from-viewing-application-data.md)**  
Use system properties to prevent an impersonating user from viewing application data.

**Parent Topic:**[Hardening settings](security-hardening-settings.md)

