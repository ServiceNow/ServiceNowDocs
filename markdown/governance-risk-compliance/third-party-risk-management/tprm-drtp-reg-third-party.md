---
title: Create a third party and enhance digital resilience data
description: Create a third-party record in Digital resilience third-party registers using Third-party Risk Management. Add the details of the third-party company such as its name, address, phone number, vendor manager. You can then enhance its digital resilience information for compliance with DORA regulation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-drtp-reg-third-party.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-05-15"
reading_time_minutes: 2
breadcrumb: [Use digital resilience third-party registers, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create a third party and enhance digital resilience data

Create a third-party record in Digital resilience third-party registers using Third-party Risk Management. Add the details of the third-party company such as its name, address, phone number, vendor manager. You can then enhance its digital resilience information for compliance with DORA regulation.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_assessor

## About this task

By selecting the Third parties list within the Digital resilience third-party registers from the Vendor Management Workspace, you can access and view the existing third parties in the system.

After installing the Digital resilience third-party registers, the **Digital resilience information** tab is added for third parties. You can open this tab and set up the digital resilience information details.

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**, select the list icon \[Omitted image "ws-list-icon.png"\] Alt text: and then navigate to **Digital resilience third-party registers**.

2.  Select **Third parties** and then create a third party by selecting **New**.

3.  On the form, fill in the fields.

    For descriptions of all these fields, see [Create New Company form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-create-third-party-company-form.md).

4.  Select **Save**.

5.  To set up the digital resilience information for DORA regulation, navigate to the **Digital resilience information** tab of the third party and select **New**.

6.  On the form, fill in the fields.

    For descriptions of all these fields, see [Create New ICT third-party service provider form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-create-ICT-thirdparty-serv-prov-form.md).

    **Note:**

    -   When you enter or update an LEI identification code \(when Type of code is set to LEI\), the system validates it against the GLEIF database and auto-populates the name and country fields. If you then edit the name or country to a value that no longer matches GLEIF data, an inline warning is displayed on the edited field. You can still save the record. For more information, see [Validate Legal Entity Identifier codes for DORA reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-valid-lei.md).
    -   Provider‑level annual expense totals may be automatically aggregated during report generation when all contracts meet the required criteria. Aggregation applies only to exported reports and does not change third‑party or contract records.

        For more information, see [Currency conversion and third-party total expense aggregation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dora-currency-aggregation.md).

    **Note:**

7.  To edit the third-party company record, select it from the list and select **Save** after making your edits.

8.  To export third-party company records, select **Export**.

9.  To delete the third-party company record, select it from the list and select **Delete**.


