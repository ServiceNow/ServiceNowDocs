---
title: Combined AI Admin Hub release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for AI Admin Hub from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-aiadminhub-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined AI Admin Hub release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for AI Admin Hub from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family AI Admin Hub release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading AI Admin Hub to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **Upgrade information**

If you customized actions on the user interface or other items that are associated with ServiceNow Otto skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions might not work as expected.

If you run into issues when you're upgrading a ServiceNow Otto product, see the [Issues and mitigation for Now Assist \(generative AI\) Applications and Plugin updates \[KB1637452\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) article in the Now Support Knowledge Base. Log in to view the article.

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform. These changes include a new read\_only\_option field with granular control levels, including strict\_read\_only and client\_script\_modifiable. The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen instance security while preserving flexibility. If you have custom client scripts that modify read‑only fields using `g_form.setValue()` or `g_form.clearValue()`, refer to the [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) article in the Now Support Knowledge Base to identify affected fields and adjust the settings.

The existing access control lists \(ACLs\) have been updated to replace the admin role with purpose-driven granular roles within scripts or security attributes. As part of this update, the `getRoles()` API is replaced with the `hasRole()` API for authorization purposes. Additionally, all references to the admin role in the code have been substituted with the granular roles for authorization use cases. For more information, see [Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for AI Admin Hub.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[New system properties for the Now Assist Readiness Evaluation app](https://www.servicenow.com/docs/access?context=nare-sys-props&family=zurich&ft:locale=en-US)**
    -   Reduce performance issues when a large volume of data is assessed with the **sn\_assess.assessment\_limit** system property.
    -   Customize the estimated remediation effort for select efforts with the **sn\_assess.effort\_visibility** system property. Setting this system property to `true` turns on the **Remediation properties** tab in the Now Assist Readiness Evaluation dashboard.
    -   Decide the maximum number of records to process for the ITSM assessment with the **sn\_assess.task\_limit** system property.

</td></tr><tr><td>

Australia

</td><td>

-   **[Using the approval assistance AI agent](https://www.servicenow.com/docs/access?context=platform-approval-aia&family=australia&ft:locale=en-US)**

ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Platform Approval Assistance AI agent. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

-   **[Using the request status AI agent](https://www.servicenow.com/docs/access?context=ticket-status-aia&family=australia&ft:locale=en-US)**

ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Platform Request status AI agent. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

-   **[ServiceNow Otto panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=australia&ft:locale=en-US)**

Enable streaming responses and unified surface operations to deliver faster, more reliable ServiceNow Otto® interactions. Support both synchronous and asynchronous workflows while maintaining compatibility with various LLM providers.

-   **[AI skill details](https://www.servicenow.com/docs/access?context=now-assist-skill-details&family=australia&ft:locale=en-US)**

Map multiple skills under subsections and display all applicable products per common skill with distinct visual tags. A visual indicator will mark skills as common, based on schema data.

-   **[Install plugins for ServiceNow Otto](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&family=australia&ft:locale=en-US)**

Control default activation of skills configured for auto-activating when installed or updated. Review the skills active by default and, activate or deactivate them individually.

-   **[Usage alerts](https://www.servicenow.com/docs/access?context=usage-alerts&family=australia&ft:locale=en-US)**

Establish limit-based alert rules at the skill level to oversee assist consumption and skill execution counts. This solution seeks to prevent resource exhaustion, and offer clear insights via an alerts feed and rule management interface.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing AI Admin Hub features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**

Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Use](https://www.servicenow.com/docs/access?context=using-now-assist-readiness-evaluation&family=zurich&ft:locale=en-US)**
    -   View the updated legend that now includes None-XXL estimated remediation efforts along with assessment icon explanations.
    -   Understand estimated remediation efforts more clearly now that blocker areas are included in the estimated remediation efforts and non-blocker observations are not included in estimated remediation efforts.
    -   Select any widget on the Agentic AI- Assessment dashboard and Now Assist assessment dashboard tabs to open that widget's data table in a separate tab.

</td></tr><tr><td>

Australia

</td><td>

-   **[Conversational Help](https://www.servicenow.com/docs/access?context=conversational-help-skills&family=australia&ft:locale=en-US)**

The discovery of Conversational Help Skills from the Now Assist panel is no longer configured as auto-enabled.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some AI Admin Hub features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some AI Admin Hub features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   In Patch 5, the **Select Use Case** drop-down menu was removed from the Agentic AI - ITSM tab.

</td></tr><tr><td>

Australia

</td><td>

-   Starting with the [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US) release, Conversational Help Skills is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate AI Admin Hub.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**
    -   **[Skills](https://www.servicenow.com/docs/access?context=now-assist-skills&family=australia&ft:locale=en-US)**

Now Assist features are available with activation of any Now Assist plugin from [https://www.servicenow.com/docs/access?context=external.sn-app-store&amp;family=australia&amp;ft:locale=en-US](https://www.servicenow.com/docs/access?context=external.sn-app-store&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for AI Admin Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **Additional requirements**

The Next Experience UI Framework must be enabled before you can use the Now Assist panel.


</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for AI Admin Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **Browser requirements**

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Internet Explorer.


</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for AI Admin Hub, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for AI Admin Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **Localization information**

Now Assist supports Dynamic Translation for Australia.


</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for AI Admin Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)

-   AI Admin Hub is the new AI experience brand. This change is reflected in the name of ServiceNow products. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

 [Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   AI Guardian is enabled by default and detects prompt injection attempts and offensive content without manual activation.
-   Configure prompt injection detection separately for each Now Assist skill.
-   Create knowledge articles from Now Assist using files stored in Box.
-   Improve the clarity and accessibility of your articles with the AI-powered prompt Reading Ease scan.

 -   **[Merge duplicate articles](https://www.servicenow.com/docs/access?context=merge-duplicate-articles&family=australia&ft:locale=en-US)**

Merge selected duplicate knowledge articles into a new consolidated article using Now Assist in Knowledge Management. The merge preserves references to source articles and helps maintain a clean, high‑quality knowledge base.


</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

