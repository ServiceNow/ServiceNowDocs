---
title: Privacy Management release notes
description: The ServiceNow Privacy Management application enables you to manage your organization's privacy risks and compliance to protect your customers, employees, and suppliers. Privacy Management was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
---

# Privacy Management release notes

The ServiceNow® Privacy Management application enables you to manage your organization's privacy risks and compliance to protect your customers, employees, and suppliers. Privacy Management was enhanced and updated in the Xanadu release.

## Privacy Management highlights for the Xanadu release

-   Use the Personal Data Rights application to manage personal data rights requests from your customers or consumers, and employees in compliance with global privacy regulations.
-   Establish a data lineage to visualize data consumption, sharing, and the associated risks for a processing activity.
-   Use the Smart Assessment Engine to respond to and view new control attestations related to your processing activity.
-   Create a regulatory agency library to store and access regulatory details, including correspondence with the regulators.
-   Initiate chats from privacy assessments, processing activities, privacy cases, and personal data rights requests to collaborate with various teams to ensure quick responses.

See [Exploring Privacy Management](https://www.servicenow.com/docs/access?context=explore-privacy-management&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Privacy Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Personal Data Rights](https://www.servicenow.com/docs/access?context=exploring-personal-data-rights&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Use the Personal Data Rights application that provides configurable workflows to manage and automate personal data rights requests efficiently, reducing the risk of non-compliance. The Personal Data Rights application enables customers to efficiently manage and fulfill Data Subject Access Requests \(DSARs\), consumer rights requests, and so on, ensuring compliance with privacy regulations. The application helps organizations to handle requests related to the personal data rights of their consumers while ensuring that employees can maintain data protection standards globally.

-   **[Create data lineage](https://www.servicenow.com/docs/access?context=processing-activity-hierarchy&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Establish a data lineage to understand how data is being consumed and shared in a given processing activity. Creating a data lineage also helps you to understand and manage the associated risks for the data being shared. This feature provides a visual representation of data lineage or hierarchy.

-   **[Create a regulatory agency](https://www.servicenow.com/docs/access?context=add-a-regulatory-agency&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Create regulatory agencies in the Privacy Workspace to identify the relevant regulatory authorities that are responsible for overseeing the businesses in the public interest. The centralized library consolidates all regulatory communication via emails.

-   **[Collaborate and chat with cross-functional teams for processing activities, privacy cases, privacy assessments, and personal data rights requests](https://www.servicenow.com/docs/access?context=manage-discussions-of-a-pa&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Initiate quick discussions with key stakeholders while working on a processing activity, privacy case, or a personal data rights request. The chat feature is integrated with Microsoft Teams and a group is automatically created on Microsoft Teams when a discussion is initiated. The chat conversations that take place using the **Discuss** button are stored in the respective record making it simpler for the privacy teams to refer to them when working on a task.

-   **[View smart attestations on the processing activities](https://www.servicenow.com/docs/access?context=ropa-record&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Use the Smart Assessment Engine feature to respond to attestations. View the reports of the new control attestations on the landing pages of the privacy analyst and the privacy manager. Utilize the filter in the Attestations report to select if you want to view the classic attestations or the new attestations.

-   **[Changes in roles with the Privacy Employee user application](https://www.servicenow.com/docs/access?context=roles-installed-prm&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    **Note:** Only applicable to the customers with the GRC Privacy Employee User application \(sn\_privacy\_emp\) installed.

    When you install the new GRC Privacy Employee User application and assign the sn\_privacy\_emp.privacy\_employee role to your employees, the role enables your employees to perform the following operations from the Employee Center:

    -   Proactively request privacy impact assessments \(PIAs\) for new implementations, applications, and processes from the Employee Center.
    -   Report privacy cases related to data privacy policy and regulatory violations.
    -   Read and acknowledge organizational privacy policies.
    -   Create policy exceptions.
    -   Create privacy issues.
-   **[Changes in roles with the GRC: Privacy Lite User application](https://www.servicenow.com/docs/access?context=roles-installed-prm&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    If the GRC: Privacy Lite User application \(sn\_privacy\_lite\) is installed, the following roles are considered as lite operators:

    -   sn\_privacy.business\_user
    -   sn\_privacy.assessment\_responder
    -   sn\_privacy\_case.privacy\_case\_business\_user
    -   sn\_grc\_pdr.data\_owner\_admin
    Users with the lite operator role can do the following:

    -   Respond to privacy assessment tasks as business users.
    -   Respond to the processing activity's criticality risk assessments and object-based assessment.
    -   View, update, and close assigned issues.
    -   Respond to the assigned control attestations.
    -   Respond to the assigned manual indicator tasks.
    -   Create, update, and close assigned remediation tasks.
    -   Work on the processing activity as a business user when it’s assigned to you to collect the required details.
    -   Work on breach assessments and other privacy case tasks.
    -   Respond to the detailed privacy risk assessments on each risk identified on a processing activity.
    -   Respond to the assessment and investigation tasks assigned by the privacy team.
    -   Work on personal data rights action tasks to handle data according to the requester's requests.

## Activation information

Install Privacy Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

