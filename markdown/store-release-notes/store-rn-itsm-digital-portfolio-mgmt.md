---
title: Digital Portfolio Management release notes
description: Version history for the Digital Portfolio Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-digital-portfolio-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 26
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# Digital Portfolio Management release notes

Version history for the Digital Portfolio Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 7.5.0 - June 2026 \(Zurich+\)**
    -   !!! WARNING: This release removes over 700 read ACLs on secondary/tertiary tables from the DPM Manager role. !!!This impacts existing installations as well as new installations. This means that if you drill down into a record \(say an incident or change record\) you will still have access to that primary record, but will not automatically be granted read access to all of the related tables that associate with incidents and changes. This change was made to remove the overly broad access given to default by the dpm\_manager role. If this impacts you, you will need to go in and manually add any specific access to specific tables your DPM managers required back to the dpm\_manager role \(or create a new sub-role, or add read access directly for certain users\).
    -   New: DPM now supports the new enterprise agile planning tables for business applications
    -   Fixed: PRB2004635 - removed deprecated DPM breakdown, improving the performance of the DPM data collection job
    -   Removed: Removed over 700 direct read ACLs from the sn\_dpm.dpm\_manager role. See warning above.
-   **Version 7.4.2 - March 2026 \(Zurich+\)**
    -   Fixed:
        -   PRB1969965
            -   Fixed an issue in DPM admin center where users were unable to map cmdb\_ci\_service\_discovered records to KPI groups.
        -   PRB1991433
            -   Fixed an issue where header config records that reference non-existent fields caused the entire screen to not load
        -   PRB1974685
            -   Fixed an issue where conditions were being ignored for the configurable headers in DPM
-   **Version 7.4.1 - January 2026 \(Yokohama+\)**

    Fixed: PRB1965567 - Fixed an issue with broken single score data visualizations when upgrading to Zurich.

-   **Version 7.3.2 - December 2025 \(Yokohama+\)**
    -   Changed: Users with the dpm\_admin role now see the correct read/write permissions when browsing personal portfolios. Previously they could see personal portfolios that were shared with them as read only, but since they are dpm\_admins, they have write access as well. This now shows appropriately in the UI.
    -   Fixed:
        -   PRB1942385 - Fixed an issue where digital portfolio management specific fields showed up on the details section of the dmn\_demand UI16 form view.
        -   PRB1953963 - Fixed an issue where the needs attention items didn't update automatically when the underlying taxonomy is changed
        -   Fixed ACL issue with the dpm\_manager role and PA dashboards
        -   Security improvements
    -   Removed:
        -   DPM no longer has a hard dependency on the spm\_premium plugin
        -   Removed unnecessary references to the 'admin' role as part of the granular admin roles directive. admins will have access regardless, and dpm\_admin is the main/required role for DPM admin tasks
-   **Version 7.2.0 - August 2025**
    -   New:
        -   DPM can be configured to show more than one KPI group on the enterprise portfolio preview pages.
        -   The "Needs Attention" feature on many screens in DPM is now more performant for larger data sets.
        -   Added a loading state spinner to Needs Attention 'right rails' in DPM, so customers with very large data sets don't perceive a slow load as broken.
        -   We have recreated the 'Overdue Incidents' indicator within the DPM scope for performance reasons.
            -   New installs will automatically use the new indicator.
            -   Existing installs will still use the old indicator and everything should continue working. However, we recommend that customers re-map to the new indicator, which has the same name but with a prefix of "DPM:"
        -   Updated the 'portfolio list' component to make it easier to switch between portfolios.
        -   Renamed 'Application Service' to 'Service Instance' per updated CSDM naming conventions.
    -   Fixed:
        -   PRB1910321 - Fixed a configuration issue with the indicator 'DPM: Number of Open Changes' which was causing high memory usage during daily data collection for large data sets.
        -   PRB1897087 - Fixed an issue where the creation of a new application service \(service instance\) portfolio was creating a business application portfolios instead.
        -   PRB1885073 - Fixed an issue where tag based application services \(service instances\) were not showing up on the service offering run tab.
