---
title: Now Assist for Collaborative Work Management release notes
description: The ServiceNow Now Assist for Collaborative Work Management \(CWM\) application uses generative AI skills to improve time to value for the tasks you perform in the CWM workspace. Now Assist for CWM is a new application in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-04-09"
reading_time_minutes: 3
---

# Now Assist for Collaborative Work Management release notes

The ServiceNow® Now Assist for Collaborative Work Management \(CWM\) application uses generative AI skills to improve time to value for the tasks you perform in the CWM workspace. Now Assist for CWM is a new application in the Yokohama release.

## Now Assist for Collaborative Work Management highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Help increase efficiency by automatically creating tasks from the context of your CWM Docs and adding them to the required Board.
-   Enable saving time by summarizing and paraphrasing blocks of content or a whole page in CWM Docs using generative AI capabilities.

See [Now Assist for Collaborative Work Management \(CWM\)](https://www.servicenow.com/docs/access?context=now-assist-for-cwm-landing&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) for more information.

**Important:** Now Assist for Collaborative Work Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Now Assist for Collaborative Work Management features

-   **[Generate tasks from Docs in Collaborative Work Management \(CWM\)](https://www.servicenow.com/docs/access?context=generate-tasks-cwm-docs-now-assist&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Help increase efficiency and save time by using Now Assist to automatically generate CWM Tasks for your Board. Using the information in your doc, Now Assist provides task recommendations. You can choose to refine or modify these recommendations. You can iterate multiple times to tweak the task recommendations according to your requirements.

    After you're satisfied with the recommendations, Now Assist can help you add these tasks to a board of your choice.

-   **[Summarize and paraphrase Docs content](https://www.servicenow.com/docs/access?context=cwm-docs&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US#section_ucs_wn1_hdc)**

    Use Now Assist capabilities to refine selected content in docs, or to get a summary of the whole document.

    -   Summarize, elaborate, or shorten selected text.
    -   Summarize the entire content on the page.

## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


## Activation information

Install Now Assist for Collaborative Work Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Collaborative Work Management](https://www.servicenow.com/docs/access?context=cwm-landing&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Collaborative Work Management \(CWM\) provides a central hub to plan, visualize, manage, and collaborate on work with your teams.

    The Now Assist for CWM application uses generative AI skills to save time and improve efficiency for the actions that you perform within the CWM workspace.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

**Parent Topic:**[Strategic Portfolio Management release notes](it-business-management-rn-landing.md)

