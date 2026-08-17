---
title: Ensure MID Server Users Have Appropriate Access Levels
description: Verify that your MID Server user accounts does not have more the necessary granted permissions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-ensure-mid-server-users-have-appropriate-access-levels.html
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-27"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Ensure MID Server Users Have Appropriate Access Levels

Verify that your MID Server user accounts does not have more the necessary granted permissions.

Granting the MID Server user account admin-level privileges \(such as admin, security\_admin or discovery\_admin\) violates the principle of least privilege and dramatically expands the attack surface.

Administrators sometimes grant elevated permissions to quickly resolve connectivity issues or enable integrations, but fail to remove them afterward. This leaves a service account with excessive access than necessary to perform its legitimate functions of facilitating communication between the ServiceNow instance and external systems within your network.

Review the User Roles \[sys\_user\_has\_role\] table for MID Server users and confirm that the following roles are not assigned:

```
access_analyzer_admin, activity_admin, actsub_admin, admin, advisor_admin, agent_security_admin, ai_user_admin, aig_admin,
ais_admin, all_high_security_admin, aisa_admin, alm_admin, analytics_categories_admin, analytics_filter_admin, analytics_task_admin,
announcement_admin, antivirus_admin, app_engine_admin, app_metadata_admin, app_template_admin, approval_admin, assessment_admin,
assignment_rule_admin, asset_admin, auth_factors_admin, backup_restore_admin, business_process_admin, business_rule_admin, canvas_admin,
catalog_admin, catalog_lookup_admin, certification_admin, change_admin, chart_admin, chat_admin, chat_analytics_admin, chat_survey_admin,
client_script_admin, clone_admin, clone_profile_admin, cmdb_consumer_admin, cmdb_dedup_admin, cmdb_import_admin, cmdb_inst_admin,
cmdb_ms_admin, cmdb_payload_admin, connection_admin, content_admin, core_ui_analytics_admin, cors_rule_admin, credential_admin,
currency_admin, currency_instance_admin, currency_instance_report_admin, customer_admin, data_classification_admin, data_destruction_admin,
data_manager_admin, data_policy_admin, decision_table_admin, df_connection_admin, discovery_admin, ecmdb_admin, email_access_notification_admin,
email_account_admin, email_client_admin, embedded_help_admin, evam_admin, export_set_admin, external_app_install_admin, fal_service_admin,
financial_mgmt_admin, form_admin, formula_admin, function_field_admin, graphql_schema_admin, guided_tour_admin, health_log_admin, hp_publisher_admin,
iam_security_admin, iar_admin, image_admin, import_admin, inbound_integration_metering_admin, integration_action_admin, inventory_admin, itil_admin,
itom_admin, kafka_admin, kafka_namespace_admin, knowledge_admin, live_feed_admin, megaphone_admin, metadata_admin, mi_admin, ml_admin,
mobile_analytics_admin, mobile_metadata_report_admin, ms_perm_no_extextend_admin, nlq_admin, nlu_admin
```

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

sys\_user\_has\_role.table, mid\_server\_user.role

</td></tr><tr><td>

Configuration type

</td><td>

User Roles \(/sys\_user\_has\_role.do\)

</td></tr><tr><td>

Data type

</td><td>

User Roles \[sys\_user\_has\_role\] record

</td></tr><tr><td>

Recommended value

</td><td>

mid\_server, and additional custom roles that may vary based on customer integrations

</td></tr><tr><td>

Default value

</td><td>

mid\_server

</td></tr><tr><td>

Fallback value

</td><td>

N/A

</td></tr><tr><td>

Category

</td><td>

[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.7
-   CVSS rating: Medium
-   Security risk details:

Granting the MID Server user account admin-level privileges represents a significant security vulnerability that violates the principle of least privilege and dramatically expands the attack surface. The MID Server acts as a bridge between trusted internal networks and the ServiceNow instance, processing credentials, executing discovery probes, and handling sensitive configuration data.

If a MID Server user account with excessive privileges is compromised, an attacker gains broad access to critical data across the entire ServiceNow instance. This could enable data exfiltration of sensitive CMDB information, manipulation of incident records, unauthorized access to customer data, or even privilege escalation to compromise additional systems.


</td></tr><tr><td>

Functional impact

</td><td>

MID Server is expected to run as intended without admin-level privileges.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

