---
title: TRM technical debt
description: Manage the TRM technical debts that are created for the products that aren’t approved for the usage.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-manage-trm-technical-debt.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring the Technology Reference Model in Enterprise Architecture Workspace, Exploring Technology Portfolio view, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# TRM technical debt

Manage the TRM technical debts that are created for the products that aren’t approved for the usage.

\[Omitted image "trm-tech-debt-list.png"\] Alt text: TRM technical debt page displaying a list of active technical debts.

A scheduled job **Populate TRM technical debts in the EA Workspace** runs and creates an entry in the TRM Technical Debt \[sn\_apm\_trm\_standards\_technical\_debt\] table for EA Workspace. The table shows a reference to the software in any business application that is not aligned with the TRM software phases. The table shows a reference to the software in any business application that either isn’t defined in TRM or has TRM product lifecycles that restrict the usage of the software. To know how the technical debts are calculated, see [Technical debt calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-trm-technical-debt-calc.md).

**Note:** The **Populate TRM technical debts in the EA Workspace** scheduled job is available only when the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

Technical debt records persist across every run of the scheduled job instead of being deleted and re-created. Each record moves between Active, Resolved, and Archived states based on what the job finds on each run. For details on these states and how records transition between them, see [TRM technical debt states and transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-trm-technical-debt-states.md). You can also configure whether the server is part of a record's identity and which reasons the job uses to create technical debt; see [Technical debt settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-setup-tech-debt.md).

**Note:**

Technical debt persistence, states, and configuration require Enterprise Architecture Workspace version 10.0.0 or later and TPM plugin \(sn\_apm\_tpm\) version 1.12.0 or later.

**Parent Topic:**[Exploring the Technology Reference Model in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-managing-the-technology-portfolio.md)

**Related topics**  


[Technical debt calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-trm-technical-debt-calc.md)

[View Technology Reference Model technical debts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/view-trm-tech-debt.md)

[Update TRM technical debt data using scheduled job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-run-job-trm-tech-debts.md)

[TRM technical debt states and transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-trm-technical-debt-states.md)

[Technical debt settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-setup-tech-debt.md)

[Governing TRM product fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-trm-governing-fields.md)

