---
title: Security jump-start - ACL rules plugin
description: The Security jump-start access control level \(ACL Rules\) plugin is installed automatically on all new instances. Use this plugin to quickly secure multiple system tables and expedite the production launch process for your organization.
locale: en-US
release: yokohama
product: Access Control
classification: access-control
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Exploring Access Control Lists, Access Control List Rules, Access Management]
---

# Security jump-start - ACL rules plugin

The Security jump-start access control level \(ACL Rules\) plugin is installed automatically on all new instances. Use this plugin to quickly secure multiple system tables and expedite the production launch process for your organization.

This plugin isn’t intended for existing instances, as it may alter security access to tables already in use in a production environment. If an admin strongly desires to install this plugin on an existing instance, you should test it thoroughly in a test instance first. Doing so helps to verify compatibility with the organization's current implementation.

If an admin is interested in the new ACL rules provided by this plugin, they can manually create one or more in an existing instance, using the list of ACLs as a guideline.

The following ACLs are included in this plugin. Select the icon in a header row to sort that column in ascending or descending order. The Operation key is as follows:

-   R=read
-   W=write
-   D=delete
-   C=create

|Name|Operation|Description|
|----|---------|-----------|
|`cmdb_ci`|WCD|asset or itil role required to write/create/delete Configuration Item records|
|`cmn_department`|WD|user\_admin role required to write/delete Department records|
|`cmn_location`|WC|user\_admin role required to write/create Location records|
|`core_company`|WD|user\_admin role required to write/delete Company records|
|`kb_knowledge`|create|knowledge role required to create Knowledge records|
|`ldap_ou_config`|RWCD|user\_admin role required to read/write/create/delete LDAP OU Definition records|
|`ldap_server_config`|RWCD|user\_admin role required to read/write/create/delete LDAP Server records|
|`process_guide`|WCD|admin role required to write/create/delete Process Guide records|
|`process_step`|WCD|admin role required to write/create/delete Process Step records|
|`sc_category`|create|catalog\_admin role required to create Service Catalog Category records|
|`sc_category`|delete|catalog\_admin role required to delete Service Catalog Category records|
|`sc_category`|write|catalog\_admin role required to write to Service Catalog Category records|
|`sc_cat_item`|write|catalog\_admin role required to write to Catalog Item records|
|`sc_cat_item`|delete|catalog\_admin role required to delete Catalog Item records|
|`sc_cat_item`|create|catalog\_admin role required to create Catalog Item records|
|`sysevent_email_action`|read|all users can read Email Notification records \(for subscription purposes\)|
|`sysevent_register`|RWCD|admin role required to read/write/create/delete Event Registry records|
|`sysevent_script_action`|RWCD|admin role required to read/write/create/delete Script Action records|
|`syslog`|RWCD|admin required to read/write/create/delete Log Entry records|
|`sysrule`|RWCD|admin required to read/write/create/delete Rule records \(Email Notifications, Inbound Email Actions, Approval Rules, and so on\)|
|`sysrule`|read|all users can read Email Notification records for \(subscription-based notifications\)|
|`sys_app_application`|WCD|admin required to write/create/delete Application records|
|`sys_app_category`|WCD|admin role required to write/create/delete Application Category records|
|`sys_app_module`|WCD|admin required to write/create/delete Module records|
|`sys_audit`|RWCD|admin required to read/write/create/delete Audit records|
|`sys_dictionary`|RWC|personalize\_dictionary role required to read/write/create Dictionary records|
|`sys_dictionary`.\*|read|personalize\_dictionary role can read Dictionary fields|
|`sys_documentation`|delete|personalize\_dictionary role required to delete Field Label records|
|`sys_documentation`|create|personalize\_dictionary role required to create Field Label records|
|`sys_documentation`|write|personalize\_dictionary role required to write to Field Label records|
|`sys_gauge`|RWCD|admin role required to read/write/create/delete Gauge records|
|`sys_gauge_count`|RWCD|admin role required to read/write/create/delete Gauge Count records|
|`sys_group_has_role`|read|itil role required to see Group Role records|
|`sys_home`|WCD|itil\_admin role required to write/create/delete Welcome Page Section records|
|`sys_installation_exit`|WCD|admin role required to write/create/delete Installation Exit records|
|`sys_job`|WCD|admin role required to write/create/delete Sys Job records|
|`sys_nav_link`|WCD|admin role required to write/create/delete Navigation Link records|
|`sys_perspective`|WCD|admin role required to write/create/delete Menu List records|
|`sys_portal`|RWCD|admin role required to read/write/create/delete Portal records|
|`sys_portal_page`|RWCD|admin role required to read/write/create/delete Homepage records|
|`sys_portal_preferences`|RWCD|admin role required to read/write/create/delete Portal Preferences records|
|`sys_processor`|WC|admin role required to write/create Processor records|
|`sys_properties`|WC|admin role required to write/create System Property records|
|`sys_properties_category`|WCD|admin role required to write/create/delete Property Category records|
|`sys_report`|delete|roles that can delete Report records \(doesn’t restrict deleting through Report UI\)|
|`sys_report`|write|roles that can write to Report records \(doesn’t restrict editing through Report UI\)|
|`sys_report`|read|users can read their own Report records, those of their groups, and GLOBAL ones \(doesn’t affect viewing through Report UI\)|
|`sys_report`|read|roles that can read Report records \(doesn’t restrict viewing through Report UI\)|
|`sys_reportroles`|read|admin role required to read Report Roles records|
|`sys_script`|WCD|admin role required to write/create/delete Business Rule records|
|`sys_script_ajax`|WCD|admin role required to write/create/delete AJAX Script records|
|`sys_script_client`|WCD|admin role required to write/create/delete Client Script records|
|`sys_script_include`|WCD|admin role required to write/create/delete Script Include records|
|`sys_security_acl`|write|admin role required to write to Access Control records|
|sys\_security\_acl\_role|create|admin role required to create Access Roles records|
|`sys_security_acl_role`|delete|admin role required to delete Access Roles records|
|`sys_security_acl_role`|write|admin role required to write to Access Roles records|
|`sys_security_operation`|delete|admin role required to delete Security Operation records|
|`sys_security_operation`|create|admin role required to create Security Operation records|
|`sys_security_operation`|write|admin role required to write to Security Operation records|
|`sys_security_operation`|query\_range| |
|`sys_security_operation`| | |
|`sys_security_type`|write|admin role required to write to Security Type records|
|`sys_security_type`|create|admin role required to create Security Type records|
|`sys_security_type`|delete|admin role required to delete Security Type records|
|`sys_status`|create|admin role required to create System Status records|
|`sys_status`|delete|admin role required to delete System Status records|
|`sys_status`|write|admin role required to write to System Status records|
|`sys_template`|write|template\_editor role required to write to Template records|
|`sys_template`|create|emplate\_editor role required to create Template records|
|`sys_template`|delete|template\_editor role required to delete Template records|
|`sys_template`|read|template\_editor role required to read Template Roles records|
|`sys_ui_action`|create|admin role required to create UI action records|
|`sys_ui_action`|delete|admin role required to delete UI action records|
|`sys_ui_action`|write|admin role required to write to UI action records|
|`sys_ui_action_view`|write|admin role required to write to UI View Action records|
|`sys_ui_action_view`|create|admin role required to create UI View Action records|
|`sys_ui_action_view`|delete|admin role required to delete UI View Action records|
|`sys_ui_policy`|create|admin role required to create UI Policy records|
|`sys_ui_policy`|delete|admin role required to delete UI Policy records|
|`sys_ui_policy`|write|admin role required to write to UI Policy records|
|`sys_ui_policy_action`|create|admin role required to create UI Policy Action records|
|`sys_ui_policy_action`|delete|admin role required to delete UI Policy Action records|
|`sys_ui_policy_action`|write|admin role required to write to UI Policy Action records|
|`sys_ui_script`|write|admin role required to write to UI Script records|
|`sys_ui_script`|delete|admin role required to delete UI Script records|
|`sys_ui_script`|create|admin role required to create UI Script records|
|`sys_user`|write|Users with no role can’t update any user record but their own|
|`sys_user_grmember`|delete|user\_admin role required to delete Group Member records|
|`sys_user_grmember`|write|user\_admin role required to write to Group Member records|
|`sys_user_group`|create|Only itil and above can create group records|
|`sys_user_group`|write|Only itil and above can write to group records|
|`sys_user_has_role`|read|itil role required to see User Role records|
|`sys_user_role`|create|admin role required to create Role records|
|`sys_user_role`|delete|admin role required to delete Role records|
|`sys_user_role`|write|admin role required to write to Role records|
|`sys_user_role_contains`|read|itil role required to see Contained Role records|
|`sys_user_role_contains`|write|admin role required to write to Contained Role records|
|`sys_user_token`|RWCD|admin role required to read/write/create/delete User Token records|

**Note:** To learn more about this plugin, see [Enable security jump start plugin \(ACL Rules\) \[Updated in Security Center 1.3\]](../../security-center/reference/sc-security-jump-start-plugin-acl-rules.md) in Instance Security Hardening Settings.

