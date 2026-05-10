---
title: Domain separation in CMDB Health
description: This is an overview of domain separation as it pertains to CMDB Health. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Reference, CMDB Health, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Domain separation in CMDB Health

This is an overview of domain separation as it pertains to CMDB Health. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Overview of domain separation in CMDB Health



CMDB dashboards should be set up with their own set of rules to best accommodate how the user needs them. CMDB dashboard jobs adhere to those rules to produce reports. These are covered in separate sections below.

## How domain separation works in CMDB Health

For dashboards to be the most effective, users should configure the dashboard accordingly. This is done by setting up the orphan, staleness, and inclusion rules to meet their needs, which then affect the reports displayed on the dashboard.

The settings and metrics define different aspects of each application because each domain can be configured differently. These rules are set up in addition to those that are included in the base system. There are different types of owners for different CIs; each domain has its own set of rules.

Metric tests from the global domain propagate to subdomains. However, subdomains can have their own local metric tests which override the global domain tests. Up until the San Diego release, subdomain local metric tests were applied to the subdomain CIs and also to the global domain CIs \(which are visible on subdomains\). Global domain CIs that failed metric tests of local subdomains, could have generated large amounts of data due to duplicated data.

Starting with the Tokyo release, CIs in the global domain are evaluated only against metric tests specified in the global domain. In subdomains, local metric tests are applied only to the CIs in that subdomain and are not applied to the global domain CIs \(even though the global domain CIs are visible in the subdomain\). Health results for CIs in the global domain appear on subdomains and health results on subdomains reflect this new behavior.

**Note:** Domain separation is on by default, but each domain can be configured as needed.

## Health Preferences

Configure these preferences during setup:

1.  Global system properties that control CMDB Health – System properties are not domain separated. To learn more see [CMDB Health system properties](../reference/r_CMDBHealthProperties.md).
2.  [CMDB Health Dashboard Jobs](../task/t_EnableCMDBHealthDashboardJob.md) – There is a dashboard job for each major KPI, such as Completeness. That job finds the health of the CIs across all the enabled domains. There is only one job run for all domains and jobs themselves are not domain separated.

    Users can define the frequency with which they want to run jobs; the report runs for all the domains. The more domains included in the job, the longer the job runs.

3.  Health Metrics – These selections are domain-separated and adhere to the established “system overrides” logic of domain separation. Changes are made according to the domain for which the user is logged in. Base system values are defined at the global domain. The overriding domain logic means these values apply for all domains. If users want different values for a domain, they must be logged in to a specific domain and change the property from there. The new property setting applies only to that domain and any domain that inherits this domain. To learn more, see [Health Metrics](../task/t_ConfigureCMDBHealthMetrics.md).

    **Note:** Regarding the Completeness, Compliance, and Correctness KPIs: Users can disable this KPI if they don’t want to see that as part of the dashboard score. All these settings are domain-separated and the user can define specific properties for the domain.

    1.  Active – This setting is the most important because it affects how long the jobs run. The more domains with flags set to **Active**, the longer the jobs take. It’s best to select only those domains you wish to be **Active** and render the rest as **Active** = **false**. You can set this in Health Preferences. The default settings for global domain are **Active** = **true**, but you can modify or disable specific domains the user wants to see in the dashboard. Users should consider the domain hierarchy when changing these values. If there is a large number of domains \(&gt;100\) the job can take a very long time. To mitigate this, set **Active** to **false** for all the root domains, thereby disabling all the other domains in the hierarchy. If there is a rule at the top, all child domains inherit that rule.
    2.  **Failure Threshold**, **Create Task**, **Task Assignee Group** – All these settings can be set differently for different domains depending on what is needed in each domain.
    3.  Exceptions – For Relationship metrics \(relationship, duplicate relations, orphan relations, stale relations\) the failure threshold setting is not domain separated. The Failure Threshold for the global domain is applied to all domains. For example, even if users were to override the Failure Threshold for a domain, the global domain setting for Threshold is still applied.
    4.  Troubleshooting / Implementation detail – These settings are stored in the **cmdb\_health\_metric\_pref** table, which is domain separated.

## CMDB Health-related rules

See CMDB Health-related rules settings at:

-   [Required](../task/t_SetCIFieldMandatory.md)
-   [Recommended](../task/t_MakingAFieldRecommended.md)
-   [Orphan](../task/t_CreateCMDBHealthOrphanRule.md)
-   [Staleness](../task/t_CreateCMDBHealthStaleRule.md)