-   **Version 7.0.6 - June 2025**
    -   Fixed:
        -   PRB1889172 - Fixed the 'remove button' while editing portfolios.
        -   PRB1889636 - Fixed missing score in the 'initiatives by state' pie chart on the service offerings build page.
        -   PRB1888180 - Fixed issue causing scheduled emails for email reporting feature to not be sent.
-   **Version 7.0.4 - May 2025**
    -   New:
        -   Configurable Info tab allows customers to configure the Info tab of the solutions pages, similarly to how they can configure the Plan, Build, and Run tabs. This includes showing or hiding sections of the tab.
        -   DPM users with the dpm\_admin role can now create and edit portfolios directly within DPM, and three portfolio templates are included \("EDUCAUSE", "IT Service Portfolio", and "Sample Organization Structure"\).
        -   DPM users can now send an email to any users with the dpm\_manager role that includes the first KPI group data and a link back to the solution they are sending an email from. This feature is off by default and can be activated in the DPM Admin center under a new 'Email properties' section.
        -   DPM admins can turn on a scheduled job that will automatically send the top KPI group data in an email to the solution owners. The schedule is configurable and will only send KPI data for the 'top level objects' that a user owns. For example, if they own a taxonomy node, it won't send data on sub nodes or services.
    -   Fixed:
        -   PRB1843573 - DPM &gt; My Lists &gt; Add new list - Columns set in the list set up are not displayed in the created List.
        -   PRB1844843 - If Available item type Business service is made inactive, DPM is displaying "The page you are looking for could not be found" when clicking on the widget's Availability for Performance or Service Metrics.
        -   PRB1845557 - Needs attention on the Enterprise Portfolio page is slow to load.
        -   PRB1850383 - Removed an unnecessary ACL.
        -   PRB1857783 - Under KPI Group properties, the switch to turn on/off the latest score property is not honored.
        -   PRB1862858 - DPM: Daily Data Collection is causing out of memory and node restarts.
        -   PRB1866992 - DPM Application Service Info tab... the "Application service description" is missing.
        -   PRB1868132 - DPM: When turning off the available item type for business applications the homepage does not load for user who have not customized their tiles.
        -   PRB1870387 - For incident indicators extended application service classes are not being counted in the affected ci/impacted service related list.
-   **Version 6.1.9 - February 2025 \(Xanadu\)**
    -   New:
        -   New Troubleshooting tab and menu in DPM Admin center.
        -   Retired \(non-operational\) services no longer show up on the homepage, nor are performance analytics calculated for non-operational services.
        -   Updated various images to be 'theme-able'.
    -   Fixed:
        -   PRB1740288 - Fixed an issue where if multiple breakdowns are associated with a formula indicator \(for example, average P1 incidents\), the shown value would be incorrect.
        -   PRB1828595 - Fixed a slow loading issue with the enterprise portfolios content tree.
        -   PRB1833597 - Fixed an issue where the enterprise portfolio content tree didn't load if the portfolio was empty.
        -   PRB1831903 - Removed the unnecessary readonly attribute on report\_view ACLs which will allow customers to tune their report view ACLs.
        -   PRB1838775 - Fixed an issue with the business capabilities and application services widgets on the business application info tab.
