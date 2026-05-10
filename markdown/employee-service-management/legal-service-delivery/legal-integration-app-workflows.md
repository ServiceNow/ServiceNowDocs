---
title: Workflows in Legal Service Delivery
description: The Legal Request Management application installs automated workflows for electronic signature and external storage. These workflows enable support for multiple integrations and accounts at the same time.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Workflows in Legal Service Delivery

The Legal Request Management application installs automated workflows for electronic signature and external storage. These workflows enable support for multiple integrations and accounts at the same time.

These workflows available in Legal Service Delivery are built using [Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/flow-designer.md).

**Note:** All workflows for Legal Service Delivery applications are read-only by default.

## Electronic signature workflows

The following predefined workflows for electronic signing of documents are available:

-   **Core electronic signature workflows**

    The following core electronic signature workflows are installed with Legal Request Management

    -   Electronic Signature Core - DocuSign
    -   Electronic Signature Core – AdobeSign
-   **NDA Signature workflows**

    The following electronic signature workflows are installed with Legal Simple Contracts and are used for sending the Non-disclosure Agreement \(NDA\) documents for electronic signature.

    -   NDA Electronic Signature \(Dynamic Flow\)
    -   NDA Electronic Signature - DocuSign
    -   NDA Electronic Signature - AdobeSign

## External storage workflows

The Legal External Storage Core flow for storing documents in external storage systems is installed with Legal Request Management. The following subflows are installed within the core workflow for each external storage system integration.

-   Legal External Storage Core - Microsoft OneDrive
-   Legal External Storage Core – Google Drive
-   Legal External Storage Core – Box
-   Legal External Storage Core – Microsoft SharePoint
-   Legal External Storage Core – iManage

**Note:** These external storage subflows can be used with another workflow to store documents in external storage.

The Legal Contracts External Storage Flow is the core external storage workflow installed with Legal Simple Contracts.

