---
title: Now Assist for IT Operations Management \(ITOM\) release notes
description: The ServiceNow Now Assist for ITOM application brings generative AI to IT Operations Management. You can access alert simplifications created by Now Assist using generative AI in both Service Operations Workspace and Express List.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-10-08"
reading_time_minutes: 4
keywords: [release notes, Now Assist for ITOM, Express List]
---

# Now Assist for IT Operations Management \(ITOM\) release notes

The ServiceNow® Now Assist for ITOM application brings generative AI to IT Operations Management. You can access alert simplifications created by Now Assist using generative AI in both Service Operations Workspace and Express List.

## Now Assist for ITOM highlights for the Xanadu release

Xanadu Patch 10

-   Get deeper impact analysis in the Analyze alert impact agentic workflow with five new AI agents.
-   Enhance security for Now Assist AI agents with Access Control Lists \(ACLs\).

Xanadu Patch 9

-   Investigate alerts and get the context that you need to respond efficiently using the Analyze alert impact agentic workflow.
-   Automatically perform initial alert triage and analysis tasks such as assigning alerts, analyzing alert history, and summarizing past incidents, with the Triage and analyze alert agentic workflow.

[Xanadu Patch 1](../quality/xanadu-patch-1.md)

-   Optimize alert resolution with Now Assist AI-driven investigation of past related incidents.
-   Generate an alert group description in Express List using Now Assist.
-   Launch an alert analysis from the Now Assist panel.

See [Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=now-assist-itom&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) for more information.

**Important:** Now Assist for ITOM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Configure the Dynatrace analysis AI agent](https://www.servicenow.com/docs/access?context=now-assist-itom-config-dynatrace&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Set up the Dynatrace analysis AI agent in the Analyze alert impact agentic workflow to investigate Dynatrace alerts. With Dynatrace, the agentic workflow now supports three observability tools, including Kentik and New Relic, helping you investigate and respond to a wider range of alerts.

-   **[Expand the Analyze alert impact agentic workflow with four new AIOps agents](https://www.servicenow.com/docs/access?context=now-assist-itom-use-aia&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Get a fuller view of alert impact with four new AIOps agents in the Analyze alert impact agentic workflow. Along with observability data, the agentic workflow now includes information from within ServiceNow to help surface business impact and related issues. Activate the AIOps agents to include them in the agentic workflow.

-   **[Add access control lists for security in AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Enable security settings to run AI agents and agentic workflows using ACLs and user identities. You can configure and manage the ACLs in AI Agent Studio.


-   **[Analyze alert impact agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itom-agentic-aia&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Analyze the impact of alerts and identify possible causes with the Analyze alert impact agentic workflow. The workflow interacts with observability tools, such as Kentik and New Relic, to surface alert details and provide insights.

-   **[Triage and analyze alerts agentic workflow](https://www.servicenow.com/docs/access?context=itom-alert-triage-agentic-workflow&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Automatically assign, acknowledge, and summarize alerts, determine significance through history analysis, and analyze related incidents. Initiate multiple parallel processes to triage and analyze different alerts.


[Xanadu Patch 1](../quality/xanadu-patch-1.md)

-   **[Speed up alert resolution with a Now Assist analysis of past related incidents](https://www.servicenow.com/docs/access?context=nai-past-incidents&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Enhance efficiency and reduce downtime with a Now Assist analysis of past incidents on the same or related CIs. Now Assist investigates historical data to identify past incidents related to the current alert and reports their frequency and criticality levels. It also provides a summary of effective strategies used to resolve them. In addition, Now Assist offers contact information for individuals or teams who have resolved similar incidents in the past and could assist when needed.

-   **[Generate an alert group description in Express List using Now Assist](https://www.servicenow.com/docs/access?context=alert-group-descr-generate-el&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Use Now Assist to generate a description of an alert group in Express List that encompasses all the alerts within the group. The generated description replaces the original description of the group.

-   **[Launch an alert analysis from the Now Assist panel](https://www.servicenow.com/docs/access?context=alert-analysis-now-assist-panel&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Analyze an alert from the Now Assist panel. The alert analysis displays directly in the Now Assist panel for convenient review.


## Removed in this release

-   Starting with version 2.0.1 of AI Agents for Observability, the sn\_obs\_aia.admin role, previously required to configure AI agents in the Analyze alert impact agentic workflow, has been removed. Users must now have the credential\_admin and connection\_admin roles instead.
-   Starting with version 2.0.1 of AI Agents for Observability, the prompt `How severe is this alert?` no longer appears in the Analyze alert impact agentic workflow.

## Activation information

Install Now Assist for ITOM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

Now Assist for ITOM is supported on Vancouver Patch 7 and later releases.

## Related ServiceNow applications and features

-   **[Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    The ServiceNow® Event Management application helps you identify health issues across the datacenter on a single management console. It provides alert aggregation and root cause analysis \(RCA\) for discovered services, application services, and automated alert groups.

-   **[Service Operations Workspace](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    ServiceNow® Service Operations Workspace is a configurable workspace that provides a unified experience for multiple IT Operations Management workflows.

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    ServiceNow® Now Assist uses generative AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    The Now Assist Admin console provides you with quick and easy access to the important information that you must set up, configure, and monitor Now Assist applications and features.


**Parent Topic:**[Now Assist release notes](../now-assist/now-assist-rn-landing.md)

