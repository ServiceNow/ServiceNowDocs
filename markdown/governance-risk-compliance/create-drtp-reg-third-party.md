---
title: Create a third party and enhance digital resilience data
description: Create a third party record in Digital resilience third-party registers. Add the details of the third party company such as its name, address, phone number, vendor manager, and so on. You can then enhance its digital resilience information for compliance with DORA regulation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/create-drtp-reg-third-party.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Digital resilience third-party registers, Maintaining Digital resilience third-party registers, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create a third party and enhance digital resilience data

Create a third party record in Digital resilience third-party registers. Add the details of the third party company such as its name, address, phone number, vendor manager, and so on. You can then enhance its digital resilience information for compliance with DORA regulation.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

To access and view the existing third parties in the system, you can navigate to the Third parties menu item within the Operational Resilience Workspace. Upon installing the Digital resilience third-party registers, the **Digital resilience information** tab is added for third parties.

\[Omitted image "tpr-tp-dig-res-info-tab.png"\] Alt text: Tab.

You can open this tab and set up the digital resilience information details.

\[Omitted image "tpr-tp-dig-res-info-view.png"\] Alt text: View.\[Omitted image "tpr-tp-dig-res-form.png"\] Alt text: Digital resilience information.

DORA requires financial entities to identify all relevant ICT third-party service providers in template B\_05.01. This includes ICT intra-group service providers — entities within the same corporate group that provide ICT services — in addition to direct third-party service providers, subcontractors, and ultimate parent undertakings.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Digital resilience third-party registers** &gt; **Third parties**.

2.  Select **New**.

    The Create New Company form is displayed.

3.  On the form, fill in the fields.

    For more information, see [Create New Company form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-third-party-company-form.md).

    When the Type of code to identify the ICT service provider field is set to LEI and a valid LEI is entered in the Identification code of ICT third-party service provider field, the system validates it in real time against the GLEIF database and auto-populates the Legal name of the ICT service provider field and Country of the ICT third-party service provider's headquarters field with GLEIF data. If you subsequently edit either of those auto-populated fields so that the value no longer matches GLEIF data, a warning message is displayed on the edited field. You can still save the record \(warn-and-save\). The same behavior applies to the Additional identification code of ICT service provider field when its code type is LEI.

4.  Select **Save**.

5.  To set up the digital resilience information for DORA regulation, navigate to the **Digital resilience information** tab and select **New**.

6.  On the form, fill in the fields.

    For more information, see [Create New ICT third-party service provider form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-ICT-thirdparty-serv-prov-form.md). Details on the fields are displayed in the example.

    \[Omitted image "tpr-dig-res-info-sample-form.png"\] Alt text: Resilience details.

    You can view the legal entity ID of the third party, which can be captured by the Value Added Tax \(VAT\) number or Company Registration Number \(CRN\) number. You can specify the country of registration and their code, which the system uses to generate the ID.

    You can also indicate if the third party is ultimate or a subsidiary. Include the name of the ICT third party and the type of service they provide, such as Software as a Service \(SaaS\). Optionally, you can note if an individual acts on behalf of the organization. Additionally, select the reporting currency and input the total annual expense for this engagement.

    For more information, see [Create New Company form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-third-party-company-form.md).

7.  Select **Save**.

8.  To edit the third party company record, select it from the list and select **Edit**.

9.  To export the third party company record, select **Export**.

10. To delete the third party company record, select it from the list and select **Delete**.


-   **[Create New Company form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-third-party-company-form.md)**  
On the Create New Company form, fill in the fields for the third party.
-   **[Create New ICT third-party service provider form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-ICT-thirdparty-serv-prov-form.md)**  
On the Create New ICT third-party service provider form, fill in the fields.

**Parent Topic:**[Using Digital resilience third-party registers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/using-dg-registers.md)

