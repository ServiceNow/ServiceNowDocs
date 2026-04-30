---
title: Add all translated Knowledge Base articles after an upgrade
description: Complete bulk tagging after you upgrade Employee Center by running the utility script. You can determine how many disassociated Knowledge Base article translations and unlinked topics that you have, using this script.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Translated Knowledge Base article attachment behaviour, Dynamic topic pages, Setup Employee Center browse experience features, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Add all translated Knowledge Base articles after an upgrade

Complete bulk tagging after you upgrade Employee Center by running the utility script. You can determine how many disassociated Knowledge Base article translations and unlinked topics that you have, using this script.

## Before you begin

Role required: esc\_admin

## About this task

Upgrade to the Employee Center app version 25.0.3 to use the script to evaluate if all your Knowledge Base article translations are correctly connected to their respective topics.

You can run the utility script to bulk tag all translated versions of Knowledge Base articles to all the respective topic pages at once.

## Procedure

1.  Append the UI link `sn_ex_sp_get_unlinked_translated_kb.do` to the end of your instance URL.

    Select one of the following buttons populated by the script:

    -   **Topic with unlinked knowledge article count**, which provides the number of topics with one or more unlinked Knowledge Base article translations.
    -   **Unlinked translated knowledge articles count**, which populates the exact number of unlinked translated article versions.
2.  To complete the association, select **Link all translated knowledge articles**.

3.  To update the count before linking, select **Refresh list**.


