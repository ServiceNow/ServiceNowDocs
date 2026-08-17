---
title: Redact sensitive data from documents using AI
description: Use AI to identify and redact sensitive information in documents. It suggests redaction codes based on compliance requirements, to help protect confidential data before documents are shared.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/redact-sensitive-data-using-AI.html
release: australia
topic_type: task
last_updated: "2026-07-21"
reading_time_minutes: 2
keywords: [redaction, sensitive data, document security, compliance, AI]
breadcrumb: [Use, ServiceNow Otto in Document Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Redact sensitive data from documents using AI

Use AI to identify and redact sensitive information in documents. It suggests redaction codes based on compliance requirements, to help protect confidential data before documents are shared.

## Before you begin

The Smart document skill must be configured and activated on the target table. For more information see, [Configure the smart documents skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configure-skill-smart-documents.md).

Add or remove data patterns to customize what the Smart Docs Agent suggests during redaction. For more information see, [Add or remove data patterns for sensitive content detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configure-regex-patterns.md).

Redaction codes can be customized by your organizations' admin to match compliance requirements. See [Add or modify redaction codes for sensitive data redaction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/add-or-modify-redaction-codes.md).

Role required: write access on the parent record

## Procedure

1.  Navigate to your workspace.

2.  In the list section, go to the table that has the smart documents skill activated and open the record.

    For example, an Incident record.

3.  Open the attached document to view it in the document viewer.

    **Note:** The maximum supported document size is 20 pages or 500,000 characters by default, redaction will stop if either limit is exceeded. Supported file type is only pdf.

4.  Select **Ask Otto**.

    The menu displays options for summarizing, generating FAQs, answering questions, and redaction.

5.  Select a redaction method.

    -   To redact all sensitive content, select **Redact Document Content**. The system scans the document and identifies potentially sensitive information such as email addresses, phone numbers, passwords, dates, and names.
    -   To redact specific categories, enter a category or keyword in the search field \(for example, `redact all the emails`\).
    A list of detected sensitive content appears.

6.  Select the items that you want to redact from the list.

7.  Select **Submit**.

    The system prompts you to apply redaction codes.

8.  Select **Yes** to apply redaction codes.

    The system displays AI-suggested redaction codes for each item based on the detected content type.

9.  Select the items that you want to redact based on the assigned redaction codes.

10. Select **Submit**.

11. To change a redaction code, select the highlighted area in the document and add or remove the redaction code.

    You can assign multiple codes to a single item.

    The AI suggestion is based on content analysis but might not be accurate. Verify that the assigned code matches your compliance requirements.

12. Select one of the following options:

    -   **Yes** to preview the redacted document.
    -   **No** to skip preview.
13. Select **Yes** to save the redacted document.

    The redacted document is saved with all selected sensitive data masked and assigned redaction codes.

14. To view the Redaction Audit Logs, navigate to **All** and enter `ds_redaction_audit_log.LIST` in the filter bar.