-   **Version 6.1.3 - November 2024 \(Washington DC+\)**
    -   New:
        -   Admin center getting started flows now have direct links to services, business apps, and app services lists.
        -   Personal Portfolio solution cards are now configurable within admin center.
        -   KPIs within KPI groups can now be set to 'active=false' and they won't render within DPM.
        -   Updated Needs attention to include application services when you add them to the Impacted services or the Affected CIs related list \(in addition to the Configuration field\). The data rolls up to the business application, taxonomy node, and at the portfolio level.
    -   Changed:
        -   Homepage card sort now based on total red/yellow status items.
        -   Made the breakdowns of incident/problem/change more consistent across DPM including admin center.
        -   Time series KPI indicator visualizations now allow drill downs into the detail view.
    -   Fixed:
        -   Accessibility defects across the workspace
        -   PRB1809875 - DPM Widget: Number of open and overdue incidents not showing entries for the "Incident SLA" tab
        -   PRB1805678 - Services \(business\_service\) not showing Critical Incidents on the DPM homepage via the solution cards
        -   PRB1768035 - DPM Run tab does not display Calculated and Tag based Application Services
        -   PRB1802698 - Incorrect service breakdown is shown in taxonomy overview page
        -   PRB1803873 - Convert error messages to info messages for some functions that weren't in an error state.
        -   PRB1783202 - DPM workspace - when creating personal portfolio, if any of the available item types\(e.g business applications or service offerings\) has zero records, the other item types are keeps loading
-   **Version 5.2.3 - September 2024 \(Vancouver\)**

    Fixed: Fixed a dependency issue causing 'view relationships' to fail for customers who don't also have the CMDB workspace installed.

