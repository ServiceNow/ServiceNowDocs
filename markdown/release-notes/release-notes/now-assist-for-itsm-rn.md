---
title: Now Assist for IT Service Management \(ITSM\) release notes
description: The ServiceNow Now Assist for IT Service Management \(ITSM\) application brings agentic AI to IT Service Management. Now Assist for IT Service Management \(ITSM\) was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
---

# Now Assist for IT Service Management \(ITSM\) release notes

The ServiceNow® Now Assist for IT Service Management \(ITSM\) application brings agentic AI to IT Service Management. Now Assist for IT Service Management \(ITSM\) was enhanced and updated in the Australia release.

## Now Assist for IT Service Management \(ITSM\) highlights for the Australia release

[Australia Patch 2](../quality/australia-patch-2.md)

-   Track which knowledge articles and catalog items support successful virtual agent deflections instead of transferring to human agents using the ITSM Virtual Agent Analytics dashboard.
-   Use the ITSM MCP server to query and retrieve any information within the context of an incident.

[Australia Patch 1](../quality/australia-patch-1.md)

-   Answer incident-related questions with context-aware agents using the incident assist agentic workflow.
-   Submit a catalog item for an account unlock using the voice AI agent.
-   Generate summaries and responses for Request Management records.
-   Use the Knowledge Article Advanced Editor page to create and edit articles.
-   Use the ITSM Conversational Analytics dashboard that provides usage adoption performance metrics in Now Assist in Virtual Agent.

See [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US) for more information.

