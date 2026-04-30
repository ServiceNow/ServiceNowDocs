---
title: Privacy Management release notes
description: The ServiceNow Privacy Management application enables you to manage your organization's privacy risks and compliance to protect your customers, employees, and suppliers. Privacy Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Privacy Management release notes

The ServiceNow® Privacy Management application enables you to manage your organization's privacy risks and compliance to protect your customers, employees, and suppliers. Privacy Management was enhanced and updated in the Yokohama release.

## Privacy Management highlights for the Yokohama release

-   Integrate criticality factors into assessments and processing activities thereby simplifying the assessment process, and reducing the workload for privacy teams.
-   Use the Smart Assessment Engine to capture details regarding information objects and hierarchies, updating all details within the assessments and eliminating the need to separately update processing activities.
-   Implement information Object \(IO\) categories such as biometric data, to align with regulatory classifications and bridge the gap between requirements and user understanding.
-   Empower privacy case analysts to perform assessments on privacy cases using the Smart Assessment Engine

See [Privacy Management](https://www.servicenow.com/docs/access?context=privacy-management&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Privacy Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   ****

    Leverage criticality factors to evaluate the initial risks associated with processing activities. Integrate these factors into privacy assessments and automatically generate a criticality score upon assessment approval. These factors are also added to processing activities, enabling you to make updates at any time. Integrating these factors in a privacy assessment eliminates the need for a separate criticality assessment. This consolidation reduces the workload for the privacy teams.

-   **[Smart assessments in Privacy Management](https://www.servicenow.com/docs/access?context=smart-assessments-in-privacy-management&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Use the new and improved assessment experience that enables:

    -   capturing the data elements, the information object attributes, hierarchies
    -   building the assessment questionnaire
    This new experience enables responders to update all the necessary details within the assessments, eliminating the need to update the processing activity separately.

-   **[Configure information object categories](https://www.servicenow.com/docs/access?context=configure-information-object-categories&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Implement Information object categories to tag and classify information objects effectively. For example, attributes like iris scans and fingerprints are often referred to as biometric data, or email addresses and phone numbers can be tagged as contact information. Information object categories enable you to categorize these information objects under these broader classifications. This approach is useful in the following ways:

    -   Enhances compliance with regulations such as GDPR, CCPA, and so on by accurately capturing and tracking required data categories.
    -   Improves clarity for business users, ensuring they can easily identify and work with terms they’re familiar with while adhering to regulatory standards.
    -   Streamlines data governance by creating a structured framework that supports both regulatory needs and business operations.
-   **[Smart assessment for privacy case management action tasks](https://www.servicenow.com/docs/access?context=accept-a-case-task&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Use the new assessment experience of Smart Assessment Engine for privacy case action tasks. Only when an action task moves from the **Draft** to the **Assigned** state, the assessment can be sent. To use the smart assessment, a new property called enable\_smart\_assessments \(sn\_grc\_case\_mgmt.enable\_smart\_assessments\) is introduced with the default value as **true**.


## Changed in this release

-   **[Tagging of information object tags](https://www.servicenow.com/docs/access?context=tag-io-with-pi&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Use the **Data classification** field to tag information objects instead of using the tag icon.

-   **[Initiating privacy assessment](https://www.servicenow.com/docs/access?context=send-privacy-asmt-from-pa&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    When you initiate a privacy assessment from either an entity or a processing activity, you’re no longer redirected to the **Create new privacy assessment form**, instead, a new pop-up window appears where you can specify all the assessment details.


## Activation information

Install Privacy Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