Most of the CMDB Health-related rules are domain separated and provided by the users. Users can define different rules for different domains by logging in to each domain and adding/overriding rules in the CI Class Manager.

1.  Completeness
    1.  Required fields – These are based on the class schema defined in the platform’s [System dictionary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_SystemDictionary.md) and is fixed for all domains. These cannot be changed.
    2.  Recommended fields – These are domain separated. The table used is CMDB Recommended Fields \[cmdb\_recommended\_fields\], which is domain separated. The user can set these up for different domains.
2.  Correctness
    1.  Duplicates – Duplicates are based on Identification rules, which are not domain separated, so the same rules apply to all domains.
    2.  Orphan – Orphan rules are domain separated; there are different orphan rules for different domains. The table used in the CMDB Health Orphan Rule \[cmdb\_health\_orphan\_rule\] table and is domain separated.
    3.  Staleness – Staleness rules are domain separated. The table used is cmdb\_health\_staleness\_rule. The base system rule \(60 days\) is set for global domain so is inherited by all domains as the default rule.
3.  Compliance

    Audit – Audit scores are based on the desired state or scripted audits defined in the compliance module by the user.Audits themselves are domain separated. When audit score evaluation is enabled for a domain, scores become based only on the audits visible in that domain.


Health inclusion rules:

-   Health inclusion rules are domain separated. The rules are stored in the cmdb\_health\_config table which is domain separated.
-   Each domain can have its specific health inclusion rules and domain-specific rules for each sub-metric.
-   When a health inclusion rule is defined globally, all sub-domains inherit the rule according to the domain structure and the rule can be overridden at any domain.
-   When a health inclusion rule is defined at the Configuration Item \[cmdb\_ci\] class level, all descending classes inherit the rule and the rule can be overridden at any class level.

## CMDB Health Dashboard

If the Domain Support — Domain Extensions Installer plugin is activated, then the CMDB Health Dashboard is domain aware:

-   The CMDB Health Dashboard aggregates and reports health failures and scores based on user’s domain visibility of CIs. If domain visibility lets a user see a CI, then the audit rule in that user’s domain applies to that CI, whether the CI is in the user's domain or in a contained domain. If a CI fails health tests from different user domains, then separate failure records are created.
-   Users can configure KPI and metric settings specific to the needs in their domain. So different domains can have different settings such as active/inactive, and thresholds.
-   A child domain derives its immediate parent's domain health configurations if the child domain does not configure its own. A child domain can override parent's configurations by modifying them.

## Health Dashboards \(Class View/Service View/Health Group View\)

In general, CMDB Health dashboards are domain aware and show data according to the logged-on domain user. If a user is logged into a domain and views a health dashboard:

1.  Only scores for enabled metrics in that domain display \(based on the Health Preferences **Active** flag as discussed above\).
2.  All scores are based on CIs that are visible from the specific domain. \(These are regular domain visibility rules: From that domain you can see CIs in global domain, the specific domain, any child domain of that domain or any domain that gets directly or indirectly contained by that domain.\)
3.  The dashboard view is based on domain rules defined in domain mapping, as opposed to those provided by the logged-in user. This view overrides any additional domain visibility rules that a logged-in user might have. The admin sets the basic rules, but does not set each individual domain. The admin can give specific users or user groups additional visibility to other domains and the dashboard still does not change. The dashboard strictly follows the domain rules mentioned above, based on the domain hierarchy for the domain in which the user is logged in.
4.  As explained in the Health Preferences section, users can define different preference values for any domain which impact the scores reported in the dashboard. Preferences that can impact scores include **Failure Threshold** and **Active**.
5.  As explained in the CMDB Health Rules section, the scores reported for the metrics are based on the health rules defined for them \(staleness, orphan, recommended, audit, and inclusion rules\) which can be defined differently for a specific domain \(in the CI Class Manager\). Only the required metric and duplicate metric are based on rules that apply in all domains.
6.  Service View/ Group View – These reports also largely follow the above points. Typically, these views differ from various views/filters for the Health Report. One is based off business rules, the other is based off CMDB Health groups.

**Parent Topic:**[CMDB Health reference](cmdb-health-ref-parent.md)

**Related topics**  


[Domain separation and Configuration Management Database \(CMDB\)](domain-separation-cmdb.md)

