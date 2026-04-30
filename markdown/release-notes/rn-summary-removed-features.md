---
title: Removed features and products in Zurich
description: Cumulative release notes summary on features that were removed from Zurich features and products.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 3
breadcrumb: [Release notes summaries for Zurich features, Release notes for upgrading from Yokohama, Learn about the Zurich release, Zurich release notes]
---

# Removed features and products in Zurich

Cumulative release notes summary on features that were removed from Zurich features and products.

Some features were removed as part of Zurich product updates.

<table id="rn-summary-removed-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Advanced Risk

</td><td>

To enhance the Risk Workspace home page load performance and reduce latency, the **Tasks** widget has been removed from the home page.

</td></tr><tr><td>

Alumni Center

</td><td>

The following system properties are removed and the existing configured values are copied to the alumni common configuration UI.

-   Email property - sn\_asc.self\_registration.personal.email.domains
-   Deleted properties - sn\_asc.import.default.state, sn\_asc.import.user\_name.max.tries, sn\_asc.import.alumni.suffix

</td></tr><tr><td>

Classic Workflow

</td><td>

-   Removed the legacy workflows created and published by ServiceNow, Inc. for new customers who start on the Zurich release.
-   Retained the legacy workflows created and published by ServiceNow, Inc. for customers who upgraded from versions prior to the Zurich release.

</td></tr><tr><td>

Configurable Workspace

</td><td>

-   The List, List - Simple, and List - Related components are no longer available in UI Builder are replaced by the Record List component bundle.
-   The Condition Builder component is no longer available in UI Builder and is replaced by the Predicate Builder component for all list types.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   Common Service Data Model no longer provides **Design** as a value for the **Operational status** attribute in CIs.

</td></tr><tr><td>

Digital End-User Experience

</td><td>

-   Removed the **Impacted users** and **Active users** cards from the landing page.
-   Removed the **Users** page.
-   Removed the **Users list** page.
-   Removed the **Users** and **Devices** filters from the **Devices** page.

</td></tr><tr><td>

Document Intelligence

</td><td>

The Document Intelligence application has been removed from the application navigator.

</td></tr><tr><td>

Impact

</td><td>

The Jumpstart Your Document Intelligence Accelerator has been removed.

</td></tr><tr><td>

Instance Data Replication

</td><td>

-   The Key Management Service test has been removed from the IDR Diagnostics page.
-   The VAULT Service Status test has been removed from the IDR Diagnostics page.

</td></tr><tr><td>

Now Assist for Creator

</td><td>

[Zurich Patch 6](../quality/zurich-patch-6.md)

-   Spoke generation has been removed from Now Assist for Creator. See the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website for additional information.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Starting with version 28.4.3 of Now Assist for Creator, the now.assist.creator role has been removed as a required role for using most Now Assist for Creator skills and agents. Some skills and agents might have additional role requirements. See the [Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) product documentation for more information.

</td></tr><tr><td>

Now Assist in Document Intelligence

</td><td>

-   The Document extraction skill has been removed from the list of Platform skills in the Now Assist Admin console.
-   The Document Q&amp;A skill has been removed from the list of Platform skills in the Now Assist Admin console.

</td></tr><tr><td>

Operational Technology Manager

</td><td>

-   The **New** button was removed from the following related lists for users with read-only access to a site:
    -   Network Adapters
    -   Memory Modules
    -   Software Installed
    -   IP Addresses

</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

-   The **glide.script.use.sandbox** system property has been removed. The script sandbox is enabled by default.
-   Dynamic groups have been removed. Instead, use dynamic attributes in dynamic categories to simplify administration and improve the dynamic schema user experience.

</td></tr><tr><td>

ServiceNow SDK

</td><td>

-   The `now-sdk upgrade` command has been removed. To upgrade the version of the ServiceNow SDK, see [Upgrade the ServiceNow SDK](https://www.servicenow.com/docs/access?context=upgrade-servicenow-sdk&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

</td></tr><tr><td>

Skills Foundation

</td><td>

-   The LinkedIn Parsing capability is not supported because it is based on ML models.
-   The skills ontology, which contained skill structure with categories and definition, is no longer provided. Supply your own skills data and import it into the Skills Foundation application.
-   Legacy Data Science algorithms from Talent Development applications.

</td></tr><tr><td>

Upgrade Console

</td><td>

-   Removed the Ready your environment step in the pre-upgrade activities on a production instance.

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Zurich features](../release-notes-summaries.md)

