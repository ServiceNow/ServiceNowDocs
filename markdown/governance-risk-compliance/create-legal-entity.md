---
title: Create a legal entity and enhance digital resilience data
description: Create a legal entity record in Digital resilience third-party registers. You can then enhance its digital resilience information for compliance with DORA regulation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/create-legal-entity.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Digital resilience third-party registers, Maintaining Digital resilience third-party registers, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create a legal entity and enhance digital resilience data

Create a legal entity record in Digital resilience third-party registers. You can then enhance its digital resilience information for compliance with DORA regulation.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

When you select the Legal entities record in Digital resilience third-party registers menu item in the Operational Resilience Workspace, you can view the existing legal entities \(core companies\) in the system.

When you install Digital resilience third-party registers, the **Legal entities** tab gets added for the existing companies. You can launch the **Legal entities** tab and configure the details.

\[Omitted image "tpr-legal-entities-tab.png"\] Alt text: Tab.\[Omitted image "tpr-legal-entities-view.png"\] Alt text: View.

**Note:** The Digital Resilience Incident Reporting questionnaire reference questions \(for example, 'Name of the entity submitting the report' and 'LEI of the entity submitting the report'\) do not read from this Legal entity table. They read from the DORA accelerator legal-entity table \[sn\_dora\_accel\_entity\]. If you also use DRIR, populate sn\_dora\_accel\_entity so those questions can be answered.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Digital resilience third-party registers** &gt; **Legal entities**.

2.  Select **New**.

    The Create New Company form is displayed.

    \[Omitted image "leg-ent-create-new-company-form.png"\] Alt text: Company form.

3.  On the form, fill in the fields.

    For more information, see [Create New Company form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-legal-entity-form.md).

4.  Select **Save**.

    The company record is set up. Users can set up the legal entity for the company and the digital resilience information on the **Legal entity** tab.

    \[Omitted image "leg-ent-tab.png"\] Alt text: Tab.

5.  To create a legal entity record and set up its digital resilience information for DORA regulation, navigate to the **Legal entity** tab and select **New**.

    For information on setting up the digital resilience information for a legal entity, see [Create New Legal entity form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-legal-entity.md).

    The Create New Legal Entity form is displayed.

    \[Omitted image "leg-ent-create-new-form.png"\] Alt text: Form.

6.  Select **Save**.

    The Legal Entity record contains fields that provide the necessary information for regulatory reporting of the legal entity. This includes details like Legal Entity Identifier \(LEI\), name, country of registration, entity type \(as defined by the regulator\), and more. These fields are offered as choice lists within the system for users to select from.

    **Note:** When the Identification code type field is set to LEI and a valid LEI is entered, the system performs a real-time lookup against the GLEIF database. On successful validation, the Name of the entity and Country of the entity fields are automatically populated with data returned from GLEIF \(Global Legal Entity Identifier Foundation\). If you subsequently edit the Name of the entity or Country of the entity field so that the value no longer matches GLEIF data, a warning message is displayed on the edited field. You can save the record despite this warning \(warn-and-save\).

    \[Omitted image "tpr-leg-ent-form.png"\] Alt text: Form.

    The system acknowledges the entity hierarchy, with no additional details required for ultimate parents, while subsidiaries must specify their parent entity. The date of registration for each legal entity is also noted.

    For each entity, the system records the following details:

    -   Last update to the record
    -   Integration date of the information register
    -   History of the financial entity's removal from the register, if any \(and if so, the deletion date, currency used, and total asset value at that time\)
    Regulators mandate these specific details for legal entities engaging with external third parties for outsourced technical services.

7.  To edit the Legal entity record, select it from the list and select **Edit**.

8.  To export the Legal entity record, select **Export**.

9.  To delete the Legal entity record, select it from the list and select **Delete**.


## What to do next

Set up branches for a legal entity. For more information, see [Create a branch and enhance digital resilience data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-drtp-reg-branch.md).

-   **[Create New Company form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-legal-entity-form.md)**  
On the Create New Company form, fill in the fields for the legal entity.
-   **[Create New Legal entity form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-legal-entity.md)**  
On the Create New Legal entity form, fill in the fields to set up the digital resilience information.

**Parent Topic:**[Using Digital resilience third-party registers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/using-dg-registers.md)

