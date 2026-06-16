---
title: Workplace Case Management release notes
description: Version history for the Workplace Service Delivery Workplace Case Management on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-wsd-workplace-case-management.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 14
breadcrumb: [ServiceNow Store - Workplace Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Workplace Case Management release notes

Version history for the Workplace Service Delivery Workplace Case Management on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.28.3 - June 2026**
    -   New: List &amp; Calendar for cases. View and manage workplace cases on a new Calendar view in Workplace Central under Case Management module, with click-through to a side panel for quick case details and actions. Unified filters apply and retain across the Calendar and List View with ability to Group Cases on the Calendar View.
    -   Changed:
        -   Unified record page experience in Workplace Central. Workplace case pages now use the standard record page for a consistent navigation and editing experience in Workplace Central
        -   Accessibility compliance. Workplace Case Management core UI now meets WCAG 2.2 AA standards, including 400% zoom and reflow support.
    -   Fixed:
        -   Service items added to a reservation via an update are no longer removed unexpectedly.  \{PRB2001559\}
        -   Capacity limits configured on workplace service items are now correctly enforced in the Catalog Items as well.  \{PRB2010040\}
        -   Editing a WSD request form no longer leaves a blank space on the form.  \{PRB1955789\}
        -   Editing a standalone workplace case no longer creates duplicate service item requests.  \{PRB2019226\}
        -   The 'Requested For' user can now add comments and approve or reject a solution when a case is in the Awaiting Acceptance state.  \{PRB2008061\}
        -   Workplace service templates no longer override descriptions and short descriptions entered by the user.  \{PRB1994849\}
        -   Location availability restrictions on a Workplace Service Location are now enforced when a request is submitted through the Record Producer path.  \{PRB2000468\}
        -   The 'KB articles read by user' tab on the case page is now accessible.  \{PRB2000894\}
-   **Version 1.27.5 - May 2026**

    Increasing version number to align with the releases.

-   **Version 1.27.3 - April 2026**

    New: Image to Case - Employees can now upload a photo of workplace issues \(broken furniture, spills, damaged equipment\) via Now Assist Virtual Agent to automatically create a Workplace Case. The system analyzes the image to populate case details and infers the location from the user's workplace profile, making it faster and easier to report workplace issues. This uses the Platform agent called Image Processing Agent.

-   **Version 1.26.1 - March 2026**
    -   New:
        -   Admins can now create conditional Smart Assessment Templates that attach to Workplace Cases and Tasks. Fulfillers can complete assessments in-line in Workplace Central, with automated follow-up task creation based on responses.
        -   The Workplace IFM Integration Framework enables Workplace Cases and Tasks to route, sync orchestration, and sync history logging with external \(FM\) provider systems.
    -   Fixed:
        -   In some cases, conditional service activities were not correctly triggered.
        -   Submitting a move request without extra items did not trigger subsequent activity tasks.
        -   The message informing users about requesting services within the lead time was always displayed to admins.
        -   The total cost was not calculated and saved when a request was made through the record producer.
        -   Delivery time was incorrectly updated after adding a service to an existing reservation.
        -   Approval workflows were re-triggered on the parent Workplace Case when a child task is created manually and then closed.
        -   The state of the parent case was incorrectly changed when the associated automated task was set to “Close – Skipped”.
        -   Adding a service to an existing reservation with completed cases could update the parent’s state to “Closed – Incomplete”.
        -   Updating services on existing requests could take a long time.
        -   Variables available on the Workplace Case were not always updated after editing an existing request
        -   Improved translations.
-   **Version 1.25.0 - December 2025**
    -   New: Introduction of the order column on Service and Service Item Tables
    -   Fixed:
        -   The "Short Description" does not copy from the Universal Request to the Workplace Case after "Transfer".
        -   Issues &amp; Performance Improvements in Case Edit.
        -   Service loading performance improvement.
        -   Cases are not re-triggering in Reconfigure an office space workplace service after edit.
        -   Flow column is not populating with the workplace manager role and workplace case manager role. Workplace case manager is not able access the flow details.
        -   In General request, RP Short description are not getting updated after edit.
-   **Version 1.24.4 - September 2025**

    Workplace Case analyzing AI agent - Handle required changes to comply with the AI Security Directive

-   **Version 1.23.1 - August 2025**
    -   New: Generate delivery reports for workplace cases, workplace tasks, and workplace reservations.
    -   Changed:
        -   Use the new neighborhood tables, which are part of Workplace Core.
        -   The banner image for the workplace dashboard has been updated.
    -   Fixed:
        -   Creating a case on an asset through the catalog sets the state to draft.
        -   When switching to certain languages, the interactive floor map in the Request Furniture catalog item could not be opened.
        -   The name of the user in the salutation could be cut in case the name contains a hyphen.
        -   Sometimes, services could not be retained when editing the requested service using the catalog.
        -   Sometimes, lead time is not working with different time zones.
        -   Sometimes, code was displayed in the email templates sent after assigning a case to an individual or group.
        -   Workplace Case Managers could not assign cases in the platform experience.
        -   The service types pop-up used when creating a new case in Workplace Central did not support translations.
        -   The Open critical cases label in Workplace Central did not support translations.
        -   Workplace Service Items were not sorted alphabetically when selecting them in the Workplace Reservation experience.
-   **Version 1.21.3 - May 2025**
    -   New:
        -   Changes made to requested services will not recreate existing cases.
        -   Employees will be able to edit requested services by opening the request in the My Request overview.
    -   Changed:
        -   Users with the Workplace Agent role can manage cases through Workplace Central.
        -   List overviews on the Case Management Dashboard are moved to a dedicated List section within Workplace Central.
    -   Fixed:
        -   Clicking the New button always launched the General Submit record producer and ignored the selected workplace service.
        -   In some cases, the space assist request could be in an in-progress state forever.
        -   Subsequent child cases were not always created to move users after deploying a scenario plan.
        -   The label "Find the space on a floor map" in the furniture request did not support translation.
        -   Security fixes
-   **Version 1.20.0 - February 2025**
    -   Fixed:
        -   Service categories and Service subcategories were incorrectly sorted when using the Outlook add-in.
        -   Invalid reference to a non-existing workplace service was included in the demo data.
        -   Deleting a location which was assigned to a workplace service will leave an empty Workplace Service Item Location record, making the service unavailable for other locations.
        -   Improved support for translations
        -   Security fixes
-   **Version 1.19.0 - November 2024**
    -   New:
        -   Employees can now submit space arrangement requests for a reservation, parking, furniture and general requests through MS Places.
        -   Employees can submit a case after selecting a space from the location directory.
    -   Fixed:
        -   The conflict message indicates that the spaces are already allocated to a different department when the request and system property are based on the cost center.
        -   On the child task creation screen, changing the task type should reveal the relevant specific fields.
        -   Accessibility improvements have been made.
        -   Security fixes.
        -   Performance improvements.
-   **Version 1.18.0 - August 2024**
    -   New:
        -   Employees will now be able to request catering, equipment and support services independent of the reservations. However, they can link it to existing reservations as well.
        -   New services like badge request, cleaning, heating &amp; cooling are available out-of-the-box.
    -   Changed: UI improvements in record producers for fresh and modern design.
    -   Fixed:
        -   Filters applied in the Case Management report in Workplace Central updated the single scorecards. This has been fixed.
        -   Fulfillment instructions were not displayed for Maintenance and Move cases. This has been fixed.
        -   The Space assist request did not show any selection in Workplace Central, even if the requester selected an option in the record producer. This has been fixed.
        -   Opening the delivery case created for requested services in a reservation could show multiple replacement case numbers. This has been fixed.
        -   Creating a new case for a service could overwrite the short description to match the template. This has been fixed.
        -   When creating a general request and only selecting the building and floor, the workplace location field did not show the floor but was empty instead. This has been fixed.
        -   In some cases, removed service items were not listed after the services were edited on the reservation. This has been fixed.
-   **Version 1.17.0 - May 2024**
    -   New:
        -   Introduced Case Management module in the Workplace Central workspace for case managers and workplace coordinators.
            -   The landing page provides key metrics related to cases like open cases, unassigned cases, the cases that have SLA breached. The page also displays charts with details of the volume of cases and cases opened vs closed.
            -   You can make bulk assignments and view details of cases like the employee's information, location requiring attention, templates, fulfillment instructions, etc. with an intuitive experience.
    -   Fixed:
        -   Localization-related issues have been fixed.
        -   The Aria label has been fixed in the case record producers.
-   **Version 1.16.0 - February 2024**
    -   Changed: The Workplace Case Dashboard can now be accessed from the Workplace Central workspace. Customers who have installed 1.15.1 or earlier versions of the app can still access the old version of the dashboard. Customers installing the app for the first time from 1.16.0 version onwards can access the dashboard in Workplace Central only.
    -   Fixed:
        -   The username of the employee who created the case was cut off in the email when additional comments were added.
        -   Parts of the additional details sometimes show as undefined.
        -   Opening case details from an email while using mobile, opens the new case form.
-   **Version 1.15.2 - January 2024**

    Security fixes.

-   **Version 1.15.1 - November 2023**

    Changed: The Workplace Case Dashboard can now be accessed from the Workplace Central workspace. Download the Workplace Central plugin and access the dashboard from the Workplace Dashboards tab.

-   **Version 1.14.0 - August 2023**
    -   New:
        -   Add descriptions to services and service items that will be visible for employees while ordering them as part of a reservation. Descriptions can contain formatting, links, and more.
        -   Introduce additional archiving configuration.
    -   Fixed:
        -   Granular ACL improvements with reporting to prevent unauthorize access to sensitive column data.
        -   Earlier, incorrect prep or clean-up times were used to create the blockers meetings when both the space and its floor or the building were configured in the Workplace Service Item Locations. This has been fixed.
        -   Earlier, the 'Workplace Service Activities Subflow' could generate an error as an empty object was passed. This has been fixed now.
-   **Version 1.13.0 - May 2023**
    -   New:
        -   Improved information on cases and tasks supporting the delivery of ordered services that are part of a reservation.
            -   The form and list views are extended to also show reservation-related information supporting the delivery.
            -   A summary is added to the new case, listing out changes made for the requested services.
            -   The costs for services are visible on case and task levels.
    -   Fixed:
        -   Earlier, imported workplace services were not available for ordering while making a reservation. This has been fixed now.
        -   Earlier, the requested value for parent reservations did not show the correct name. This has been fixed now.
-   **Version 1.12.1 - February 2023**
    -   New: Report a case on enterprise assets
    -   Changed: Default email templates are updated to match the next experience content and style guidelines. The new templates are installed beside the old ones in cases the old ones already exist on the instance.
    -   Fixed
        -   Earlier, submitting a general request, space name and floor values were not auto-populated after selecting a space using a MappedIn foormap. This has been fixed now.
        -   Earlier, there were issues with restricted caller access in some cases. This has been fixed now.
-   **Version 1.11.0 - November 2022**

    New: Perform single-user move requests generated from a scenario plan deployment, and manage employee space assignment changes.

-   **Version 1.10.0 - August 2022**

    Changed: Added 'Title' field to the record producers to support translations accordingly.

-   **Version 1.9.2 - May 2022**
    -   New
        -   Browse through the map, navigate to a location, or create a case using the new Indoor Mapping plugin.
        -   View locations that do not have a floor map in a list view. Allow employees to report a case on any location directly from the list view.
    -   Fixed: Earlier, conditions were not validated correctly when handling the approval type.
-   **Version 1.8.3 - February 2022**
    -   New
        -   You can now configure specific users and assignment groups as approvers for workplace cases.
        -   You can now create workplace services that can be requested as part of reservations.
    -   Changed
        -   You can now manage approval assignments through the Performer Criteria in Workplace Safety Management.
        -   A workplace service item will now be available to all locations if it is not assigned to any specific location.
    -   Removed: The option to configure the Approval Options configuration is removed.
-   **Version 1.7.1 - December 2021**
    -   New: Users can now generate and print QR codes to enable employees to create a case or check-in and check-out their reservation.
-   **Version 1.6.6 - October 2021**
    -   New: The application now provided additional support for all the 22 languages that are currently available across the ServiceNow AI Platform.
    -   Fixed: The 'Request a desk change' and 'Request furniture' out-of-the-box services were unavailable to access in the Employee Center portal.
-   **Version 1.6.3 - September 2021**
    -   New
        -   The application now enables you to configure service items as part of workplace services. You can execute service activities against the service items selected by employees via the portal request form.
        -   You can apply different templates on both the workplace services and the service activity levels based on the employee responses in the portal request form.
        -   You can configure field mappings to copy data from the parent case to the child tasks.
    -   Changed: You can configure multiple record producers for a workplace service so that you have different forms for both portal and the platform.
-   **Version 1.5.3 - June 2021**
    -   New:
        -   A Parent-Child case relationship is introduced to manage duplicate cases.
    -   Changed:
        -   The case management form view will now display the record producer variables.
        -   A Dynamic workflow engine is being used for case management.
-   **Version 1.4.1 - March 2021**
    -   New:
        -   You can configure a workplace service as a Universal request. Workplace Service Delivery is integrated with Universal requests.
        -   You can create a workplace case from a universal request.
        -   You can transfer a workplace case to a universal request or to another department. New location fields are added in the 'Submit a general inquiry' workplace service form in the Workplace Service portal.
-   **Version 1.3.1 - December 2020**
    -   No new updates for this release
-   **Version 1.2.2 - November 2020**
    -   New:
        -   Configure fulfillment instructions to resolve a workplace case.
        -   Create an escalation rule to escalate a workplace case.
        -   Virtual agent chat support to request general workplace service help.
    -   Changed:
        -   From Workplace Safety Management \(sn\_wsd\_core\) version 2.1, all updates, and new features are available only on the Workplace Service Portal. The workplace services provided by ServiceNow® are removed from the Service Portal from Workplace Safety Management \(sn\_wsd\_core\) version 2.1.
        -   The Workplace Case Dashboard is now accessible only from the Workplace Safety Management application.
        -   The mobile web interface has been improved in the Now Mobile app.
        -   The Workplace Services Catalog can also be accessed from the Now Mobile app homepage.
-   **Version 1.0.2 - October 2020**
    -   New: Workplace Case dashboard to track the workplace cases on any day

## Notice regarding use by organizations

All decisions in connection with the implementation of this application are at the sole decision of the Organization utilizing this application. Organizations agree that use of the application is not a representation by ServiceNow regarding the application’s compliance with any law or regulation and any suggested language provided out of the box with the application does not constitute legal advice by ServiceNow.

Organizations remain solely responsible for complying with their legal obligations under applicable law, including \(but not limited to\) data protection and employment laws, and should modify any language within the templates provided to meet the Organizations' specific requirements.

## Notice regarding use by government agencies

ServiceNow is offering this application to government agencies and their authorized users, not to government employees in their individual capacities. Use of the application does not modify any existing, or future entitlements or payment obligations for ServiceNow software or applications otherwise purchased by the government agency. ServiceNow shall not be responsible for any implementation or configuration costs associated with use of the application unless separately purchased. Government customers are solely responsible to confirm with the agency’s Ethics Office or its authorized representative that acceptance and usage of the application is permissible.

All decisions in connection with the implementation of this application are at the sole decision of the government agency utilizing this application. Agencies remain solely responsible for complying with their legal obligations under applicable laws and regulations, including \(but not limited to\) data protection and employment laws and regulations, and should modify any language within the templates provided to meet the agency’s specific requirements.

**Parent Topic:**[ServiceNow Store - Workplace Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-wsd-highlight.md)

