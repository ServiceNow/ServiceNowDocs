---
title: Turn on Full automation mode for a use case
description: Turn on Full automation mode to automatically complete and submit document tasks without an agent review. Full automation mode is turned off by default in use cases.
locale: en-US
release: australia
product: Now Assist in Document Intelligence
classification: now-assist-in-document-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Configure, Now Assist in Document Intelligence, Enable AI experiences]
---

# Turn on Full automation mode for a use case

Turn on Full automation mode to automatically complete and submit document tasks without an agent review. Full automation mode is turned off by default in use cases.

## Before you begin

-   Set up a use case fora Now Assist in Document Intelligence skill. For more information, see [Set up a use case for Now Assist in Document Intelligence](set-up-use-case-for-now-assist-document-intelligence.md).
-   Role required: sn\_docintel.manager

## About this task

The extraction mode determines how Now Assist in Document Intelligence processes document tasks for a use case. For more information, see [Data extraction modes in Now Assist in Document Intelligence](../reference/data-extraction-modes-now-assist-document-intelligence.md).

Turn on Full automation mode if you want Now Assist to bypass the agent review used to check the accuracy of the predicted values. Now Assist auto-fills the values for all required fields or marks them as missing in the document. Document tasks created for the use case are automatically completed and submitted by Now Assist.

**Warning:** Now Assist may not always produce accurate, complete, or appropriate information. By choosing to bypass the agent review, there is no way to check the accuracy of the predicted values before using the data in your workflows.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  In the workflow list, select **Platform**.

3.  In the Platform skills list, find the applicable document intelligence skill and select **Edit** in the options menu \( ![Field options menu icon](../image/icon-docintel-field-options-menu.png)\).

4.  Select the use case you would like to configure.

5.  Click the settings icon \(![Use case settings icon](../image/icon-docintel-settings-gear.png)\).

6.  On the Extraction mode screen, selectthe **Full automation mode \(no agent review required\)** option.

7.  Select the **Any required field is missing in the document** option to turn off the automation and require an agent review when any of the required fields are missing in the document.

8.  Close the Settings box.


**Parent Topic:**[Configuring Now Assist in Document Intelligence](../concept/docintel-configuring-now-assist.md)

**Related topics**  


[Activate a Now Assist in Document Intelligence skill](activate-now-assist-in-document-intelligence-skill.md)

[Set up a use case for Now Assist in Document Intelligence](set-up-use-case-for-now-assist-document-intelligence.md)

[Change the language models for a use case](change-llm-for-use-case.md)

[Edit a use case in Now Assist in Document Intelligence](edit-now-assist-document-intelligence-use-case.md)

[Make a copy of a use case in Now Assist in Document Intelligence](make-copy-of-now-assist-document-intelligence-use-case.md)

[Deactivate a use case in Now Assist in Document Intelligence](deactivate-now-assist-document-intelligence-use-case.md)

[Delete a use case in Now Assist in Document Intelligence](delete-now-assist-document-intelligence-use-case.md)

