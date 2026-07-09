---
title: Healthcare Operations Core release notes
description: The ServiceNow Healthcare Operations Core application streamlines and optimizes healthcare team operational tasks. Healthcare Operations Core was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-11-04"
reading_time_minutes: 2
---

# Healthcare Operations Core release notes

The ServiceNow® Healthcare Operations Core application streamlines and optimizes healthcare team operational tasks. Healthcare Operations Core was enhanced and updated in the Zurich release.

## Healthcare Operations Core highlights for the Zurich release

-   Leverage the streamlined launch context when embedding Care Team Portal into electronic medical record \(EMR\) systems.
-   Assign roles and responsibilities more efficiently with an updated user configuration process.

See [Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/healthcare-life-sciences/hcls-cto-app.md) for more information.

**Important:** Healthcare Operations Core is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Changed in this release

-   **[Embedding Care Team Portal in Epic Hyperspace via Hyperdrive](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/healthcare-life-sciences/configure-care-team-portal.md)**

    The process for embedding Care Team Portal into your EMR system has been streamlined to enable more efficient launch context configuration.

    The portal now supports capturing launch context tokens across multiple launches within the same Hyperspace session when embedding Care Team Portal into Epic's Hyperspace. Previously, only tokens captured from the initial launch were displayed.

    The FHIR endpoint is now retrieved dynamically, eliminating the need to embed it directly in the Single Sign-on Script.

-   **[Setting up roles and responsibilities for Healthcare Operations users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/healthcare-life-sciences/cto-setting-up-roles-responsibilities.md)**

    Roles and responsibilities have been updated to enable more selective user access.

    The following responsibilities were added in Healthcare Operations Core:

    -   Support Department Agent
    -   Support Department Manager
    The following responsibilities were renamed in Healthcare Operations Core:

    -   Team Member has become Care Team Member
    -   Team Manager has become Care Team Manager
    Healthcare operations users can now be assigned these responsibilities in the Edit member related list within healthcare organizations.


## Activation information

Install Healthcare Operations Core by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Care Team Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/healthcare-life-sciences/care-team-mobile-landing.md)**

    ServiceNow® Care Team Mobile provides a mobile experience for hospital care teams to report issues to support departments.

-   **[Care Team Operations for Healthcare IT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/healthcare-life-sciences/hcls-cto-it-app.md)**

    ServiceNow® Care Team Operations for Healthcare IT contains the case types to report and fulfill healthcare IT issues and uses the Healthcare Operations Core data model from the Healthcare Operations Core application.

-   **[Care Team Operations for Biomed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/healthcare-life-sciences/care-team-operations-for-biomed.md)**

    ServiceNow® Care Team Operations for Biomed contains the case types to report and fulfill healthcare biomed issues and uses the Healthcare Operations Core data model from the Healthcare Operations Core application.

-   **[Care Team Operations for Facilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/healthcare-life-sciences/cto-facilities-landing.md)**

    ServiceNow® Care Team Operations for Facilities contains the case types to report and fulfill facilities issues in healthcare spaces and uses the Healthcare Operations Core data model from the Healthcare Operations Core application.

-   **[Care Team Operations for Environmental Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/healthcare-life-sciences/cto-evs-landing.md)**

    ServiceNow® Care Team Operations for Environmental Services contains the case types to report and fulfill environmental issues in healthcare spaces and uses the Healthcare Operations Core data model from the Healthcare Operations Core application.


**Parent Topic:**[Healthcare and Life Sciences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/healthcare-life-sciences-rn-landing.md)

