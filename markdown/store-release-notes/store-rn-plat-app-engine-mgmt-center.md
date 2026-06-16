---
title: App Engine Management Center release notes
description: Version history for the App Engine Management Center application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-app-engine-mgmt-center.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - ServiceNow AI Platform App Engine release notes, ServiceNow Store release notes]
---

# App Engine Management Center release notes

Version history for the App Engine Management Center application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 29.2.1 - June 2026**

    None.

-   **Version 29.1.1 - March 2026**

    Changed: Added better filtering experience in AEMC lists, including the ability to create saved filters and share those saved filters with other users or groups.

-   **Version 28.2.1 - December 2025**
    -   New:
        -   Manage releases and deployment requests for ReleaseOps, a new update set pipeline.
        -   Ability to migrate deployments from the App Engine pipeline to ReleaseOps.
-   **Version 27.2.1 - May 2025**

    New: Added detail section to App Readiness and Compliance report.

-   **Version 27.1.0 - February 2025**
    -   New:
        -   Generate an App Readiness report for custom apps from App Engine Management Center to better understand if an app is ready to be promoted to production. The App Readiness report is generated based on an out-of-the-box Instance Scan suite that includes 11 best practice checks and can be extended by customer by adding suites as children to the parent suite. The suite will run on the app in development and generate the report in App Engine Management Center.
        -   App description field is now visible on the App info page for each app in App Engine Management Center. The app description can be filled in manually by a developer or a developer can copy it from the new App Summary Generation GenAI skill.
-   **Version 26.2.1 - November 2024**
    -   Fixed:
        -   Approval state now recording correctly when a deployment request is approved.
        -   Made decision table for pipelines editable.
        -   Fixed instructions to set up Scan Suites table in Guided Setup.
-   **Version 26.1.0 - August 2024**

    Changed: In the admin section of the Application Intake, App Engine Admins will now have the ability to select a Creator Studio user group, in addition to or instead of just an App Engine Studio user group to provision a new user to.

-   **Version 25.1.2 - May 2024**
    -   New: App Engine Admins will be able to manage App Requests submitted by Creator Studio Restricted Users in AEMC.
    -   Changed: The Developers tab will now show users with a Creator Studio role or the admin role, in addition to AES roles and delegated development roles.
    -   Fixed: The Subscription Monitoring tab in AEMC now supports Licensing Engine v2.
-   **Version 24.1.1 - November 2023**
    -   New: License role type mapping. Now an App Engine Admin can see which role type a custom application role maps to, in addition to which users have those roles. We also show why a role is mapped to a given role type.
    -   Changed: Deployment requests, application requests, and collaboration requests are now more aggressively cached to prevent long delays in page load times on pages that display these records.
    -   Fixed: Performance improvements throughout. Many pages in AEMC are twice as fast to load as in previous versions, even for customers with significantly more data.
-   **Version 24.0.1 - August 2023**
    -   New:
        -   Pipelines and Deployments have two new features:
            -   Run any Instance Scan and ATF suite during deployment, which can be configured by adding those suites to the Scan Suites table on the production instance.
            -   Schedule deployments to production, allowing customers to deploy an app now or schedule for a later date/time.
        -   AEMC can now be accessed from the Admin tab, in addition to All.
    -   Changed: Added pipeline stepper back to the deployment request.
    -   Fixed: Confirmed that all versions of Pipelines and Deployments can use both OAuth credentials and basic auth credentials.
-   **Version 23.1.3 - May 2023**

    -   New: Added trend chart of requests over time showing number of requests by created date up to one year.
    -   Changed: Custom app and developer scorecards have been replaced with PAR charts. The PAR charts will collect data up to 90 days.
    -   Fixed: When scorecards are clicked, the associated list will be filtered to the correct records.
-   **Version 23.0.5 - February 2023**
    -   Changed:
        -   App Engine Management Center \(AEMC\) has been redesigned. AEMC is no longer a workspace, but is still accessible from App Engine &gt; Administration &gt; App Engine Management Center.
        -   The Lists tab has been renamed to Requests.
        -   The Applications tab has been renamed to Custom apps.
        -   A single record for each app is shown on the Custom apps tab instead of a record for development and a record for production. If an app has been published to production, the Published version field is populated. If the app has not been published to production, the Published version field is blank.
-   **Version 22.1.2 - November 2022**

    New: For each app that has been deployed to production, App Engine admins can now see usage data in AEMC. The App Engine admin now has both a usage summary for the current month where they can see the aggregated number of users, inserts, and updates, and a more granular view of the usage of various experiences in the app through User Experience Analytics.

-   **Version 22.0.1 - August 2022**
    -   New:
        -   The new Applications tab will give App Engine admins visibility into what custom apps are being built in any development instance \(as defined in the Pipelines and Deployments Environments tables\), that are in an active deployment, that have been published to a production instance \(as defined in the Pipelines and Deployments Environments tables\), and a breakdown of apps in both development and production by department. App Engine admins will be able to drill into individual apps to see the deployment history and who has access to develop on that app.
        -   The new Developers tab will give App Engine admins visibility into users in the App Engine Users group and users that have any delegated development permission in any development instance \(as defined in the Pipelines and Deployments Environments tables\). App Engine admins will be able to drill into individual developers to see what apps they are developing and their request history.
-   **Version 21.1.2 - May 2022**
    -   New:
        -   Added related records to the user details pages. When a customer selects a user's name in AEMC, it opens the user details page and they will see a related records panel on the left with all AES-related requests submitted by that user.
        -   Configured search for AEMC
        -   Added two filters to the home page and pipelines page. The filters can be used together or individually and they will persist between the home page and pipeline page. The filters do not currently persist on the list page.
            -   Date: Created date filters all requests based on the created date
            -   App name filters all requests based on the application name

**Parent Topic:**[ServiceNow Store - ServiceNow AI Platform App Engine release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-plat-app-engine.md)

