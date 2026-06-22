---
title: Combined Access Management release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Access Management from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-accessmanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Access Management release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Access Management from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Access Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Access Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Access Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Security data filters](https://www.servicenow.com/docs/access?context=security-data-filters&family=yokohama&ft:locale=en-US)**

Security data Filters enable you to control who can access sensitive data by restricting access to authorized users, regardless of how the data is accessed. Security data filters are applied before query execution, ensuring restricted data never leaves the database and prevents data leakage at the query level. Filters integrate into queries for GlideRecordSecure, GlideRecordSandbox, and GlideAggregateSandbox by default.

-   **[Related record access](https://www.servicenow.com/docs/access?context=related-record-access&family=yokohama&ft:locale=en-US)**

Related record access integrated into the ACL framework enhances access management by enabling administrators to enforce specific ACLs for related tables. This ensures users can only access records in related tables, such as costs, estimations, or tasks, based on their permissions for the parent table, like projects or cases. Combined with broader ACL capabilities, Related record access ensures consistent, granular, and enforceable


</td></tr><tr><td>

Zurich

</td><td>

-   **[Machine identity access controls](https://www.servicenow.com/docs/access?context=machine-identity-access-controls&family=zurich&ft:locale=en-US)**

Enforce fine-grained access to data via REST or SOAP endpoints using Machine Identity Access Controls. This feature enables you to define which integrations can access specific data, confirming that the integrations only have access to the resources they need.

-   **[Scripting Governance Tool](https://www.servicenow.com/docs/access?context=scripting-governance&family=zurich&ft:locale=en-US) tool and role**

Review and help reduce the number of users with scripting privileges using the Scripting Governance Tool. This tool helps improve platform security with scripting governance based on user role.

A new deny-by-default behavior is enforced for scripting unless you have the snc\_required\_script\_writer\_permission role. After an upgrade or zBoot, this role is automatically assigned via the Conditional Script Writer group.

-   **[Datatype ACL](https://www.servicenow.com/docs/access?context=datatype-acl&family=zurich&ft:locale=en-US)**

Simplify and help reduce redundant ACL definitions with Datatype ACLs. Create a single ACL to target all table columns of a specific data type, streamlining access control configurations.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Access Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Deny-Unless condition for ACLs](https://www.servicenow.com/docs/access?context=acl-denial-behavior&family=xanadu&ft:locale=en-US)**

A new decision type field helps administrators define the conditions that give or deny users access to data. It enables more granular decision-making while defining the right access strategy on the platform.

-   **[Enhanced ACL Security](https://www.servicenow.com/docs/access?context=acl-denial-behavior&family=xanadu&ft:locale=en-US)**

If an ACL is misconfigured or empty, you can deny access to data by default, enhancing the overall security of the platform.

-   **[ACL Query Behavior](https://www.servicenow.com/docs/access?context=r_SecurityJumpStartACLRules&family=xanadu&ft:locale=en-US)**

Fine-tune your access control by dictating rules for querying data with the introduction of new operators: query match and query range.

-   **&gt;[Explicit Roles behavior adjustment](https://www.servicenow.com/docs/access?context=explicit-roles&family=xanadu&ft:locale=en-US)**

When the system property `glide.security.explicit_roles.do_not_fix` is true, the **snc\_internal** role is no longer added in memory or to the User Roles \[sys\_user\_has\_role\] table.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **[Query ACLs](https://www.servicenow.com/docs/access?context=query-acl-rule&family=australia&ft:locale=en-US)**

Query ACLs now load automatically during plugin installation for most platform plugins. These preconfigured ACLs reduce the need to run the QueryRangeACLAuditor tool to generate query ACLs. Store app query ACLs aren't included in preconfigured query ACLs. For more information about preconfigured query ACLs, see the [Maintenance Information \[KB2046494\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2046494) article in the Now Support Knowledge Base.

Existing custom query ACLs are preserved and loaded as inactive. To view inactive ACLs, use this command: `<INSTANCE_URL>/sys_security_acl_list.do?[query_parameters]`

QueryRangeACLAuditor tool modifications are preserved.

-   **[ACL rule types](https://www.servicenow.com/docs/access?context=acl-rule-types&family=australia&ft:locale=en-US)**

Core field and datatype ACLs are replaced with more comprehensive rules to optimize ACL volume.


-   **[Access Analyzer](https://www.servicenow.com/docs/access?context=access-analyzer&family=australia&ft:locale=en-US)**

Use ServiceNow® Access Analyzer v6.1, a tool designed for AI administrators or creators to validate the access controls configured within agentic assets \(agentic workflows and AI agents\) on the ServiceNow AI Platform.

**Important:** Access Analyzer is available in the ServiceNow Store. For more information, visit [ServiceNow Store](https://store.servicenow.com/store).


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Access Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Access Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Access Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Access Management is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Yokohama

</td><td>

Access Management is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Zurich

</td><td>

Access Management is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Australia

</td><td>

Access Management is a ServiceNow AI Platform feature that is active by default.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Access Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Access Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Access Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Access Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Access Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Fine-tune your access control with the new Deny-Unless ACL and query operators.
-   Enhance ACL security with a new default denial behavior.
-   Identify and fix empty or misconfigured ACLs with new ACL creation rules.

 See [Access Control List Rules](https://www.servicenow.com/docs/access?context=access-control-rules&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Security Data Filters are a powerful new feature designed to restrict access to sensitive records based on roles or security attributes. This ensures only authorized users can view data, regardless of how the data is accessed.
-   Related Record Access allows enforcement of consistent access rules across related tables, ensuring that users only see records associated with the data they are authorized to access.

 See [Access Control List Rules](https://www.servicenow.com/docs/access?context=access-control-rules&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Enforce access to data via REST or SOAP endpoints using the Machine Identity Access Controls, which helps improve security, governance, and auditability.
-   Target all table columns of a given data type with a single ACL using Datatype ACLs.
-   Govern scripting permissions with the Scripting Governance tool, a new base system deny-by-default behavior.

 See [Access Control List Rules](https://www.servicenow.com/docs/access?context=access-control-rules&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

Early Availability

-   Use ServiceNow® Access Analyzer v6.1, a self-service tool designed for AI administrators or creators to validate the access controls configured within agentic assets \(agentic workflows and AI agents\).
-   Use new preconfigured query ACLs for most platform plugins, as part of ongoing security risk mitigation. These base system ACLs significantly reduce the need to run the QueryRangeACLAuditor tool.
-   Use Access Findings, the proactive detection and remediation layer within Access Management Console, to run eight base system access checks against your instance on a daily schedule. This surfaces prioritized findings when misconfigurations are detected, and provides a complete remediation workflow including AI-powered guidance.

 See [Access Control List Rules](https://www.servicenow.com/docs/access?context=access-control-rules&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

