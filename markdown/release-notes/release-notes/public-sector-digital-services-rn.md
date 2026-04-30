---
title: Public Sector Digital Services release notes
description: The ServiceNow Public Sector Digital Services application enables government agencies to provide citizens, businesses, and other agencies with important services such as public records, licenses, permits, and social services. Public Sector Digital Services was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
---

# Public Sector Digital Services release notes

The ServiceNow® Public Sector Digital Services application enables government agencies to provide citizens, businesses, and other agencies with important services such as public records, licenses, permits, and social services. Public Sector Digital Services was enhanced and updated in the Zurich release.

## Public Sector Digital Services highlights for the Zurich release

-   Create funding programs to establish top-level budgets and timelines that flow down to associated grant programs.
-   Simplify and streamline the grant application decisions​ with Grants Management:​ Evaluation &amp; Decision.
-   Enable merit reviewers to track, score, and monitor grant applications via a dedicated Reviewer Service portal.
-   Enable applicants to review and download the results letter and merit review summary of their grants application, and accept or decline their award, all within the new **Results** tab of the Grants Management portal.
-   Define fees for and autonomously assess fee waivers against agency-defined criteria for information requests with the Help manage public information requests agentic AI Agent, part of the Public Sector Digital Services AI Agent Collection application.

See [Public Sector Digital Services](https://www.servicenow.com/docs/access?context=bun-public-sector-landing-page&version=zurich&pubname=zurich-government-industry&ft:locale=en-US) for more information.

**Important:** Public Sector Digital Services is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Public Sector Digital Services to Zurich

After the upgrade, certain public sector menus and menu items in CSM Configurable Workspace revert to their original CSM label names. You can relabel these items for public sector use by updating the labels for the Customer, Accounts, and Service Organizations UX list category records. For more details on relabeling, navigate to **All** &gt; **Constituent Service** &gt; **Administration** &gt; **Guided Setup**, and select **Configurable Workspace for Public Sector Digital Services** &gt; **Customize Workspace Labels Manually**.

## New in the Zurich release

-   **[Grants Management Funding Program](https://www.servicenow.com/docs/access?context=psds-using-grants-management-playbook&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)**

    Create a funding program, which serves as the top-level container from which individual grant programs are created and derive their budget allocations.

    Grant program managers can create a new funding program, or start by copying data and configurations from an existing funding program, using the funding program ID. From this funding program, admins can create grant programs directly, set and update the duration and overall budget, and ensure budgets flow down logically to individual grants.

    Each grant program is associated with a single funding program via the funding program ID. All grant programs linked to a specific funding program share the cumulative budget of that funding program, and their start and end dates fall within the funding program's duration.

-   **[Grants Management Evaluation &amp; Decision​](https://www.servicenow.com/docs/access?context=psds-using-grants-management-playbook&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)**

    Simplify and streamline your grant application decisions​ with Grants Management:​ Evaluation &amp; Decision. You can review, score, and manage proposals for grant programs in the Merit Review portal and define a funding proposal for a grant program by using the Grants Workspace. You can share this information internally with the grant program director.​ Grant program managers can define the merit review framework criteria, assign a reviewer group to each application, create, and track merit review tasks. Grant program managers can use document templates to compose letters that inform the applicants of results, with template options for Award, Rejected \(Ineligible\), and Rejected \(Decline\).

-   **[Grants Management Reviewer Service portal](https://www.servicenow.com/docs/access?context=psds-gmp-using-merit-review-portal-agent&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)**

    Enable your merit reviewers to track, score, and monitor grant applications via a dedicated Reviewer Service portal. The merit reviewers can capture and aggregate scores across the Grant Proposal review framework​ in the Grants Workspace. A score and rationale can be summarized as part of the application proposal result.​

-   **[Agentic AI for Public Sector Digital Services](https://www.servicenow.com/docs/access?context=agentic-ai-psds-explore&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)**

    Define the fees for information requests and autonomously assess waivers against an agency's criteria​. You can automate the process of synthesizing similar information requests and associated fees, and apply those fees to cases​. Your case fields are automatically filled in and integrated into the Information Request Playbook workflow and ServiceNow's AI framework.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Enhancements to Constituent Service Portals](https://www.servicenow.com/docs/access?context=portals-psds-exploring&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)**

    UI Enhancements have been made to all Public Sector Digital Services constituent portals by replacing legacy widgets \(for example, portal banners, data lists\) with standardized, CSM Configurable Widgets and components. The update ensures backward compatibility, migration guidance, usage analytics, and provide training for admins, and also enables dynamic data rendering, better filtering, and improved accessibility across service flows.


## Changed in this release

-   **[Enhancements to Grants Management: Program Setup](https://www.servicenow.com/docs/access?context=psds-using-grants-management-playbook&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)**

    In the Grants Management: program setup, grant program managers can now add new points of contact for the applicants to the grants program in the Define Program stage. In the Publish Program stage, new fields have been added for program announcement removal. Grants program managers can now set grants programs to auto-remove at a defined date, and set application close to disable new applications from being submitted through the Grants Management portal.

-   **[Enhancements to Grants Management portal](https://www.servicenow.com/docs/access?context=psds-gmp-using-grants-mgmt-portal&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)**

    Enable grant program managers to turn off new grant proposal submissions after the proposal close date. Applicants can no longer submit proposals after the proposal close date, keeping the process on schedule and helping prevent late submissions from being reviewed.

    Enable applicants to review and download the results letter and merit review summary \(where applicable\) of their grants application, as well as accept or decline their award, all within the new **Results** tab of the Grants Management portal. Notify constituents about a pending award decision through the portal.


-   **[Constituent Service Dashboard Migration to Platform Analytics](https://www.servicenow.com/docs/access?context=constituent-services-dashboard&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)**

    The Constituent Service Dashboard has been migrated to Next Experience Platform Analytics. Next Experience is a ServiceNow AI Platform® feature that is active by default when you load or upgrade to the Zurich release. The dashboard migration to Next Experience enables you to visualize historical and real-time process statistics in role-based dashboards. Access the new dashboard by navigating to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.


## Activation information

Install Public Sector Digital Services applications by requesting them from the ServiceNow Store. For details on installing the applications, see [Configuring Public Sector Digital Services](https://www.servicenow.com/docs/access?context=configuring-public-sector-digital-services&version=zurich&pubname=zurich-government-industry&ft:locale=en-US). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    The ServiceNow®Customer Service Management application enables customer service organizations and service operations to collaborate and resolve customer problems.

-   **[CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-workspaces-configure&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    The ServiceNow®CSM Configurable Workspace application provides government agents with the tools to research information, respond to questions from the public, and resolve cases.

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The ServiceNow®Now Assist application uses generative AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.


**Parent Topic:**[Features and changes by product](../new-features-changes.md)

