---
title: Combined Access Management release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Access Management from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-accessmanagement-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 4
breadcrumb: [Products combined by family]
---

# Combined Access Management release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Access Management from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Access Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Access Management to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Access Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Access Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Query ACLs](https://www.servicenow.com/docs/access?context=query-acl-rule&family=australia&ft:locale=en-US)**

Query ACLs now load automatically during plugin installation for most platform plugins. These preconfigured ACLs reduce the need to run the QueryRangeACLAuditor tool to generate query ACLs. Store app query ACLs aren't included in preconfigured query ACLs. For more information about preconfigured query ACLs, see the [Maintenance Information \[KB2046494\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2046494) article in the Now Support Knowledge Base.Existing custom query ACLs are preserved and loaded as inactive. To view inactive ACLs, use this command: `<INSTANCE_URL>/sys_security_acl_list.do?[query_parameters]`QueryRangeACLAuditor tool modifications are preserved.

-   **[ACL types](https://www.servicenow.com/docs/access?context=acl-rule-types&family=australia&ft:locale=en-US)**

Core field and datatype ACLs are replaced with more comprehensive rules to optimize ACL volume.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Explore Access Control Lists](https://www.servicenow.com/docs/access?context=exploring-access-control-list&family=brazil&ft:locale=en-US)**

Improve access control predictability by enforcing strict denial when none of the referenced roles referenced in an ACL exist on the instance. This behavior doesn't apply to ACLs that have a mix of valid and invalid roles. This behavior is on by default for new instances. If you upgraded to this release, use the **glide.security.acl\_with\_invalid\_roles\_strict\_deny** property to turn it on. Navigate to **All** &gt; **Access Management** &gt; **Access Findings** to find these ACLs in the Access Checks list.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Access Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Access Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

-   **Activation information**

Access Management is a ServiceNow AI Platform feature that is active by default.


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Access Management is a ServiceNow AI Platform feature that is active by default.


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Access Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Accessibility information**

Coral is the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme uses brand-neutral illustrations. A dark theme option is available for web and mobile experiences.


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Access Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

Early Availability

-   Use ServiceNow® Access Analyzer v6.1, a self-service tool designed for AI administrators or creators to validate the access controls configured within agentic assets \(agentic workflows and AI agents\).
-   Use new preconfigured query ACLs for most platform plugins, as part of ongoing security risk mitigation. These base system ACLs significantly reduce the need to run the QueryRangeACLAuditor tool.
-   Use Access Findings, the proactive detection and remediation layer within Access Management Console, to run eight base system access checks against your instance on a daily schedule. This surfaces prioritized findings when misconfigurations are detected, and provides a complete remediation workflow including AI-powered guidance.

 See [Access Control Lists \(ACLs\)](https://www.servicenow.com/docs/access?context=access-control-rules&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Validate access controls configured within various resources and agentic assets with Access Analyzer.
-   Improve your security posture by ensuring that access to applications and data is granted on a least privilege basis with Zero Trust Access.
-   Use Access Findings, the proactive detection and remediation layer within Access Management Console, to run base system access checks against your instance on a daily schedule.
-   Restrict access to data by requiring users to pass a set of requirements before they can interact with it by using ACLs.
-   Control which Customer Service and Support employees can access your instance, and when, using the SNC Access Control plugin \(com.snc.snc\_access\_control\).

 See [Access Management](https://www.servicenow.com/docs/access?context=access-management-landing&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

