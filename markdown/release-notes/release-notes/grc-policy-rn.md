---
title: Policy and Compliance Management release notes
description: The ServiceNow Policy and Compliance Management application provides a centralized process for creating and managing policies, standards, and internal control procedures that are cross-mapped to external regulations and benchmarks. Policy and Compliance Management was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
---

# Policy and Compliance Management release notes

The ServiceNow® Policy and Compliance Management application provides a centralized process for creating and managing policies, standards, and internal control procedures that are cross-mapped to external regulations and benchmarks. Policy and Compliance Management was enhanced and updated in the Xanadu release.

## GRC: Policy and Compliance Management highlights for the Xanadu release

-   Revise your policies and update the policy text periodically by integrating with Microsoft SharePoint.
-   Use policy authoring and the redlining feature to enable policy owners and reviewers to collaborate, review, and redline policies.
-   Perform a Cyber Risk Institute \(CRI\) assessment on a company as an entity to determine its control status and calculate the assessment score.
-   Use the employee operator role introduced in Policy and Compliance Management for operations in Employee Center.

See [Policy and Compliance Management](https://www.servicenow.com/docs/access?context=r_PolicyComplianceMgmt&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Policy and Compliance Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Upload policy document from your local machine to Microsoft OneDrive](https://www.servicenow.com/docs/access?context=upload-word-doc-onedrive&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Upload a Microsoft Word document that exists in your local machine to Microsoft OneDrive and link the document with the policy. You can access the document from any device and enable multiple users to collaborate on the policy document.

-   **[Create and associate a policy text document in Google Drive](https://www.servicenow.com/docs/access?context=create-policy-redlining-docu-google-drive&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Integrate your ServiceNow instance with Google documents to manage documents in Google Drive. Create a Word document in Google Drive that you can access through a browser and store in Google Drive. You also have the option to create a Microsoft Word document that you can manage in Google Drive.

-   **[Upload policy document from your local machine to Google Drive](https://www.servicenow.com/docs/access?context=upload-word-doc-googledrive&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Upload a Microsoft Word document that exists in your local machine to Google Drive and link the document with the policy to enable multiple users to collaborate on the policy document.

-   **[Upload policy document from your local machine to Microsoft SharePoint](https://www.servicenow.com/docs/access?context=upload-word-doc-sharepoint&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Upload a Microsoft Word document that exists in your local machine to Microsoft SharePoint and link the document with the policy to enable multiple users to collaborate on the policy document.

-   **[Policy authoring using Microsoft SharePoint](https://www.servicenow.com/docs/access?context=connect-sharepoint-doc&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Monitor and revise your organization's policies at regular intervals to maintain their relevance and compliance. Integrating Microsoft Word document files with multiple Microsoft SharePoint sites helps your policy owners, reviewers, and approvers to author, modify, and maintain different versions of a policy text and thus retain its history. You can also collaborate on policy drafting and review processes. The policy text is updated automatically. You can copy and paste text from a document into the **Policy text** field in HTML and then convert it to a PDF format.

-   **[Using CRI assessment questions to profile an entity](https://www.servicenow.com/docs/access?context=perform-cri-assess-pc-ws&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Perform a CRI tiering assessment for an entity to determine its tier, and then perform a CRI assessment for that entity. Based on the response to the CRI questionnaire from the assessor, the compliance status of each mapped control to a question is determined. The overall compliance score of the entity is also calculated.

-   **[User role enhancements in Policy and Compliance Management](https://www.servicenow.com/docs/access?context=manage-pol-comp-emp-center&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Respond to policy acknowledgments and request a policy exception from the Employee Center portal with the employee operator role.


## Changed in this release

-   **[Perform CRI tiering questionnaire to determine the tier value of entity](https://www.servicenow.com/docs/access?context=perform-cri-tier-pc-ws&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    In addition to the Entity owner, the Corporate compliance manager \[sn\_compliance\_ws.corporate\_compliance\_manager\], Corporate compliance analyst \[sn\_compliance\_ws.corporate\_compliance\_analyst\], and IT compliance manager \[sn\_compliance\_ws.it\_compliance\_manager\] can trigger CRI tiering questionnaire and initiate CRI profile assessments.

    -   UI action button **Initiate CRI tiering assessment** has been renamed as **Initiate CRI tiering questionnaire**.
    -   UI action button **Initiate CRI assessment** has been renamed as **Initiate CRI profile assessment**.
-   **[Domain separation in GRC: Policy and Compliance Management](https://www.servicenow.com/docs/access?context=domain-separation-pol-comp&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Now both manually created records and auto-generated records created through scheduled jobs or scripts are domain separated based on their parent object or user domain for all Policy and Compliance Management objects.


## Activation information

Install Policy and Compliance Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Browser requirements

GRC: Policy and Compliance Management requires the latest public release and two previous release versions of the following browsers:

-   Google Chrome
-   Firefox and Firefox Extended Support Release \(ESR\)
-   Microsoft Edge Chromium
-   Safari 12.0 and later versions

**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

