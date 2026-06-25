---
title: Review a software bill of materials submission from an engagement
description: Track processing status and review the outcome of a SBOM submission from an engagement, including successful upload, failed upload, and decline.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/sbom-review.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 4
keywords: [SBOM, software bill of materials, due diligence, vendor risk assessment, processing]
breadcrumb: [Collecting software bill of materials, Assess third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Review a software bill of materials submission from an engagement

Track processing status and review the outcome of a SBOM submission from an engagement, including successful upload, failed upload, and decline.

## Before you begin

To update manufacturer data in the SBOM workspace, ensure that you have edit access to the CMDB \(configuration management database\) product model table.

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager or sn\_vdr\_risk\_asmt.vendor\_risk\_assessor

## About this task

SBOM information is collected through the engagement-level external assessment. After the engagement contact submits the assessment in the third-party portal, post-assessment processing sends the uploaded file to the SBOM API, provided by Unified Security Exposure Management \(USEM\) \(Unified Security Exposure Management\), and records status updates. To troubleshoot API processing issues, see the Unified Security Exposure Management \(USEM\) documentation.

Third-party assessment reviewers can view SBOM component records on engagement and third-party records but can't access the SBOM workspace.

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**.

2.  Select the list icon \[Omitted image "ws-list-icon.png"\] Alt text:.

3.  Navigate to **External risk assessments** &gt; **All open**.

4.  Select the External assessment \(VRA\) number of an assessment that is in the **Responses received** state.

5.  Review work notes on the external assessment and the source assessment to track processing status.

    The SBOM process status field on the engagement reflects the current state.

    |Status|Description|
    |------|-----------|
    |**Not started**|The engagement has not yet submitted the external assessment, or post-assessment processing has not begun.|
    |**Processing**|The uploaded file has been sent to the SBOM API and is being parsed.|
    |**Errored**|The file could not be parsed. The source assessment is reopened so the engagement can resubmit a corrected file.|
    |**Processed**|The file was parsed and component records were created. Review the SBOM document related list on the engagement for results.|
    |**Declined**|The third party selected a No response option and did not provide an SBOM file. The assessment is closed and a comment is logged. No component records are created.|

    An entry is created in the SBOM document related list on the engagement for each submission attempt, including failed attempts.

6.  Take action based on the processing outcome.

    -   If the engagement uploaded a valid JSON or XML file, the system performs post-assessment processing without additional input. The SBOM API parses the file, creates component records, and links the parsed component data to the engagement and, where applicable, to the related engagement record. Work notes are updated when processing is complete.

        Review collected SBOM components from the SBOM document related list on the engagement. If your instance includes the SBOM Response app and Vulnerability Response, vulnerability details are available at the component level.

    -   If the engagement uploaded a file that cannot be parsed — for example, invalid or corrupted JSON or XML, or an unsupported format such as PDF or Word — the system records an error in work notes and creates an entry in the SBOM document related list to record the failed attempt. The source assessment is reopened so the engagement can resubmit.

        Notify the engagement contact to upload a corrected SBOM file in JSON or XML format.

    -   If the engagement declined to provide a SBOM, the system logs a comment on the external assessment and closes the assessment in the **Responses received** state.

        Review the reason for the declination and determine whether further action is required as part of your risk evaluation process.


## What to do next

After reviewing the submission outcome, use the information to support your risk evaluation:

-   Review SBOM document and component records on the engagement to assess the engagement's software inventory.
-   If your instance includes the SBOM Response application and Vulnerability Response, review vulnerability details at the component level.
-   If the engagement declined to provide an SBOM, consider the declination as part of your overall risk assessment and determine whether additional due diligence steps are required.

**Related topics**  


[Exploring software bill of materials collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sbom-exploring.md)

[Collecting software bill of materials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sbom.md)

[Request a software bill of materials from an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sbom-collect.md)

[Activate SBOM support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/sbom-activate.md)

[SBOM records and relationships in Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sbom-relationship.md)

