---
title: Request a software bill of materials from an engagement
description: Turn on SBOM collection on a due diligence request and send the external assessment to collect SBOM data from an engagement contact.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-sbom-collect.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 2
keywords: [SBOM, software bill of materials, due diligence, vendor risk assessment, external assessment, engagement]
breadcrumb: [Collecting software bill of materials, Assess third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Request a software bill of materials from an engagement

Turn on SBOM collection on a due diligence request and send the external assessment to collect SBOM data from an engagement contact.

## Before you begin

-   Confirm that the following applications are installed for SBOM file collection:
    -   SBOM Core \(sn\_sbom\_core\)
    -   Data Model for SBOM \(sn\_sbom\_dm\)
-   If your organization requires vulnerability details for SBOM components, confirm that the following additional applications are installed:

    -   SBOM Response \(sn\_sbom\_resp\)
    -   Vulnerability Response \(sn\_vul\)
    For more information see, [Activate SBOM support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/sbom-activate.md).

-   Confirm that the engagement uses the Smart Assessment Engine. SBOM collection isn't supported for Classic assessments.
-   Inform the engagement contact that they will receive an external assessment requesting an SBOM file in JSON or XML format. The third party generates this file using their own tooling. The ServiceNow platform does not create or edit SBOM files.

**Important:** Depending on your entitlements, some SBOM capabilities require additional configuration. For more information, see [Activate SBOM support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/sbom-activate.md).

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager or sn\_vdr\_risk\_asmt.vendor\_risk\_assessor

## About this task

SBOM collection uses the standard third-party due diligence workflow and does not change onboarding or IRQ processes.

The engagement-level external assessment is the mechanism through which SBOM information is collected.

## Procedure

1.  Turn on SBOM collection for the engagement.

<table><thead><tr><th align="left" id="d78076e196">

Option

</th><th align="left" id="d78076e199">

Steps

</th></tr></thead><tbody><tr><td id="d78076e205">

**New due diligence request**

</td><td>

1.  Initiate the due diligence request.
2.  Select **SBOM required**.
3.  Complete the request.
 For details, see [Request due diligence for a third-party engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-request-dd-for-engagement.md).

</td></tr><tr><td id="d78076e240">

**Existing due diligence request**

</td><td>

1.  Open the due diligence request.
2.  Select **SBOM required**.
3.  Save the record.


</td></tr></tbody>
</table>2.  Send the external assessment to request the SBOM.

    1.  Complete the Request, IRQ, and third-party element steps \(if applicable\), to advance the engagement to the due diligence process.

        The system associates the SBOM questionnaire with the engagement’s external assessment.

    2.  Send the external assessment to the engagement contact.

        The engagement contact receives the assessment through the third-party portal.


## What to do next

After the external assessment is submitted, review the submission outcome. For details, see [Review a software bill of materials submission from an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/sbom-review.md).

**Related topics**  


[Exploring software bill of materials collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sbom-exploring.md)

[Collecting software bill of materials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sbom.md)

[Activate SBOM support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/sbom-activate.md)

[Review a software bill of materials submission from an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/sbom-review.md)

[SBOM records and relationships in Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sbom-relationship.md)

