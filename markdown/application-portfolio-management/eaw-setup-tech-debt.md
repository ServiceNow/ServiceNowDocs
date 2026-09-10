---
title: Technical debt settings
description: Control which server and reason criteria the scheduled job uses to create TRM technical debt records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-setup-tech-debt.html
release: australia
topic_type: concept
last_updated: "2026-08-24"
reading_time_minutes: 1
keywords: [technical debt, settings]
breadcrumb: [Configure EA Workspace using the Setup page, Configuring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Technical debt settings

Control which server and reason criteria the scheduled job uses to create TRM technical debt records.

**Note:**

The Technical debt settings page requires Technology Portfolio Management plugin \(sn\_apm\_tpm\) version 1.11.1 or later. If this version isn't installed, contact your system administrator to update the plugin.

\[Omitted image "trm-tech-debt-settings.png"\] Alt text: Technical debt settings page in the EA Workspace Setup page.

By default, the scheduled job **Populate TRM technical debts in the EA Workspace** creates a separate technical debt record for each server on which unapproved software runs. You can change this so that the job creates one technical debt record for a software product regardless of how many servers it runs on.

You can also choose which reasons the job uses to create technical debt. If you clear a reason, the job stops creating new technical debt records for that reason, and any existing active records for that reason move to the **Archived** state.

**Note:**

Changing the server configuration requires you to delete all existing technical debt records first. The system blocks the change until you do.

An organization early in its technology governance practice might not be concerned yet with whether a software product is cataloged in the TRM at all. However, it does want to enforce version compliance for products that are cataloged. That organization can clear the reasons related to whether the product is defined or approved, and keep only the version- and edition-related reasons selected. As the organization's practice matures, it can select additional reasons to build a stricter definition of technical debt.

-   **[Configure technical debt settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-configure-tech-debt.md)**  
Configure whether the server is part of a technical debt record's identity and select which reasons the scheduled job uses to create technical debt.

**Parent Topic:**[Configure EA Workspace using the Setup page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-config-eaw-using-setup-page.md)

**Related topics**  


[Configure technical debt settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-configure-tech-debt.md)

[TRM technical debt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-manage-trm-technical-debt.md)

[TRM technical debt states and transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-trm-technical-debt-states.md)

