---
title: Document Services release notes
description: The ServiceNow Document Services application provides a broad range of services that are related to document management, such as creating, maintaining, and converting documents, as well as integrating with third parties like Microsoft SharePoint. Document Services was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# Document Services release notes

The ServiceNow® Document Services application provides a broad range of services that are related to document management, such as creating, maintaining, and converting documents, as well as integrating with third parties like Microsoft SharePoint. Document Services was enhanced and updated in the Zurich release.

## Document Services highlights for the Zurich release

-   Compare any two document versions and track changes by using document comparison.
-   Connect and manage external cloud documents by uploading files, storing URLs, and syncing metadata with your records.
-   Authenticate with your personal accounts on an external cloud, Microsoft OneDrive, or Google Drive.
-   Control public sharing by using document classification to ensure document security.
-   Accelerate documents insights with instant summaries for highlights and quick insights, interactive Q&amp;A, and FAQs.

See [Document Services](https://www.servicenow.com/docs/access?context=document-services-landing-page&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.

**Important:** Multi Provider Document Services Framework is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Document comparison](https://www.servicenow.com/docs/access?context=compare-document-version&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Compare two versions of the document side by side.

-   **[Guardrails for PDF generation and accessibility](https://www.servicenow.com/docs/access?context=guardrails-pdf-generation-accessibility&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Use static and dynamic guardrails to help maintain stability during PDF generation and accessibility.

-   **[Smart Documents](https://www.servicenow.com/docs/access?context=configure-skill-smart-documents&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Accelerate insights with quick summaries, dynamic Q&amp;A, and FAQs that reduce time spent searching for information


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Upload to provider button](https://www.servicenow.com/docs/access?context=upload-external-provider&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    The **Upload to provider** button was changed to **Upload to cloud** button within the Connect with external cloud dialog box.

-   **[Sync button](https://www.servicenow.com/docs/access?context=sync-versions&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    The **Sync** button was changed to the **Download from Cloud** button.

-   **[Upload to cloud button](https://www.servicenow.com/docs/access?context=upload-versions-external-cloud&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    The **Upload to cloud** button has been added for versions.

-   **[External Provider Settings tab](https://www.servicenow.com/docs/access?context=sync-versions&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    The **External Provider Settings** tab was changed to the **External Cloud Settings** tab.

-   **[Summarize button](https://www.servicenow.com/docs/access?context=configure-skill-smart-documents&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    The **Summarize** button was changed to the **Ask Now Assist** button.


## Changed in this release

-   **[Connect documents on external cloud](https://www.servicenow.com/docs/access?context=upload-versions-external-cloud&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Upload your files directly to an external cloud \(including multiple versions of the document\).

-   **[Permissions for external cloud files](https://www.servicenow.com/docs/access?context=document-configuration&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Set the sharing permissions on your external cloud files.

-   **[Authenticate personal accounts on external cloud](https://www.servicenow.com/docs/access?context=personal-authentication-documents&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Implement personal token-based authentication for an external cloud so that you can verify user-specific access, audit trails, and compatibility with existing and future integrations.

-   **[Connect file extensions](https://www.servicenow.com/docs/access?context=upload-versions-external-cloud&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Link any Google Drive file to a document record by selecting a provider and entering the file URL All file extension are now supported.

-   **[HTML to PDF Conversion](https://www.servicenow.com/docs/access?context=pdf-generation-accessibility&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Specify an image retrieval timeout for HTML to PDF conversion.

-   **[Document classification](https://www.servicenow.com/docs/access?context=share-document-link&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Limit public sharing based on a document's classification.

-   **[PDF generation](https://www.servicenow.com/docs/access?context=pdf-generation-accessibility&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Generate a PDF with accessibility for regulated markets.

-   **[Property value for digital signature using CAC or PIV smart cards](https://www.servicenow.com/docs/access?context=property-value-cac-piv-signing&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Specify the method used to identify and validate the user who has signed the PDF using the property value.

-   **Document summarization**

    Use AI to generate summaries for feedback, disclaimers, and usage tracking in PDFs and Microsoft Word files.

-   **[Document Services Framework for Microsoft OneDrive](https://www.servicenow.com/docs/access?context=onedrive-spoke-document-services-framework&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Retrieve the list of files and folders based on the given search query from Microsoft OneDrive.

-   **[Document Services Framework for Google Drive](https://www.servicenow.com/docs/access?context=google-drive-spoke-document-services&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Retrieve the list of files and folders based on the given search query from Google Drive.


## Activation information

Document Services is a ServiceNow AI Platform feature that is active by default.

Document Management is available with activation of the Document Management plugin \(com.snc.platform\_document\_management\). For more details, see [Activate Document Management](https://www.servicenow.com/docs/access?context=activate-doc-mgmt-plugin&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

Multi Provider Document Services Framework needs to be installed by requesting it from the ServiceNow Store. For more information, see [Multi Provider Document Services Framework](https://www.servicenow.com/docs/access?context=mp-document-services-framework-landing&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.

-   **[Guardrails for PDF generation and accessibility](https://www.servicenow.com/docs/access?context=guardrails-pdf-generation-accessibility&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Added static and dynamic guardrails for accessibility support for PDF document generation

-   **[PDF generation and accessibility](https://www.servicenow.com/docs/access?context=pdf-generation-accessibility&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Added support for PDF document generation with accessibility for regulated markets.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](now-platform-capabilities-rn-landing.md)

