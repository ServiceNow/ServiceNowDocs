---
title: Now Assist for Third-party Risk Management \(TPRM\) release notes
description: The ServiceNow Now Assist for TPRM application brings generative AI to Third-party Risk Management. Now Assist for Third-party Risk Management \(TPRM\) is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-11-07"
reading_time_minutes: 4
---

# Now Assist for Third-party Risk Management \(TPRM\) release notes

The ServiceNow® Now Assist for TPRM application brings generative AI to Third-party Risk Management. Now Assist for Third-party Risk Management \(TPRM\) is a new application in the Zurich release.

## Now Assist for Third-party Risk Management \(TPRM\) highlights for the Zurich release

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Use generative AI to recommend TPRM issues for reviewer validation.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Use Now Assist for Third-party Risk Management \(TPRM\) to generate concise, AI-powered summaries of TPRM that can help with interpreting complex issue records.
-   Some Now Assist skills, agents, and agentic workflows are now turned on by default.

See [Now Assist for Third-party Risk Management \(TPRM\)](https://www.servicenow.com/docs/access?context=now-assist-tprm&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Now Assist for TPRM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Now Assist for Third-party Risk Management \(TPRM\)](https://www.servicenow.com/docs/access?context=now-assist-tprm&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)[Generate issue recommendations for TPRM](https://www.servicenow.com/docs/access?context=create-recommendation-tprm-issue&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    If you have the third‑party assessment reviewer role \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] and have installed the if you have the third‑party assessment reviewer role \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] and have installed the Now Assist for Third-party Risk Management \(TPRM\), you can use generative AI to automatically identify and recommend issues based on assessment responses. The TPRM issue management recommendation skill recommends issues with rationalized summaries. Recommended issues are presented for review and are created as standard TPRM issues only after user confirmation.


-   **[Now Assist for Third-party Risk Management \(TPRM\)](https://www.servicenow.com/docs/access?context=now-assist-tprm&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role and have installed the Now Assist for Third-party Risk Management \(TPRM\) for TPRM application, you can use generative AI to automatically summarize complex issue records. The TPRM Issue Summarization skill works across all issue states including New, Analyze, Review, Finalize, and Closed and can help reduce manual review time, improve consistency in issue descriptions and remediation guidance, and accelerate triage and reporting for customers managing high volumes of third-party risk data.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## Activation information

Install the Now Assist for TPRM application by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

After installing Now Assist for TPRM all Now Assist for TPRM skills are activated by default.

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console for access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[AI Agent Studio](https://www.servicenow.com/docs/access?context=ai-agent-studio&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use AI Agent Studio to create, manage, or test AI agents and agentic workflows so that you can create self-executing workflows to help you achieve your business goals.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist panel conversational interface in ServiceNow® Software Asset Workspace to interact with and get assistance from generative AI.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the ServiceNow® Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.

-   **[Third-party Risk Management](https://www.servicenow.com/docs/access?context=third-party-risk-mgt-landing-page&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The ServiceNow® GRC: Third-party Risk Management \(TPRM\) application enables you to proactively identify, assess, and mitigate risks that are associated with your third-party relationships. TPRM provides a centralized process for managing your portfolio of third parties, assessing and scoring risk, and performing remediation.


**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