**Important:** Now Assist for IT Service Management \(ITSM\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist for IT Service Management \(ITSM\) to Australia

To use the Knowledge Article Advanced Editor page in the generate a knowledge article skill, you must activate the knowledge content recommendation skill. Follow these steps to activate the skill.

1.  Go to **Admin** &gt; **Now Assist admin**.
2.  Select **Now Assist Skills**.
3.  Select **Platform**.
4.  Select **Knowledge**.
5.  Make sure the knowledge content recommendation skill is active.

The incident assist agentic workflow is active by default and includes all the capabilities of the \[DEPRECATED\] incident assist skill, with enhancements. When you upgrade to [Australia Patch 1](../quality/australia-patch-1.md), if you have the \[DEPRECATED\] incident assist skill activated, consider deactivating it to avoid redundancy. For more information, see [Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

Starting with the [Australia Patch 2](../quality/australia-patch-2.md), the Incident assist skill has been deprecated, moved to the **Archive** section, and is no longer available for use.

## New in the Australia release

-   **[ITSM Virtual Agent resources analytics](https://www.servicenow.com/docs/access?context=now-assist-itsm-conversational-dashboard-resources&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    Identify which knowledge article or catalog item resources support successful deflections and which ones are unable in preventing the transfer to a live agent using the **Resources** tab in the ITSM Virtual Agent dashboard to gain visibility into the ITSM Virtual Agent usage and effectiveness.

-   **[ITSM MCP server](https://www.servicenow.com/docs/access?context=now-assist-itsm-mcp-server&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    Retrieve and modify incident details, search similar incidents, or lookup users and assignment groups by connecting the ITSM MCP server to any AI-enabled MCP client, such as Moveworks, or Claude.


-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[ITSM Virtual Agent resources analytics](https://www.servicenow.com/docs/access?context=now-assist-itsm-conversational-dashboard-resources&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    Identify which knowledge article or catalog item resources support successful deflections and which ones are unable in preventing the transfer to a live agent using the **Resources** tab in the ITSM Virtual Agent dashboard to gain visibility into the ITSM Virtual Agent usage and effectiveness.

-   **[Incident assist agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist-workflow&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    Answer incident-related questions using context-aware agents. Handle queries about incident details and get information about related records.

-   **[Enhancements to the Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    The features in the \[DEPRECATED\] incident assist skill are available in the incident assist agentic workflow. You may turn off this skill and use the agentic workflow that has enhanced capabilities.

-   **[Creating a catalog item for unlocking accounts using the voice AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    Use the Submit account unlock catalog with the voice AI agent, which is a primer, to create a catalog item to unlock the specified account when a user calls the help desk.

-   **[Enhancements to Troubleshoot Outlook issue with voice AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    Email relevant troubleshooting articles and instructions to users when you troubleshoot Outlook issues for them.

-   **[Knowledge Article Advanced Editor page](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-SOW-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    Use the new Knowledge Article Advanced Editor page to create or edit Knowledge articles using open prompts.

-   **[ITSM Conversational analytics dashboard](https://www.servicenow.com/docs/access?context=using-itsm-conversational-analytics-dashboard&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    Get insights into virtual agent adoption, usage trends, and track metrics in Now Assist in Virtual Agent.

-   **[Getting summary of an incident in the Details tab](https://www.servicenow.com/docs/access?context=summarize-incident-now-assist&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    Resolve incidents faster by getting the incident summary in the **Details** tab of the incident.

-   **[Configure summaries and responses for Request Management records](https://www.servicenow.com/docs/access?context=cust-now-assist-request-summarization-skill&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    As an admin, you can configure the following Request Management skills:

    -   Request summarization
    -   Requested item summarization
    -   Catalog task summarization
    -   Request activity response generation
    -   Requested item activity response generation
    -   Catalog task activity response generation
-   **[Summarize Request Management records](https://www.servicenow.com/docs/access?context=summarize-request-related-skill&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    View an aggregate of all relevant updates and progress indicators in a single, dynamic summary.

-   **[Generate a response to request activity](https://www.servicenow.com/docs/access?context=summarize-request-related-activity-response-generation&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    Generate a response in record activity streams of requests, requested items, and catalog tasks.

-   **[DEX issue diagnosis and resolution agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-dex-diagnosis-resolution-workflow&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    Service desk agents can diagnose and resolve Zoom call quality issues using the Digital End-User Experience \(DEX\) issue diagnosis and resolution agentic workflow, which integrates Zoom- specific diagnostics that correlate device, network, and application data.

-   **[AI-powered root cause analysis for Zoom call quality issues](https://www.servicenow.com/docs/access?context=investigate-and-resolve-zoom-call-issues&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    Use Now Assist for Zoom call issues to identify the root cause of call quality degradation and review the supporting metric evidence for deeper insight. The analysis highlights the contributing device and network factors directly in the Zoom call quality view. Get the real-time guidance, including device ready remedial actions, contextual self-help instructions, and relevant Knowledge articles to help resolve the issue efficiently.

-   **[Get AI driven insights for boot time performance](https://www.servicenow.com/docs/access?context=investigate-and-resolve-boot-time-issues&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    Monitor device boot time to identify slow start-up issues and use Now Assist to investigate the root cause and get suggested resolutions, including remedial actions, self-help instructions, and Knowledge articles to resolve boot performance problems quickly.


## Changed in this release

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Renaming the Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    The incident assist skill has been renamed to **\[DEPRECATED\] Incident assist**.

-   **[Renaming demo voice AI agents](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    The voice AI demo agents have been renamed as primers.

-   **[Skills activated by default in Now Assist for ITSM](https://www.servicenow.com/docs/access?context=using-now-assist-for-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    For new Now Assist for IT Service Management \(ITSM\) users, the following skills are activated by default:

    -   Resolution notes generation
    -   Knowledge generation
    -   Chat reply recommendation
-   **[Editing change request skills using Now Assist Skill Kit \(NASK\)](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    Easily edit the change request risk explanation and change request summarization skill prompts and inputs directly in the Now Assist Skill Kit \(NASK\).

-   **[Configuration item details for suggest configuration items for a change request workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-suggest-configuration-items-for-a-change-request&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    Provide details such as class, location, and environment to find configuration items \(CIs\) relevant to a change request while using the suggest configuration items for a change request agentic workflow from the Now Assist panel.

-   **[Role masking for change risk explanation skill](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    Enhance security for the change request risk explanation skill by enabling admins to limit roles that are inherited by the user.

-   **[Virtual agent topics available as demo data](https://www.servicenow.com/docs/access?context=itsm-va-prebuilt-topics&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    The Virtual Agent topics listed in this table have been renamed and are now available as demo data.

    |Existing name|Updated name|
    |-------------|------------|
    |Add Comment To incident|\(DEMO\) Add Comment To incident-LLM|
    |Approve Sysapproval Approver|\(DEMO\) Approve Sysapproval Approver-LLM|
    |Change Password|\(DEMO\) Change Password \(Template\) - LLM|
    |Check IT Ticket Status|\(DEMO\) Check IT Ticket Status \(Template\)|
    |Close incident|\(DEMO\) Close incident-LLM|
    |Explain change risk|\(DEMO\) Explain change risk|
    |Mark incident Unresolved|\(DEMO\) Mark incident Unresolved-LLM|
    |Open IT Ticket|\(DEMO\) Open IT Ticket \(Template\)-LLM|
    |Reject Sysapproval Approver|\(DEMO\) Reject Sysapproval Approver-LLM|
    |Reset Password|\(DEMO\) Reset Password \(Template\) - LLM|
    |Resolve incident|\(DEMO\) Resolve incident-LLM|
    |Unlock Account|\(DEMO\) Unlock Account \(Template\) - LLM|
    |View And Add Comments|\(DEMO\) View And Add Comments-LLM|


## Deprecated features

Starting with the [Australia Patch 2](../quality/australia-patch-2.md) release, the [Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&version=australia&pubname=australia-it-service-management&ft:locale=en-US) is deprecated, moved to the **Archived** folder and is no longer available for use.

## Activation information

Install Now Assist for IT Service Management \(ITSM\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console for quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    Use this conversational interface in ServiceNow® Service Operations Workspace to summarize a chat, an incident, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    Use the ServiceNow® Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

