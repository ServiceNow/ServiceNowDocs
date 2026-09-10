---
title: AI Data Kit release notes
description: Version history for the AI Data Kit application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-now-assist-data-kit.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications version history release notes, ServiceNow Store - ServiceNow AI Platform Capabilities version history release notes, ServiceNow Store version history release notes]
---

# AI Data Kit release notes

Version history for the AI Data Kit application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 9.0.4 - September 2026**
    -   New:
        -   Ground Truth creation: a new end-to-end flow to create, label, and review ground truth data for agentic evaluation, including a dedicated labelling experience with task and project views, and guided entry from the dataset page
        -   Datasets can now be added directly as an input source to labelling projects, with a configurable data sink step
        -   Ground truth data is now available for Skill Kit to consume directly in evaluation runs
        -   Data discovery through automatically extracted dataset metadata
        -   Record-level filtering within a dataset
        -   Japanese language support for Voice Evaluation data generation, with testing across all supported languages
    -   Changed:
        -   Improved synthetic data generation quality by incorporating agent instructions from Skill Kit
        -   Dataset creation now captures source details
    -   Fixed:
        -   Multiple defect fixes across the ground truth and labelling experience, the dataset page, and synthetic data generation
        -   Security fixes
-   **Version 8.1.6 - July 2026**
    -   Data Creation updates — Data Kit Admins can now create a dataset with as few as 1 record \(reduced from 10\) and dataset names now support up to 200 characters.
    -   Push to Table — Data Kit Admins can now push generated synthetic data directly to the respective target tables for Multi-table Data Generator requests \(advised for Sub Prod Environment\), using script assistance available within the Data Kit screen.
-   **Version 7.1.2 - April 2026**

    We have given the ability for users to move the data from Data kit to Instance tables like incident or Case

-   **Version 4.0.7 - August 2025**

    Now Assist Data Kit is a one stop shop to meet your data for AI needs. Now Assist Data Kit enables users to add, discover, cherry pick, and curate data sets by adding ground truth for skill evaluation through Now Assist Skill Kit. Users can add ground truth to the selected record, add it to data collection, and publish the data collection for consumption within Now Assist Skill Kit for evaluation. Apart from data curation, users can generate synthetic data using Data Kit.


**Parent Topic:**[ServiceNow Store - Other ServiceNow AI Platform Capabilities applications version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-platcap-rn-other-landing.md)

