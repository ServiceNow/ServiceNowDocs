---
title: View Technology Reference Model technical debts
description: View Technology Reference Model \(TRM\) technical debts created for products that are not aligned with TRM phases and standards.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-portfolio-management/view-trm-tech-debt.html
release: zurich
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 4
keywords: [TRM technical debt, technology reference model, EA workspace, software alignment]
breadcrumb: [Working with Technology Reference Model \(TRM\) in EA Workspace, Manage, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# View Technology Reference Model technical debts

View Technology Reference Model \(TRM\) technical debts created for products that are not aligned with TRM phases and standards.

## Before you begin

Role required: sn\_apm.apm\_analyst

## About this task

\[Omitted image "trm-tech-debt-list.png"\] Alt text: TRM technical debt page displaying a list of active technical debts.

The **Populate TRM technical debts in the EA Workspace** scheduled job creates entries in the TRM Technical Debt \[sn\_apm\_trm\_standards\_technical\_debt\] table. This table references software in business applications that is not aligned with TRM software phases.

The table identifies software that either is not defined in TRM or has TRM product lifecycles that restrict software usage. For information about technical debt calculation, see [Technical debt calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-trm-technical-debt-calc.md).

**Note:** The **Populate TRM technical debts in the EA Workspace** scheduled job is available only when the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

Technical debt records persist across job runs instead of being deleted and re-created. Each record moves between Active, Resolved, and Archived states. For details, see [TRM technical debt states and transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-trm-technical-debt-states.md).

## Procedure

1.  Navigate to **Workspace** &gt; **Enterprise Architecture Workspace**.

2.  Select the Technology Portfolio icon \[Omitted image "technology-portfolio-icon.png"\] Alt text: to open the Technology Portfolio page.

3.  Select **Technical Debt**.

    **Note:** You can also open this list directly by selecting the **Business applications with TRM technical debt** card in the **Portfolio Overview and Health** section on the Enterprise Architecture Workspace home page.

4.  In the **Reason** column, select a value to open the technical debt record.

    For field information, see [TRM technical debt form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-trm-technical-debt-form.md).

    \[Omitted image "trm-tech-debt-details.png"\] Alt text: Tech debt details page displaying the field level information of the tech debt.

5.  In the technical debt record, select the **Discovered Technology** related list to view the TPM discovered technology records that the technical debt was created from.

    \[Omitted image "trm-tech-debt-discvrd-tchlgy.png"\] Alt text: Discovered Technology related list showing columns for Number, Earliest lifecycle date, Business application, Application service, Type, Software product, Product model, and Server.


## Result

The list displays TRM products, associated business application details, and the reason for each technical debt. Use this information to identify and address alignment issues in your technology portfolio.

**Parent Topic:**[Working with Technology Reference Model \(TRM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-work-with-trm.md)

**Related topics**  


[View all TRM phases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-view-all-trm-phases.md)

[Add a TRM product in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-create-trm-prod-lifecycle.md)

[View all TRM categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/view-all-trm-categories.md)

[View all TRM products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-view-all-trm-products.md)

[Update TRM technical debt data using scheduled job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-run-job-trm-tech-debts.md)

[Request a TRM product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-request-a-trm-products.md)

[View all TRM products grouped by product category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-view-all-trm-products-grouped-by-product-category.md)

[Request a TRM product lifecycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-request-a-trm-product-lifecycle.md)

[Associate an Architectural Artifact to a TRM product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-assoicate-artifact-trm-prod.md)

[Add a TRM product lifecycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-create-trm-prod-lifecycle-req.md)

[Exploring the Technology Reference Model in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-managing-the-technology-portfolio.md)

[View or update your TRM requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-view-update-trm-requests.md)

[TRM technical debt states and transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-trm-technical-debt-states.md)

[Configure technical debt settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-configure-tech-debt.md)

