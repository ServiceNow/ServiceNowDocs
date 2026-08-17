---
title: Turn on full automation mode
description: Turn on Full automation mode to automatically complete and submit document tasks without an agent review. Full automation mode is turned off by default in document extraction use cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/turn-on-full-automation.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Information Extraction skill, Configure, Content Understanding, Enable AI experiences]
---

# Turn on full automation mode

Turn on Full automation mode to automatically complete and submit document tasks without an agent review. Full automation mode is turned off by default in document extraction use cases.

## Before you begin

-   Set up a use case for the Information Extraction skill. For more information, see [Configure Information Extraction skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cu-configure-information-extraction-skill.md).
-   Role required: DocIntel Manager \[sn\_docintel.manager\]


## About this task

The extraction mode determines how Content Understanding processes document tasks for a use case. For more information, see [Automation modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/automation-modes.md).

**Warning:** AI may not always produce accurate, complete, or appropriate information. By choosing to bypass the agent review, there is no way to check the accuracy of the predicted values before using the data in your workflows.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills**.

2.  In the workflow list, select **Platform**.

3.  In the Platform skills list, find the Extract Information from documents skill and select **Edit** in the options menu \( \[Omitted image "options-icon.png"\] Alt text: Field options menu icon\).

4.  Select the use case you would like to configure.

5.  Select the settings icon \(\[Omitted image "icon-docintel-settings-gear.png"\] Alt text: Use case settings icon\).

6.  On the Extraction mode screen, select the **Full automation mode \(no agent review required\)** option.

7.  Select the **Any required field is missing in the document** option to turn off the automation and require an agent review when any of the required fields are missing in the document.

8.  Close the Settings box.


