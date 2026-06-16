---
title: Document Intelligence release notes
description: Version history for the Document Intelligence application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-nowintel-document-intelligence.html
release: store
topic_type: reference
last_updated: "2025-09-10"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Platform Analytics release notes, ServiceNow Store release notes]
---

# Document Intelligence release notes

Version history for the Document Intelligence application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 7.1.5 - September 2025**

    Changed: UI changes to support Now Assist in Document Intelligence

-   **Version 7.0.10 - August 2025**

    Added support for Coral theme.

-   **Version 7.0.1 - June 2025**

    User interface \(UI\) fixes.

-   **Version 7.0.7 - May 2025**

    No updates.

-   **Version 6.0.0 - February 2025**

    Fixed: Issues with Draw tool.

-   **Version 5.2.1 - November 2024**
    -   New: UI improvements for Now Assist in Document Intelligence use cases
    -   Changed: UI/UX improvements for draw tool for single fields
    -   Fixed:
        -   Fixes to data normalization for ambiguous dates
        -   Fixes to data normalization for reference fields
-   **Version 5.1.0 - September 2024**
    -   New: Extract data from single fields using the draw tool to select a document area and extract the information.
    -   Changed: Ensure check box selection, row number, status, and row actions columns are visible at all times in the table section.
    -   Fixed:
        -   Fixes to ambiguity handling logic for dates, numbers, and references.
        -   Inactive fields are now hidden from the agent workspace.
-   **Version 5.0.1 - August 2024**
    -   New:
        -   Support for reflow
            -   Enables pages and content to be zoomed up to 400% through browser settings without loss of content or functionality
            -   Data normalization enhancements
                -   Ability to match extracted field values with fields in a referenced table record
                -   Better handling for ambiguous values for date and number fields
            -   Document classifier improvements
                -   New out-of-the-box integration flows: Process Task, Extract Values, Map to Document Data Extraction Use Case
                -   More informative error and warning messages
            -   Support for Chinese and Japanese languages
    -   Fixed:
        -   Usability improvements to Draw tool features
        -   Usability improvements to Table section
    -   Removed: The legacy Platform Document Intelligence Usage dashboard is no longer supported or available through the Document Intelligence application \(now available in the Admin experience\)
-   **Version 4.1.6 - March 2024**
    -   New: New option to mark a blank page when classifying a document.
    -   Changed:
        -   Updated features of the draw tool for a better user experience when extracting tables
        -   Various improvements to increase user accessibility
    -   Fixed:
        -   More robust automated saving mechanism for large tables
        -   Date normalization for table fields
        -   Chrome browser warnings when attempting to close the DocIntel workspace
-   **Version 4.0.0 - February 2024**
    -   New: Extract data from tables easily using the draw tool on an area on the document you want to extract
    -   Changed:
        -   Various table extraction features are updated to create a more consistent user experience
        -   The file size limit for attachments is increased to 10 MB
        -   The default maximum number of document tasks processed per instance per day is increased to 2,000
        -   More streamlined input form and better error handling when creating document classifier use cases
        -   Various accessibility improvements
    -   Fixed:
        -   Issues with the duplicate use cases and export use case functionalities
        -   Issues with how accuracy values are calculated and shown in dashboards
-   **Version 3.1.1 - September 2023**
    -   New:
        -   Document extraction: New field types available \(date, integer, decimal, float\)
        -   Document classifier: Document-level predictions for multi-page documents
    -   Fixed:
        -   Localization of the DocIntel workspace in languages other than English
        -   Document classifier: fixed a number of small UI/UX issues
        -   Document classifier: Autofill mode now correctly populates values
-   **Version 3.0.0 - August 2023**
    -   New:
        -   Document classifier feature, enabling you to categorize incoming documents
        -   Support for dark theme
    -   Changed:
        -   More granularity for straight-through processing mode, enabling you to define fields to consider for full automation
        -   Improvements to the table extraction experience: ability to adjust column width, ability to insert a new row in arbitrary locations
-   **Version 2.4.2 - June 2023**

    Fixed: Issues with application version upgrade \(unable to display tasks created previously; existing trained models fail to upgrade and show as untrained\).

-   **Version 2.4.0 - March 2023**
    -   New:
        -   Check box extraction user experience
        -   Ability to clone an existing use case
        -   'Field group' group type to logically group fields together
    -   Changed: Provide read-only access to the DocIntel workspace for the sn\_docintel.viewer role
-   **Version 2.3.2 - February 2023**
    -   New:
        -   New user experience for extracting information from tables
        -   Ability to process multiple documents concurrently
    -   Changed: Key terminology across the product
    -   Fixed: More robust saving mechanism
-   **Version 2.2.0 - November 2022**
    -   Fixed:
        -   Reviewed fields are marked as still needing review after page refresh
        -   Inability to type "/" character on certain keyboard layouts
        -   Version upgrade fixes
        -   Accessibility fixes
-   **Version 2.1.0 - September 2022**
    -   New:
        -   Support for table extraction in Autofill and Straight-through processing modes, for simple tables that have an explicit grid and span a single page.
        -   Automatically predict whether a given attribute is present or not in a document
        -   Ability to link a key group target record with a parent record
    -   Fixed:
        -   Fixes for the Process Task and Extract Values integration flows
        -   Additional validations to prevent unsupported user actions
-   **Version 2.0.1 - August 2022**
    -   New:
        -   Extract information from lists and tables, where the number of data items is not known beforehand \(supported in Recommend mode only\)
        -   Improved out-of-the-box workflow integration experience via Flow Designer actions and flow templates
        -   Straight-through processing mode: extraction information automatically \(without user input\) when predefined conditions are met
    -   Fixed:
        -   Bugs in the training and prediction AI workflows
        -   Bugs related to roles and permissions
-   **Version 1.0.1 - July 2022**
    -   Fixed:
        -   Issue that prevented the UI from loading on some instances
        -   Issue that prevented the submission of retraining jobs in specific scenarios
-   **Version 1.0.0 - May 2022**

    Document Intelligence is an intuitive and flexible application for dynamic businesses with highly variable document processing needs that change over time. You define what information you want to extract from your documents and then teach AI models to extract that information through our user-friendly interface. Over time, the application gets better and better, making it faster for you to extract data from your documents and eventually enabling full automation if desired.


**Parent Topic:**[ServiceNow Store - Platform Analytics release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-air.md)

