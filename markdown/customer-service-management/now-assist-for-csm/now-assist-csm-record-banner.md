---
title: Banners in Now Assist for Customer Service Management \(CSM\)
description: Banners display information about generative AI skills and the form fields that are generated or predicted by the those skills.
locale: en-US
release: xanadu
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Now Assist for Customer Service Management \(CSM\), Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Banners in Now Assist for Customer Service Management \(CSM\)

Banners display information about generative AI skills and the form fields that are generated or predicted by the those skills.

## Overview

The generative AI banner displays information about the fields on a form that are generated or predicted by the skills available with Now Assist for CSM. Messages that appear in the banner:

-   Alert agents when fields are being generated or predicted and when the process is complete.
-   Remind agents to review the information in these fields.
-   Inform agents if fields cannot be generated or predicted.

Messages also include links to the fields that are generated or predicted by Now Assist for CSM.

![Banner with links to predicted fields in CSM Configurable Workspace](../image/now-assist-csm-case-banner.png "Generative AI banner in CSM Configurable Workspace")

## Links to generated or predicted fields

Messages displayed in the generative AI banner can include links to the fields that are generated or predicted by AI. For case records, this includes fields such as the case description and short description. For interaction records, this includes fields such as the short description and chat summary.

When an agent selects a link in the message, that field is highlighted on the form. If an agent modifies the field and saves the record, the link to that field is removed from the message. Restoring the field to the original value returns the link to the message.

## Setting default record pages

A record page provides the base structure for how a record is displayed in CSM Configurable Workspace. When the system displays information in CSM Configurable Workspace, such as case records and interactions, it uses the pages that have been set as the default record pages.

Set the following pages as the default record pages in UI Builder:

-   **CSM default record page**: Includes specific features for case management.
-   **CSM Interaction record page**: Includes CSM-specific features for interaction management.

These pages support the Now Assist for Customer Service Management \(CSM\) functionality in CSM Configurable Workspace, including the display of the generative AI icon and banner. For more information, see [Set record page order](../task/config-csm-ws-set-record-page-order.md).