-   **Version 6.0.8 - August 2024 \(Washington DC\)**
    -   New:
        -   Updated the DPM Admin Center feature to include guided setup flows for business applications and application services.
        -   Added a new Needs Attention attribute type for Problem records that customers can activate.
        -   Added descriptive KPI tooltips to clarify indicator data. The DPM admin role can update these tooltips.
        -   Updated the team logic in the DPM Contacts tab in the Needs attention panel. The Teams tab shows multiple teams that support the service offering.
        -   Added the ability to automatically add the DPM breakdowns and jobs for DPM KPIs to reduce PA-related errors on KPIs in DPM.
        -   Added the ability to configure the Header section and Info tab General info section of solutions in DPM. It's no longer necessary to customize those pages using UI Builder.
    -   Fixed:
        -   Removed unnecessary ACLs for planned\_task and cmdb\_ci\_business\_app tables.
        -   Fixed the display overlap issue for retired service offerings.
        -   Removed needs attention Audit tab for applications, services, and application service taxonomy nodes \(audits don't apply to app services\).
        -   Critical incidents attached to offerings in Personal Portfolios now show up correctly in the Needs attention panel area of the Personal Portfolio.
-   **Version 5.2.2 - June 2024 \(Vancouver and Washington DC\)**
    -   New:
        -   Created Phase 1 of the Digital Portfolio Management Admin Center.
            -   Provides administrators a guided walk-through as they set up and configure the DPM Workspace for the organization.
            -   Includes the Overview and Settings tabs.
            -   Provides the necessary plug-ins and visibility into the end-to-end service and application life cycle.
            -   Accessible from the ServiceNow Admin Configuration Hub.
    -   Changed:
        -   Replaced the DPM custom relationship map with the global ServiceNow Unified CI map.
        -   Added default tooltips to PAR visualizations for all KPI Description fields. Administrators have the option to remove the default tooltips.
        -   The KPI latest score is set to be true for new and zboot customers, removing the former Sum and Average fields on KPI records.
    -   Fixed:
        -   PRB1743920 - Resolved non functioning 'new' button for business apps, app services, and business services during the personal portfolio creation tool.
        -   PRB1739321 - Removed class qualifier on query for outages in the needs attention results. Now outages attached to other sub-classes of cmdb\_ci\_service will show up in Needs attention.
        -   PRB1735943 - Fixed an issue that limited users available to pick from when adding editors and viewers during personal portfolio creation.
        -   PRB1734438 - Fixed an issue with a missing filter on the single score of 'upcoming changes this week' on the service offering build tab.
        -   PRB1730749 - First round of fixes related to missing i18n translations throughout DPM.
        -   PRB1730749 - removed an non critical read ACL on the 'planned\_task\_custom\_console\_member' table that was limiting access for users w/o the dpm\_manager role.
-   **Version 5.0.6 - March 2024 \(Vancouver and Washington\)**
    -   Fixed:
        -   Needs Attention: outages and alerts associated with services now roll up to the taxonomy nodes and portfolios.
        -   Fixed an issue that would cause a blank homepage in DPM when the com.snc.apm plugin was installed.
-   **Version 4.3.3 - March 2024 \(Utah\)**
    -   Fixed:
        -   Needs Attention: outages and alerts associated with services now roll up to the taxonomy nodes and portfolios.
        -   Fixed an issue that would cause a blank homepage in DPM when the com.snc.apm plugin was installed.
-   **Version 5.0.3 - February 2024 \(Washington DC\)**
    -   New:
        -   View related knowledge articles on the service and offering detail pages, located in the contextual side panel.
        -   View related business applications in the Info tab of a business application. When the business application is a platform host, you can now see all platform applications that run on that host. When the application is a platform application, you can now see the related platform host.
        -   Use the CSDM lifecycle fields for services and offerings when the CSDM activation plugin is installed \(com.snc.cmdb.csdm.activation\). With the plugin installed, the Lifecycle Stage and Lifecycle Stage Status fields replace the Phase and Status fields for all services and offerings.
        -   Sort the Needs attention section.
    -   -   Changed:
    -   View the updated Team and Team member contact cards in the side panel of solutions.
    -   See changes from related application services on the Build tab of business applications. This update was made possible due to the condition updates to the Change widgets.
    -   View any number of solutions on the DPM homepage. There's no longer a limit to the number of solutions. Use the Refresh button on the DPM homepage to update the solution status.
-   **Version 4.2.5 - November 2023 \(Vancouver\)**
    -   New:

        -   The redesigned DPM homepage enables you to keep track of all your solution cards and access your DPM browsing history. You can also personalize the updated DPM homepage.
            -   Upon first login, the DPM homepage displays solution cards that the user is associated with, based on the username in certain table fields.
            -   To tailor a users first-time experience, the DPM Admin can modify a user's homepage solutions table to set the solutions that should be shown.
            -   Add or remove solution cards and configure the needs attention attributes and thresholds for a personalized view of your DPM homepage \(see Performance\).
            -   Once you add or remove a solution card from your homepage, the system will no longer generate the solution cards to display. Instead, your homepage will show the solution cards based on your preferences and keep those preferences in the user's homepage solutions table.
        -   DPM Homepage Performance
            -   Two system properties limit the number of solutions cards that DPM can show for the user per table. The limit is 200 solution cards. DPM offers this breakdown:
                -   Services table: 150 cards' \(services, service offerings, and application services\)
                -   Business applications table: 50 cards
            -   DPM Admins can adjust the limits of 150 and 50, but the total limit cannot exceed 200
            -   When a user adds and removes solutions cards, they can add any combination of solutions to their homepage, but the total solution cards cannot exceed 200.
            -   It's in the roadmap for a future release to increase the number of solution cards.
        -   Available item types
            -   DPM Admins access the available item types table from the filter navigator within the DPM Administration section.
            -   DPM Admins use the available item types table to hide or show specific solution types in the homepage, as well as the personal portfolio.
            -   When a DPM Admin hides a solution type, that solution will not be included in the auto-generation results, in the add and remove items options, in the set status conditions modal, or in the page filters.
        -   Process Mining for DPM
            -   Process Mining enables DPM users to see key performance indicator \(KPI\) details and analyze anomalies.
            -   Project templates that come with DPM for Process Mining are incidents, problems, changes, and requests.
            -   DPM Admins enable Process Mining by installing the ITSM Process Mining Content Pack from the ServiceNow Store and setting the system property sn\_dpm.enable.po.dpm to true.
        -   Changed:
            -   Needs attention cards no longer display on the homepage. Instead, needs attention attributes display on each solution card.
            -   The order of the needs attention attributes determines how they show on each solution card.
-   **Version 4.2.4 - November 2023 \(Utah\)**
    -   New:
        -   The redesigned DPM homepage enables you to keep track of all your solution cards and access your DPM browsing history. You can also personalize the updated DPM homepage.
            -   Upon first login, the DPM homepage displays solution cards that the user is associated with, based on the username in certain table fields.
            -   To tailor a user's first-time experience, the DPM Admin can modify a user's homepage solutions table to set the solutions that should be shown.
            -   Add or remove solution cards and configure the needs attention attributes and thresholds for a personalized view of your DPM homepage \(see Performance\).
            -   Once you add or remove a solution card from your homepage, the system will no longer generate the solution cards to display. Instead, your homepage will show the solution cards based on your preferences and keep those preferences in the user's homepage solutions table.
        -   DPM Homepage Performance
            -   Two system properties limit the number of solutions cards that DPM can show for the user per table. The limit is 200 solution cards. DPM offers this breakdown:
                -   Services table: 150 cards \(services, service offerings, and application services\)
                -   Business applications table: 50 cards
            -   DPM Admins can adjust the limits of 150 and 50, but the total limit cannot exceed 200
            -   When a user adds and removes solutions cards, they can add any combination of solutions to their homepage, but the total solution cards cannot exceed 200.
            -   It's in the roadmap for a future release to increase the number of solution cards.
        -   Available item types
            -   DPM Admins access the available item types table from the filter navigator within the DPM Administration section.
            -   DPM Admins use the available item types table to hide or show specific solution types in the homepage, as well as the personal portfolio.
            -   When a DPM Admin hides a solution type, that solution will not be included in the auto-generation results, in the add and remove items options, in the set status conditions modal, or in the page filters.
        -   Process Mining for DPM
            -   Process Mining enables DPM users to see key performance indicator \(KPI\) details and analyze anomalies.
            -   Project templates that come with DPM for Process Mining are incidents, problems, changes, and requests.
            -   DPM Admins enable Process Mining by installing the ITSM Process Mining Content Pack from the ServiceNow's Store and setting the system property sn\_dpm.enable.po.dpm to true.
    -   Changed:
        -   Needs attention cards no longer display on the homepage. Instead, needs attention attributes display on each solution card.
        -   The order of the needs attention attributes determines how they show on each solution card.
-   **Version 4.0.12 - September 2023 \(Utah\)**

    Fixed an issue with missing data on taxonomy nodes screens when the "Service Portfolio Management Estimated Spend" plugin is installed.

-   **Version 4.0.10 - August 2023**
    -   New:
        -   Create and view Enterprise Portfolios for business applications and application services.
        -   Filter enterprise portfolio solutions by lifecycle status.
        -   Create, map, and view KPI groups for business application and application service enterprise portfolios.
        -   Create, map, and view KPI groups for business applications.
        -   Enable the latest score system property to view the last collected score for all KPIs in DPM.
        -   Add groups of users as editors and viewers of a personal portfolio.
    -   Changed:
        -   Updated the Technology Portfolio Management data to the new TPM data model to show key lifecycle dates for business applications and application services on the Risk tab.
        -   Moved all applications services from the Run tab to the Info tab on the business application detail page.
        -   Moved all software and hardware models from the Run tab to the Info tab on the application service detail page.
        -   Updated the MTTR KPI in the Performance snapshot KPI group to Incidents not updated in the last 5 days.
-   **Version 2.2.21 - March 2023**
    1.  KPI drill downs: fixed an issue causing leaf nodes to display grid instead of record list.
    2.  KPI drill downs: fixed an issue with a missing scrollbar when there are more than 10 offerings.
    3.  KPI drill downs: If a customer maps incidents directly to a service instead of an offering \(preferred\) the correct incident count will show on the service, and the correct \(but different\) incident count will show on the offerings.
    4.  Removed 'edit in service builder' buttons if a user doesn't have permission to edit the given service from various screens in DPM.
    5.  Alignment Planner Workspace: Fixed version incompatibility with Alignment Planner workspace \(APWS\). San Diego compatible versions of DPM \(2.\*\) and now compatible with San Diego compatible versions of APWS \(4.\*\). Tokyo compatible versions of DPM \(3.\*\) are now compatible with Tokyo/Utah versions of APWS \(renamed to Portfolio Planning for standard licenses and to Strategic Planning for pro licenses\).
    6.  Service offering info tab: Now showing description value, not short description value.
    7.  Service details page: Now showing business criticality field and the pill is now the correct color.
    8.  Service details build tab: The improvement initiatives donut chart will now show the '0' count instead of being blank when there are no mapped improvement initiatives.
    9.  Service details run tab: Removed a 'link to self' on offering drill downs grid view. This caused the page to navigate back to itself, creating recursive breadcrumbs and a confusing customer experience.
    10. Service details build tab: fixed initiatives by state count to key off of 'state' and not 'breakdown\_level2' which means the number in the donut chart and the number of initiatives in the list drilldown are now consistent.
    11. Home page: fixed 'undefined' showing up during page load.
    12. Enterprise portfolio overview page: Reduced duplicate API calls on portfolio overview page, improving page load times.
    13. Personal portfolios page: Improved slow loading issue with personal portfolio view.
-   **Version 3.1.4 - February 2023**
    -   NOTE: This version is compatible with the Utah family release.
    -   New:
        -   Added system property to enable DevOps data in DPM. When enabled, users can:
            -   Navigate to the DevOps Insights dashboard from the flow metrics section of the business application Build tab.
            -   Navigate to the DevOps Change Workspace from the accelerate metrics section of the business application Build and Run tabs.
        -   Added DevOps accelerated metrics to business applications Build and Run tabs.
    -   Changed:
        -   Moved DevOps flow metrics from business applications Plan tab to the Build tab.
        -   Updated the dpm\_manager role:
            -   Removed the service\_editor role and business app editor from dpm\_manager role.
            -   Users now must have the service\_editor role to edit services and offerings in Service Builder from DPM.
        -   Hid the create CIM \(create demand\) option when the CIM plugin or the Demand plugin is not installed. 
        -   Updated the Contacts tab so any users and groups related to the service, offering, business application, or application service will display on that tab.
        -   Updated the auto-create a personal portfolio feature to add application services.
        -   Updated KPI groups:Users can now choose the source indicator for a Formula Indicator KPI so the source records will show on the KPI drill down.
        -   Added a provided "Changes" KPI group.
        -   Changed the label of the "Catalog activity" KPI group from "New requests" to "Service requests."
        -   Created a new provided KPI group called "Service performance" that can be mapped directly to services. It has the same supporting KPIs as the Performance snapshot.
        -   KPI visualization configurations are now on the KPI record related list.
        -   Added the ability to sort offerings in taxonomy from a-z.
    -   Fixed:
        -   Improved labels and metrics in the 'initiatives by state' donut chart
        -   Fixed an issue where the KPI details grid had a link to itself.
        -   Added business criticality field on the business service details page.
        -   Improved slow loading issue with personal portfolio view.
        -   Fixed version compatibility issue between DPM and Alignment Planner Workspace.
        -   Fixed an issue where a service portfolio incident and the incident\_sla indicators scores didn't match taxonomy nodes scores. Now, when an incident is mapped directly to a service \(instead of to an offering\) the counts reflect that in the related indicators.
        -   Fixed an issue where a disabled 'admin' account created users and incidents \(demo data script name issue\).
        -   Updated the name of demo data creation script to avoid confusion.
        -   All KPI configurations now display in the related list on the KPI Group record \(not just on a group filter\)
        -   Fixed general performance issues:
            -   The Close dialog box in "Manage access" wasn't working.
            -   "Number of Overdue Changes" KPI indicator had a faulty condition.
            -   DPM historic data collections in job log wasn't correct.
            -   Improvement initiatives donut chart wasn't displaying total count.
            -   Workspace pagination behavior wasn't consistent.
            -   Sparkline view of the Performance snapshot KPI group/MTTR wasn't accurate.
            -   Duplicate team values were showing in the DPM Workspace.
-   **Version 3.1.3 - February 2023**
    -   NOTE: This version is compatible with the Tokyo family release.
    -   New:
        -   Added system property to enable DevOps data in DPM. When enabled, users can:
            -   Navigate to the DevOps Insights dashboard from the flow metrics section of the business application Build tab.
            -   Navigate to the DevOps Change Workspace from the accelerate metrics section of the business application Build and Run tabs.
        -   Added DevOps accelerated metrics to business applications Build and Run tabs.
    -   Changed:
        -   Moved DevOps flow metrics from business applications Plan tab to the Build tab.
        -   Updated the dpm\_manager role:
            -   Removed the service\_editor role and business app editor from dpm\_manager role.
            -   Users now must have the service\_editor role to edit services and offerings in Service Builder from DPM.
        -   Hid the create CIM \(create demand\) option when the CIM plugin or the Demand plugin is not installed.
        -   Updated the Contacts tab so any users and groups related to the service, offering, business application, or application service will display on that tab.
        -   Updated the auto-create a personal portfolio feature to add application services.
        -   Updated KPI groups:
            -   Users can now choose the source indicator for a Formula Indicator KPI so the source records will show on the KPI drill down.
            -   Added a provided "Changes" KPI group.
            -   Changed the label of the "Catalog activity" KPI group from "New requests" to "Service requests."
            -   Created a new provided KPI group called "Service performance" that can be mapped directly to services. It has the same supporting KPIs as the Performance snapshot.
            -   KPI visualization configurations are now on the KPI record related list.
        -   Added the ability to sort offerings in taxonomy from a-z.
    -   Fixed:
        -   Improved labels and metrics in the 'initiatives by state' donut chart
        -   Fixed an issue where the KPI details grid had a link to itself.
        -   Added business criticality field on the business service details page.
        -   Improved slow loading issue with personal portfolio view.
        -   Fixed version compatibility issue between DPM and Alignment Planner Workspace.
        -   Fixed an issue where a service portfolio incident and the incident\_sla indicators scores didn't match taxonomy nodes scores. Now, when an incident is mapped directly to a service \(instead of to an offering\) the counts reflect that in the related indicators.
        -   Fixed an issue where a disabled 'admin' account created users and incidents \(demo data script name issue\). Updated the name of demo data creation script to avoid confusion.
        -   All KPI configurations now display in the related list on the KPI Group record \(not just on a group filter\)
        -   Fixed general performance issues:
            -   The Close dialog box in "Manage access" wasn't working.
            -   "Number of Overdue Changes" KPI indicator had a faulty condition.
            -   DPM historic data collections in job log wasn't correct.
            -   Improvement initiatives donut chart wasn't displaying total count.
            -   Workspace pagination behavior wasn't consistent.
            -   Sparkline view of the Performance snapshot KPI group/MTTR wasn't accurate.
            -   Duplicate team values were showing in the DPM Workspace.
-   **Version 3.0.3 - December 2022**
    -   Fixed the following issues in this latest patch:
        -   Fixed an issue causing search within DPM when working on the Utah family release.
        -   Fixed issues when searching the needs attention section on the homepage.
        -   Fixed ACL issues when the ITSM roles plugin is not installed.
        -   Fixed first row indicator links on grid on overview/run tabs for taxonomy/services/offerings.
        -   Fixed an issue that required the specific "performance snapshot" KPI group to be used for all Services/Offerings. Now any KPI group can be used/mapped to any given service or offering.
        -   Fixed an issue causing the node breakdown grid to be blank if the performance snapshot is not on a page \(related to above issue\).
-   **Version 3.0.2 - November 2022**
    -   DPM highlights for v3 \(Nov release\):
        -   Added visual spark lines to key performance indicators \(KPIs\) and record views for another way to present data.
        -   Added DevOps flow metrics for the business applications Plan tab.
        -   Expanded the reporting model so you can see incidents, problems, changes, and outages related to or impacting the performance of your services and service offerings.
        -   Updated the indicators on the Performance snapshot KPI group.
        -   Added availability tracking for application services.
        -   Moved the subscriber count KPI group to meta data so it can be viewed in the headers of portfolios, taxonomies, and nodes.
        -   Added service offerings to the service portfolio Info tab.
        -   Added a Contacts tab for nodes in relationship maps.
-   **Version 2.2.20 - November 2022**
    -   The following four issues were fixed in this patch release:
        -   Fixed an issue that caused duplicate drafts of services and service offerings to be created when viewing a service in DPM.
        -   Fixed the 10-child limit on breakdown KPI view \(it's not set to 1000\).
        -   On the Application services dependencies grid: Removed dead link when Technology risk is empty.
        -   Removed an unnecessary plugin dependency \(APM\) related to application services.
-   **Version 2.2.15 - October 2022**
    -   Fixed: Minor Bug fixes
    -   Please note that there are two versions of this patch, one that is San Diego compatible \(2.2.14\), and one that is Tokyo compatible \(2.2.15\). Select 'Other App Versions' on the store page to select the option that best meets your needs.
-   **Version 2.2.13 - September 2022 \(San Diego\)**
    -   Minor Bug fixes
    -   Please note that 2.2.13 \(this version\) is compatible with San Diego, and 2.2.12 \(prior version\) is compatible with Tokyo. They are otherwise the same release.
-   **Version 2.2.12 - September 2022 \(Tokyo\)**

    Minor bug fixes

-   **Version 2.2.9 - August 2022 \(San Diego\)**

    New:

    -   Configure DPM interfaces in DPM - hide life cycle tabs and content sections on detail views.
    -   View relationship maps of services, offerings, business applications, and application services to see dependencies and understand impacts.
    -   Use updated flow changes when creating personal portfolios.
    -   Add to personal portfolios from detail views and in the enterprise portfolio preview.
-   **Version 2.1.7 - July 2022 \(San Diego\)**

    Fixed: Fixed the KPI group mappings in Service Builder when Digital Portfolio Management is enabled.

-   **Version 2.1.6 - June 2022 \(San Diego\)**

    Minor patch release

-   **Version 2.1.4 - May 2022 \(San Diego\)**
    -   New: Added Application Services \(Run and Info tabs\) for users to view application service data that affect their solutions. This addition doesn't affect the existing ability for solution owners to view the full life cycle of Plan-Build-Run for services, service offerings, and business applications. A reminder that business applications also include a Risk tab to view epics and releases in the current sprint.
    -   Changed: Made general UI changes to ensure a consistent visual experience.
-   **Version 1.0.11 - May 2022 \(Rome\)**
    -   Fixed: This is a patch of the Rome compatible version of DPM, with the following fixes:
        -   L10N and i18N fixes
        -   ACL fixes \(that were blocking other roles from accessing tables\)
        -   Fixed 500 error on the technical services info page
        -   Fixed intermitted 500 error on the personal portfolios page
        -   Fixed 3 different performance issues
        -   Fixed multi line chart visualizations in KPI groups
        -   Fixed personal portfolios empty state
        -   Fixed GRC tab on business application details page role requirements
-   **Version 2.0.6 - March 2022**
    -   Fixes
    -   Please note that there are two concurrent versions of Digital Portfolio Management. the 1.\* version is compatible with our Rome release, and the 2.\* version is compatible with the San Diego release. For the 1.\* version of Digital Portfolio Management, please install the 1.\* version of sn\_opt\_components, and for the 2.\* version of Digital Portfolio Management, please install the 2.\* version of sn\_opt\_components.
-   **Version 2.0.4 - February 2022**

    Use Digital Portfolio Management to holistically view and collectively manage serivces, applications, and products through the full lifecycle to drive aligment and deliver measurable outcomes. You can plan for, build, and run your services and applications with detailed operational and experience data all in one single location. DPM surfaces service impacts from across the platform, including outages, changes and high impact incidents.


