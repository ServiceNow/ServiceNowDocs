---
title: Business Continuity Management release notes
description: The ServiceNow Business Continuity Management application gives your organization the capability to continue to deliver products and services at an acceptable level when a disruptive incident occurs. Business Continuity Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Business Continuity Management release notes

The ServiceNow® Business Continuity Management application gives your organization the capability to continue to deliver products and services at an acceptable level when a disruptive incident occurs. Business Continuity Management was enhanced and updated in the Yokohama release.

## Business Continuity Management highlights for the Yokohama release

-   Use the latest assessment template to perform a Business Impact Analysis.
-   Create nested plans in an event so that you can activate cross-references to multiple plans.
-   Use the hierarchical view in the plans to organize nested event tasks according to their dependencies.
-   Use the Crisis map functionality that includes the latest UIB components.

See [Business Continuity Management](https://www.servicenow.com/docs/access?context=business-continuity-mangmt-overview&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Business Continuity Management is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Using latest assessment template for conducting BIAs](https://www.servicenow.com/docs/access?context=using-smart-asmt-template&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Conduct a Business Impact Analysis \(BIA\) by using the latest assessment template. The assessment template enables you to create questions of different types and automate the responses from existing data sources. You can configure the logic for calculating the recovery tier, recovery point objective, recovery time objective, or maximum tolerable downtime.

-   **[Adopting UIB page for improved performance](https://www.servicenow.com/docs/access?context=crisis-map-migration&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Leverage the Crisis map functionality that includes the latest UIB components. By adopting the UIB components, you can help to minimize development efforts and get more configuration options within the Crisis map application.

    You can filter alerts by their state \(active or inactive\), severity level, location \(regions\), or source. You can refine your search, perform detailed queries, or edit actions on the alerts, so that it's easier to find both the alerts and assets on the map. Additionally, you can set the secondary values such as urgency, severity, category for the alerts in the Details card.

-   **[Using nested plans](https://www.servicenow.com/docs/access?context=creating-nested-plan-in-event&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Create nested plans in an event so that you can activate cross-references to multiple plans. You can use the hierarchical view to organize nested event tasks according to their dependencies with the work-breakdown structure \(WBS\) functionality. You can also monitor the progress bar to track the creation of related plans, event assets, or event tasks.


## UI changes

-   **[Using latest assessment template for conducting BIAs](https://www.servicenow.com/docs/access?context=using-smart-asmt-template&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**
    -   The BIA form displays the assessment questionnaire that is based on the latest assessment template. The **Assessments** tab in the BIA record page has been enhanced to eliminate repetitive UI actions and reduce large empty spaces. The latest assessment template includes additional question types such as drop-down, references, text, attachments, check boxes, date, time, and number value inputs.
    -   The PDF template for the BIA has been updated to include the questions and answers that are based on the latest assessment template.
-   **[Adopting UIB page for improved performance](https://www.servicenow.com/docs/access?context=crisis-map-migration&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The enhancements to the Crisis map user interface are:

    -   Alerts are displayed in the side panel of the Crisis map application.
    -   The alert details page includes the **Open alert** and **Dismiss alert** UI actions, which enable you to either open or dismiss alerts.
    -   The active alerts can be sorted by using the **Severity**, **Created**, **Updated** fields, and can also be toggled from top-to-bottom or bottom-to-top by using the Toggle option.
    -   The alerts display can be updated with the Refresh icon ![Refresh icon.](../image/refresh-icon.jpg).
    -   The active and dismissed alerts are now displayed on the Alerts page.
-   **[Using nested plans](https://www.servicenow.com/docs/access?context=creating-nested-plan-in-event&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The enhancements to the nested plans user interface are:

    -   The hierarchical view shows the nested event tasks.
    -   The progress bar displays the progress of the creation of related plans, event assets, or event tasks.

## Changed in this release

-   **[Using latest assessment template for conducting BIAs](https://www.servicenow.com/docs/access?context=using-smart-asmt-template&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    You can use the latest assessment template to conduct the Business Impact Analysis \(BIA\).


## Activation information

Install Business Continuity Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Browser requirements

Business Continuity Management requires the following browsers:

-   Google Chrome
-   Firefox and Firefox Extended Support Release \(ESR\)
-   Microsoft Edge Chromium
-   Safari 12.0 and later versions

## Accessibility information

Various accessibility issues in the Crisis map application have been resolved with the implementation of the Geomap \[sn\_geo\_map\] component, which has replaced the FAM Map \[sn-fam-map\] component.

**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

