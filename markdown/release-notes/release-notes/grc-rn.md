---
title: Common Core release notes
description: The ServiceNow Integrated Risk Management \(IRM\) application enables your organization to continue to provide its business services during adverse operational events, such as a pandemic, extreme weather, or hacking. Integrated Risk Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
---

# Common Core release notes

The ServiceNow® Integrated Risk Management \(IRM\) application enables your organization to continue to provide its business services during adverse operational events, such as a pandemic, extreme weather, or hacking. Integrated Risk Management was enhanced and updated in the Yokohama release.

## IRM highlights for the Yokohama release

-   Generate a GRC issue action plan by using the agentic AI workflow.
-   Segregate data by entities and granular access management when using entity-based access.
-   Summarize an issue by using generative AI to provide quicker context gathering and contextual awareness. With this feature, you can improve the efficiency and productivity of your analysts on GRC issues.
-   Use the enhanced GRC licensing summary dashboard to understand the licensing treatment for users that are added to the group by roles that are mapped or assigned to the group.
-   Select a user record on the licensing summary dashboard and select the role hierarchy to see all the parent roles that are assigned to the user and their role hierarchies.
-   Monitor the email activity from the Overview page for regulatory agencies.
-   Update and add content by using Microsoft 365 for ServiceNow Reporting, which is now integrated with the Document designer application.
-   Add up to 20 columns in a table and in a content block by using the Document designer application.
-   Select and reorder columns by using the Document designer Microsoft Word add-in while creating templates.

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Some Now Assist skills are now turned on by default.
-   Review changes to Now Assist usage measurements.

For detailed documentation, see [Common Governance, Risk, and Compliance features](https://www.servicenow.com/docs/access?context=common-grc-features&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US).

**Important:** IRM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Entity Based Access](https://www.servicenow.com/docs/access?context=entity-based-access&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Implement data segregation and detailed access management so that users can access only the permitted data through entity-based access. Administrators can grant access to an entity's related records by adding users or user groups or by using entity user fields for entity-based access configuration. You can enhance your data security and minimize the risk of unnecessary data exposure while ensuring that only authorized users can access an entity's related records.

-   **[Gen AI issue summarization](https://www.servicenow.com/docs/access?context=generate-grc-issue-resolution&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Optimize the GRC issue resolution agentic AI workflow in the Integrated Risk Management application to help your issue managers and analysts resolve GRC issues with AI agents in the Now Assist panel. This workflow makes the issue resolution process more efficient by introducing targeted solutions for key steps in the issue management life cycle.

-   **[Gen AI issue summarization](https://www.servicenow.com/docs/access?context=now-assist-for-irm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Summarize an issue by using the Now Assist for IRM application to provide quicker context gathering and contextual awareness. You can quickly analyze the issue records, including the description, activity log, and remediation tasks, and then generate a concise summary that provides you with a concise context of the issue to help you resolve it. Check your entitlements to determine whether you have access to issue summarization.

-   **[Searching user groups to understand the licensing treatment](https://www.servicenow.com/docs/access?context=grc-licensing-summary-dashboard&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Use the enhanced GRC licensing summary dashboard to understand the licensing treatment of users that are added to the group by roles that are mapped or assigned to the group.

-   **[Overview of an agency record](https://www.servicenow.com/docs/access?context=regulatory-agency-library-rcm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    View the pie charts that depict the total number of emails that are sent to the various regulatory domains. On the overview page of a regulatory agency, you can view the domains where the maximum number of emails were sent and access the Emails Tracker page directly from an agency record. You can also filter and display only the relevant emails that were sent to a specific agency.

-   **[Document designer integration](https://www.servicenow.com/docs/access?context=configuring-audit-word-based-templates&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Update and add content by using Microsoft 365 for ServiceNow Reporting, which is now integrated with the Document designer application. You can insert data and reports into a Microsoft Word document.


## UI changes

-   **[Create data relationships](https://www.servicenow.com/docs/access?context=create-data-relationships&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The **Data Relationship** tab has been added to the template configuration record as part of the configuration process for the Document designer Microsoft Word add-in.


## Changed in this release

-   **[Column Organization](https://www.servicenow.com/docs/access?context=create-an-audit-report-template&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    You can select and reorder columns when adding a table into your template by using the Document designer Microsoft Word add-in. You can now organize your content better to meet your reporting needs.

-   **[Create content configurations](https://www.servicenow.com/docs/access?context=create-content-configurations&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    You can add up to 20 columns in a table and content block by using the Document designer application. You now have more flexibility with customizing your table and content block to meet your reporting needs.


-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## Deprecations

The template data relationship table has been removed and deprecated for the Document designer application.

## Activation information

Install Integrated Risk Management and Now Assist for IRM by requesting them from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

