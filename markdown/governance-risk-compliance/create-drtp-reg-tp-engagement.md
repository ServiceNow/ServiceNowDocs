---
title: Create a third-party engagement and enhance digital resilience data
description: Create a third-party engagement record in Digital resilience third-party registers. Add details of the third-party engagement such as name of the third party, its type, annual spend, engagement tier, and so on. You can then enhance its digital resilience information for compliance with DORA regulation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/create-drtp-reg-tp-engagement.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Digital resilience third-party registers, Maintaining Digital resilience third-party registers, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create a third-party engagement and enhance digital resilience data

Create a third-party engagement record in Digital resilience third-party registers. Add details of the third-party engagement such as name of the third party, its type, annual spend, engagement tier, and so on. You can then enhance its digital resilience information for compliance with DORA regulation.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

By selecting the Third-party engagements menu item within the Digital resilience third-party registers from the Operational Resilience Workspace, you can access and view the existing third-party engagements in the system.

The **Digital resilience information** tab is also available for the Third-party engagement module, allowing you to report on third-party engagements at a more detailed, granular level. This module is visible only when the Third-party Risk Management application is installed. If you don't have this application, you can still use the Third-Party tables and digital resilience information for your third parties.

Upon installing the Digital resilience third-party registers, the **Digital resilience information** tab is added for third-party engagements. You can open this tab and set up the digital resilience information details.

\[Omitted image "tpe-dig-res-info-tab.png"\] Alt text: Info tab.\[Omitted image "tpe-dig-res-info-form.png"\] Alt text: Info form.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Digital resilience third-party registers** &gt; **Third-party engagements**.

2.  Select **New**.

    The Create New Third-party engagement form is displayed.

3.  On the form, fill in the fields.

    For more information, see [Create New Third party engagement form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-tp-engmt-form.md).

    When the Identification code type field is set to LEI and a valid LEI is entered in the Identification code field or the Additional identification code field, the system validates the code in real time against the GLEIF database and auto-populates the associated name and country fields. If you subsequently edit either auto-populated field so that the value no longer matches GLEIF data, a warning message is displayed on the edited field. You can still save the record \(warn-and-save\).

4.  Select **Save**

5.  Add digital resilience information.

    For more information, see [Add Digital resilience information to third-party engagements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tp-eng-add-digi-resi-info.md).

6.  To edit the third-party engagement record, select it from the list and select **Edit**.

7.  To export the third-party engagement record, select **Export**.

8.  To delete the third-party engagement record, select it from the list and select **Delete**.


-   **[Add Digital resilience information to third-party engagements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tp-eng-add-digi-resi-info.md)**  
Add Digital resilience information to third-party engagements.
-   **[Create New Third party engagement form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-tp-engmt-form.md)**  
On the Create New Third-party engagement form, fill in the fields.

**Parent Topic:**[Using Digital resilience third-party registers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/using-dg-registers.md)

