---
title: Use case for False positive or Request Exception Questionnaire
description: Scenario when the questionnaire for False Positive or Request Exception is raised but not filled completely.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Questionnaire support in Exception Management via Smart Assessment, Exception Management Overview, Use, Unified Security Exposure Management, Security Operations]
---

# Use case for False positive or Request Exception Questionnaire

Scenario when the questionnaire for False Positive or Request Exception is raised but not filled completely.

When the questionnaire for False positive or Request exception is raised but not filled completely, the Change Approval \(CA\) record goes into “Draft” state. If you want to raise an exception from the same category, you are navigated to the previous questionnaire following a pop-up note regarding the same. In case you want to raise a False Positive record instead of an existing request exception, the system overrides the False positive Change Approval record. It then creates a new False Positive Change Approval record.

In case the questionnaire is half filled and the same Vulnerability Item \(VIT\)/ or any ITEM is opened in classic view, you’re navigated to the workspace questionnaire to fill the remaining data if the same type of request is raised again. If the questionnaire in classic view is selectively filled and the same item is opened in the workspace, then the classic view questionnaire is opened in the workspace.

**Parent Topic:**[Questionnaire support in Exception Management via Smart Assessment](../concept/sem-smart-assessment-exp-management.md)

