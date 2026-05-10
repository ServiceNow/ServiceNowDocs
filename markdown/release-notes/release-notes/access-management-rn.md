---
title: Access Management release notes
description: The ServiceNow Access Management application provides robust tools to manage security data on the ServiceNow AI Platform. Access Management includes many controls, such as Access Control Lists \(ACLs\), Security Attributes, Security Data Filters, and Machine Identity Access Control. These controls provide granular control and help improve security for managing data access. Access Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Access Management release notes

The ServiceNow® Access Management application provides robust tools to manage security data on the ServiceNow AI Platform. Access Management includes many controls, such as Access Control Lists \(ACLs\), Security Attributes, Security Data Filters, and Machine Identity Access Control. These controls provide granular control and help improve security for managing data access. Access Management was enhanced and updated in the Australia release.

## Access Management highlights for the Australia release

Early Availability

-   Use ServiceNow® Access Analyzer v6.1, a self-service tool designed for AI administrators or creators to validate the access controls configured within agentic assets \(agentic workflows and AI agents\).
-   Use new preconfigured query ACLs for most platform plugins, as part of ongoing security risk mitigation. These base system ACLs significantly reduce the need to run the QueryRangeACLAuditor tool.
-   Access Findings is the proactive detection and remediation layer within Access Management Console. It runs eight out-of-box access checks against your instance on a daily schedule, surfaces prioritized findings when misconfigurations are detected, and provides a complete remediation workflow including AI-powered guidance.


See [Access Control List Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/access-control-rules.md) for more information.

## Changed in this release

-   **[Query ACLs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/query-acl-rule.md)**

    Query ACLs now load automatically during plugin installation for most platform plugins. These preconfigured ACLs reduce the need to run the QueryRangeACLAuditor tool to generate query ACLs. Store app query ACLs aren't included in preconfigured query ACLs. For more information about preconfigured query ACLs, see the [Maintenance Information \[KB2046494\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2046494) article in the Now Support Knowledge Base.

    Existing custom query ACLs are preserved and loaded as inactive. To view inactive ACLs, use this command: `<INSTANCE_URL>/sys_security_acl_list.do?[query_parameters]`

    QueryRangeACLAuditor tool modifications are preserved.

-   **[ACL rule types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/acl-rule-types.md)**

    Core field and datatype ACLs are replaced with more comprehensive rules to optimize ACL volume.


-   **[Access Analyzer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/access-analyzer.md)**

    Use ServiceNow® Access Analyzer v6.1, a tool designed for AI administrators or creators to validate the access controls configured within agentic assets \(agentic workflows and AI agents\) on the ServiceNow AI Platform.

    **Important:** Access Analyzer is available in the ServiceNow Store. For more information, visit [ServiceNow Store](https://store.servicenow.com/store).


## Activation information

Access Management is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)

