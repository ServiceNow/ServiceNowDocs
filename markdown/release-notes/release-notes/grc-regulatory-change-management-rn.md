---
title: Regulatory Change Management release notes
description: The ServiceNow Regulatory Change Management application enables you to check upcoming regulatory changes, assess their impact, and implement risk and compliance-related changes. Regulatory Change Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
---

# Regulatory Change Management release notes

The ServiceNow® Regulatory Change Management application enables you to check upcoming regulatory changes, assess their impact, and implement risk and compliance-related changes. Regulatory Change Management was enhanced and updated in the Yokohama release.

## Regulatory Change Management highlights for the Yokohama release

-   Summarize a regulatory alert by using the Now Assist summarization skill.
-   Use Regulatory mapping with AI to help organizations identify, track, and manage regulatory requirements that are specific to their industry.
-   Set up a recommendation context.
-   Analyze the potential impacts of a new regulation to assess whether it's likely to achieve the required business or regulatory compliance objectives.

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Some Now Assist skills are now turned on by default.
-   Review changes to Now Assist usage measurements.

See [Regulatory Change Management](https://www.servicenow.com/docs/access?context=reg-change-mgmt-landing-page&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Regulatory Change Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Generating a summary of a regulatory alert](https://www.servicenow.com/docs/access?context=create-a-summary-of-a-reg-alert&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Transform your detailed regulatory information into concise, business-focused summaries that emphasize the most critical changes and impending deadlines. You can significantly cut down the time that is required to interpret complex updates, ensuring that no vital details are overlooked. By streamlining compliance processes, your organization becomes more efficient and minimizes the risks.

-   **[Regulatory mapping with AI](https://www.servicenow.com/docs/access?context=recommendations-for-a-regulatory-alert&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Leverage artificial intelligence to help your organizations identify, track, and manage regulatory requirements that are specific to their industry. AI automates the mapping of incoming regulatory changes to internal business operations, such as citations and control objectives, making it easier to ensure compliance. By analyzing the incoming regulatory changes and vast amounts of internal regulatory data, AI highlights the relevant policies for association and mapping, which helps your organization to streamline the compliance process and reduce manual effort.

-   **[Recommendation contexts and templates](https://www.servicenow.com/docs/access?context=recommendation-contexts&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Enable your administrators to use a framework engine to create decision templates for primary records. This framework simplifies the enterprise decision-making processes and includes the configurable user interface elements that provide contextual insights and improve the display of these elements. By integrating this framework, your organization can help to ensure that every recommendation is both relevant and informed.

-   **[Impact radius extension](https://www.servicenow.com/docs/access?context=add-impacted-area-reg-alert&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Identify the impacted areas of your business operations, such as the citations, control objectives, policies, risks, controls, and authority documents, that you can add to a regulatory alert. You can then conduct a review for implementation acceptance that triggers a change management program by assigning ownership and accountability through a Change Task. Additionally, an existing dashboard was improved so that you can get a clear overview of the impacted business operations.

-   **[Regulatory assessment for a regulatory alert](https://www.servicenow.com/docs/access?context=regulatory-assessment-in-rcm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    View the new Regulatory assessments related list for a regulatory alert. This list displays the uniquely generated regulatory assessments that are powered by the Smart Assessment Engine application so that you can analyze and track the completion status for compliance users. Your users with the sn\_grc.business\_user role can work on these assessments.


## UI changes

-   **[Changes on the action task form](https://www.servicenow.com/docs/access?context=create-action-task-using-ws&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The Category: Compliance section and the Category: Risk section on an action task form have been removed. They're replaced by the **Impacted area table** field and the **Impacted area** field.

-   **[Assess impact](https://www.servicenow.com/docs/access?context=assess-impact-of-reg-change-using-ws&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The **Initiate Impact Assessment** button is now called the **Assess impact** button.


## Changed in this release

-   **[Overview page of regulatory alerts](https://www.servicenow.com/docs/access?context=list-view-of-reg-alerts&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The Overview page for regulatory alerts includes a drop-down menu that enables you to track the progress of a regulatory assessment. Additionally, you can view the counts of completed, open, and overdue regulatory assessments.

-   **[Home page updates for Regulatory Change Management](https://www.servicenow.com/docs/access?context=rcm-workspace-for-managers&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    On the Regulatory Change Management home page, within the Tracking section, a new drop-down menu has the Regulatory Assessments or Risk Assessments options. With these options, regulatory change managers can see the number of open and overdue assessments to help them efficiently monitor the status of their assessments.

-   **[Regulatory assessments in the Tasks pane](https://www.servicenow.com/docs/access?context=regulatory-assessment-in-rcm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The Tasks pane in the Compliance Workspace now displays all the Regulatory assessments.


-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## Removed in this release

-   Related documents related list will be hidden for both the workspace and classic view for a regulatory alert.
-   The entity class configuration has been removed and is no longer necessary for conducting an assessment. You can select the entities now when you send the risk assessment.
-   Starting with the Yokohama release, all open assessments for a regulatory alert, whether they’re risk assessments or regulatory assessments, aren’t marked as canceled and remain open even after an alert is marked as applicable.

## Activation information

Install Regulatory Change Management and Now Assist for IRM by requesting them from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

