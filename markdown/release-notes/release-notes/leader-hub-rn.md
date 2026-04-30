---
title: Leader Hub release notes
description: The ServiceNow Leader Hub application empowers organizational leaders to understand the strengths of their teams, identify gaps in skills, and facilitate changes that are conducive to the success of their workforce. Leader Hub is a new application in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
---

# Leader Hub release notes

The ServiceNow® Leader Hub application empowers organizational leaders to understand the strengths of their teams, identify gaps in skills, and facilitate changes that are conducive to the success of their workforce. Leader Hub is a new application in the Xanadu release.

## Leader Hub highlights for the Xanadu release

-   Get quick access to a comprehensive overview of your organization's talent, including metrics for skill competency across different teams, identifying significant skill gaps, and employee engagement with the growth tools provided in the Talent Development suite of applications.
-   Gain visibility into the skills and talent composition of each team that exists within your organization, at any level of granularity, through an organizational chart that illustrates the reporting relationships across the different teams in your organization.
-   Give organizational supporters to whom the leader has delegated responsibilities access to Leader Hub from a view that enables them to see their designated leader's organization and provide support accordingly.

See [Leader Hub](https://www.servicenow.com/docs/access?context=td-lh-landing&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US) for more information.

**Important:** Leader Hub is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Leader Hub features

-   **[At a glance](https://www.servicenow.com/docs/access?context=td-lh-explore&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    Supply your organizational and HR leaders with instant access to a comprehensive overview of their organization's talent via the At a glance page. This page is the home page for Leader Hub and it offers a glance at data that measures employee engagement and skill proficiency, along with a glimpse of the teams that comprise your organization. The At a glance page gives leaders quick and easy access to the following information about the teams in their organization:

    -   Skill scores
    -   Significant skill gaps
    -   Employee engagement with the growth tools available in the Talent Development suite of applications.
    Leaders can access the At a glance page by selecting **At a glance** from the Leader hub drop-down list.

-   **[Org talent](https://www.servicenow.com/docs/access?context=td-lh-explore&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    Provide your leaders with a centralized location to view the talents of each team that exists within their organization via the Org talent page. Leaders can view talent data at any level of granularity through an interactive organizational chart that illustrates the structure of their organization and the reporting relationships between managers and employees for each team in their organization.

    Leaders can access the Org talent page by selecting **Org talent** from the Leader hub drop-down list.

-   **[Org skills](https://www.servicenow.com/docs/access?context=td-lh-explore&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    Equip your leaders with the tools to understand the skill composition of their organization via the Org skills page. The Org skills page displays skills relevant to your leader's organization and provides metrics that leaders can use to identify critical skill gaps and hold managers responsible for developing talent within their teams. Leaders can further examine the details associated with each skill by selecting the name of the skill that they want to view to access the Skill details page.

    Leaders can access the Org skills page by selecting **Org skills** from the Leader hub drop-down list.

-   **[Orgs you support](https://www.servicenow.com/docs/access?context=td-lh-explore&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    Give organizational supporters insights into their leader's workforce via the Orgs you support page. Supporters entrusted with delegated responsibilities can be designated by their leaders to access Leader Hub so they can provide support in the capacity required for the organization to succeed.

    Supporters can access the Orgs you support page by selecting **Orgs you support** on the mega menu from the Employee Center portal.

-   **[Quick start tests for Leader Hub](https://www.servicenow.com/docs/access?context=quick-start-tests-leader-hub&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that Leader Hub still works. If you customized Leader Hub, copy the quick start tests and configure them for your customizations.


## UI changes

-   **[Leader hub drop-down list](https://www.servicenow.com/docs/access?context=td-lh-explore&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    The Leader hub drop-down list is a new menu item that appears on the mega menu in the Employee Center portal. The Leader hub drop-down list is only accessible to employees with the leader \(sn\_egd\_lh.leader\) role assigned to their user record. This drop down list contains the following options from which you can select:

    -   **At a glance**
    -   **Org talent**
    -   **Org skills**
-   **[Orgs you support menu item](https://www.servicenow.com/docs/access?context=td-lh-explore&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    Orgs you support is a new menu item that appears on the mega menu in the Employee Center portal. The Orgs you support menu item is only accessible to employees with the supporter \(sn\_egd\_lh.supporter\) role assigned to their user record.


## Activation information

Install Leader Hub by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

You must have Talent Development Core to use Leader Hub.

## Related ServiceNow applications and features

-   **[Talent Development Core](https://www.servicenow.com/docs/access?context=egd-landing-page&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    Talent Development Core \(sn\_egd\_core\) includes the Skills Intelligence plugin \(sn\_skills\_int\) which must be enabled to use Leader Hub. Talent Development Core also provides the following modules which are growth tools used in the metrics that Leader Hub generates for measuring employee engagement:

    -   Aspirations
    -   Growth plans
-   **[Skills Intelligence](https://www.servicenow.com/docs/access?context=skills-intelligence&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    Leader Hub uses the skill data from Skills Foundation in the metrics it produces for skill competency scores and critical skill gaps.

-   **[Career Conversations](https://www.servicenow.com/docs/access?context=egd-activities-conversations-module&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    When you optionally install the Career Conversations plugin \(sn\_egd\_act\), Leader Hub generates metrics for employee engagement with the Career Conversations app, such as the percentage of managers in your organization who had conversations with their employees in the past 30 days.

-   **[Mentoring](https://www.servicenow.com/docs/access?context=mentoring-egd-overview&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    When you optionally install the Employee Connections plugin \(sn\_ecn\), Leader Hub generates metrics for employee engagement with the Mentoring app, such as the percentage of employees in your organization currently engaged in mentorship.

-   **[Learning](https://www.servicenow.com/docs/access?context=exploring-learning-exp&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    When you optionally install the Learning plugin \(sn\_lep\), Leader Hub generates metrics for employee engagement with the Learning app, such as the percentage of employees in your organization who have completed courses in the past 30 days.


**Parent Topic:**[Talent Development release notes](employee-growth-development-landing.md)

