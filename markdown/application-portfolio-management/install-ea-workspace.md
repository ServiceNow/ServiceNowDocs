---
title: Install Enterprise Architecture Workspace
description: Install the Enterprise Architecture Workspace application \(sn\_apm\_ws\)if you have the admin role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/install-ea-workspace.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Configuring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Install Enterprise Architecture Workspace

Install the Enterprise Architecture Workspace application \(sn\_apm\_ws\)if you have the admin role.

## Before you begin

-   Review the Enterprise Architecture Workspace application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, Application Portfolio Management plugin \(com.snc.apm\).
-   For enabling the technology portfolio management information in the Enterprise Architecture Workspace:
    -   Ensure you have activated the Basic Software Asset Management \(com.snc.sams\).
    -   Ensure you have installed the Technology Portfolio Management \(sn\_apm\_tpm\) store app.

Role required: admin

\[Omitted image "eaw-install-app.png"\] Alt text: Install Enterprise Architecture Workspace screen.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


-   **[Components installed with Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-installed-with-eaw.md)**  
Several types of components are installed with Enterprise Architecture Workspace including user roles, scheduled jobs, tables, and scripts.
-   **[Enterprise Architecture Workspace access roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-access-roles.md)**  
The following roles help you to configure and use the Enterprise Architecture Workspace application. After access has been granted to a role, all the groups or users assigned to the role are granted access. Roles can contain other roles, and any access granted to a role is granted to any other role that includes it.
-   **[Business stakeholder role for Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-business-stakeholder-role.md)**  
The Business Stakeholder \(com.snc.business\_stakeholder\) plugin contains the business stakeholder role for Enterprise Architecture Workspace application. Users with this role can view or read records in the Enterprise Architecture Workspace.
-   **[ServiceNow Otto for Enterprise Architecture \(EA\) access roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/sn-otto-access-roles.md)**  
The following roles help you to configure and use each ServiceNow Otto for Enterprise Architecture \(EA\) skill.
-   **[Tables installed with Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-installed-tables.md)**  
The following tables are added with activation of Enterprise Architecture Workspace.
-   **[Granular admin role changes in Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-gran-admin-role-changes.md)**  
Understand the transition from global admin usage to feature‑specific granular admin roles, outlining the intent, architectural principles, and governance expectations defined by the Granular Admin Directive.
-   **[Application plugin installation sequence for Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-plugin-activation-sequence.md)**  
Activate the required plugins and optional add-ons in the correct order to confirm all Enterprise Architecture Workspace features are available on your instance.

**Parent Topic:**[Configuring Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/configure-eaw.md)

**Related topics**  


[Enterprise Architecture Workspace access roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-access-roles.md)

[Tables installed with Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-installed-tables.md)

[Granular admin role changes in Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-gran-admin-role-changes.md)

[Application plugin installation sequence for Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-plugin-activation-sequence.md)

[Scheduled jobs installed with Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-scheduled-jobs.md)

