---
title: Legacy: Landing page filter configuration
description: You can add new filters or modify existing filters that appear in the Security Analyst Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/sir-new-ui-setup-landpage.html
release: brazil
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Legacy: Additional Security Analyst Workspace configuration, Legacy: Configure the Security Analyst Workspace, Install and configure Security Incident Response, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Legacy: Landing page filter configuration

You can add new filters or modify existing filters that appear in the Security Analyst Workspace.

**Important:**

The Security Incident Response UI \[sn\_app\_secops\_ui\] is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Use the [Security Incident Response Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/security-incident-response/sir-workspace-landing-page.md) instead.

The Security Analyst Workspace has primary and secondary filters that allow you to filter the list of security incidents so you can quickly find the security incidents you want to analyze. Fore more information, see [Legacy: Manage security threats using the Security Analyst Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/security-incident-response/sir-new-ui.md).

\[Omitted image "sir-new-ui-setup-main.png"\] Alt text: Security Analyst Workspace: Filters

## Create a new filter

1.  Navigate to **Security Incidents** &gt; **Analyst Workspace Setup \(New UI\)** &gt; **Landing Page Filter Configuration**.
2.  Click **New**.
3.  Enter a title for the filter, specify the filter condition and click **Submit** to return to the previous page.

    You will see the newly added filter listed on the page.

4.  Add a tag for this filter to indicate whether this is a primary or secondary filter. The following tags are available:
    -   SN\_SI\_Primary
    -   SN\_SI\_Secondary

## Edit existing filters

You can also do the following:

-   Modify existing filters: Click the Title of an existing filter. Modify the title and the filter condition and click **Update**.
-   Modify tags: Select a filter and click the Tag column in the Landing Page Filter Configuration. You can delete the existing tag or add a new tag for the filter.

