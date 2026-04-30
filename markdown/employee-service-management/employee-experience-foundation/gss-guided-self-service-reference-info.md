---
title: Guided Self-Service reference
description: Use the following reference information for the Guided Self-Service functionality.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Reference, Employee Center, Employee Service Management]
---

# Guided Self-Service reference

Use the following reference information for the Guided Self-Service functionality.

## Guided Self-Service: Things to remember

You can display Guided Self-Service as a widget on the home page or as a quick link or as a widget on topic pages. Remember the following information:

-   Ensure that the **sn\_hr\_sp.esc\_admin** user has the **playbook.write** role to edit the playbook design and **playbook\_experience.admin** to preview the guided experience.
-   Only when the playbook and guided help process are in an active state, the guided help process appears on the Employee Center.
-   Guided Self-Service can’t be created from the playbook page directly, create the process from the GSS form, see [Configure Guided Self-Service](../task/gss-guided-help-config.md).
-   Guided Self-Service flow is a single-stage flow.
-   The Activity Definition \[sys\_pd\_activity\_definition\] table lists the definitions for the activities that you can add to a playbook in **Workflow Studio**.

    To access the activity definitions, navigate to **Process Automation** &gt; **Process Automation Administration** &gt; **Activity Definitions**

-   State management of your choices in an activity is retained for 24 hours only.
-   When a guided process activity is partially completed or aborted mid-way, you can resume and complete the rest of the process within 24 hours.
-   Currently, the option to restart the activity or change the selections isn’t supported after 24 hours. The process restarts afresh.
-   The completed self-service is purged after 30 days with the auto-flush schedule available from sys\_trigger\_list.
-   The `Cancel incomplete guided help playbook` scheduled job for the automatic cancellation of incomplete guidance is only available for admin.
-   Deleting the GSS process from `sn_ex_sp_gd_help_process` doesn’t delete the process from `sys_pd_process_definition`.

**Parent Topic:**[Employee Center reference](emp-center-reference.md)

**Related topics**  


[Activity Configuration form](ec-activity-configuration-form.md)

[Activity Configuration Detail form](activity-configuration-detail-form.md)

[Approvals experience reference](approval-hub-ootb.md)

[Block content form](block-content-form.md)

[Browser Extension for Employee Center forms](../concept/ecbe-forms.md)

[Campaign overview and Campaign analytics dashboards](../concept/ecpro-content-automation-content-pack.md)

[Components installed with Employee Center Pro](components-installed-with-employee-center-pro-1.md)

[Components installed with Content engagement](installed-content-engagement.md)

[Components installed with Content Experiences](installed-with-content-auto.md)

[Components installed with Content Publishing](installed-with-content-delivery-1.md)

[Components installed with Content Governance](ec-installed-content-governance.md)

[Components installed with Content Analytics](ecpro-installed-content-analytics-1.md)

[Connected Content form](connected-content-form.md)

[Content Analytics dashboards](../concept/content-analytics-dashboards.md)

[Content engagement dashboard](../concept/ec-pro-content-engagement-dashboard.md)

[Content Library Overview dashboard](../concept/content-library-overview-dashboard.md)

[Default Employee Profile Header Configuration record](default-profile-header.md)

[Employee Center widgets](../concept/employee-center-widgets-list.md)

[Employee Profile form](employee-profile-fieldconfig.md)

[Employee Profile Header Configuration form](profile-header-config-form.md)

[Employee Profile portal configuration form](profile-portal-config-form.md)

[Employee Profile upgrade scenarios](emp-profile-upgrade.md)

[Enhanced Requests Experience forms](req-concept-ec.md)

[External Link form](external-link-form.md)

[Featured Content form](featured-content-form.md)

[Feedback Analytics dashboard](../concept/ex-fdback-board.md)

[Feedback configuration form](ex-feedback-new-record.md)

[Feedback definition form](fdbck-dfnition-record.md)

[Footer form](ec-footer-form.md)

[Footer Menus form](ec-footer-menus.md)

[Link content form](link-content-form.md)

[Menu Item form](menu-item-form.md)

[Configuring translation for Content Publishing after upgrade](../concept/ec-multiple-language-support.md)

[Notification content form](notification-content-form.md)

[Employee Profile Overview section form](profile-overview-section-form.md)

[Properties installed with Content Experiences](properties-installed-with-content-auto.md)

[Properties installed with Content Governance](properties-installed-content-governance.md)

[Properties installed with Content Publishing](properties-with-content-delivery.md)

[Quick Link form](ec-quick-link-form.md)

[Standard banner and icon sizes](ec-portal-images-size.md)

[Tab widget mapping form](tab-widget-mapping-form.md)

[Taxonomy form](taxonomy-form.md)

[To-do content form](to-do-content-form.md)

[Topic form](topic-form.md)

[User Criteria form](ec-user-criteria-form.md)

[User Criteria output](user-criteria-output.md)

[Use Guided Self-Service](../concept/gss-guided-self-service-homepage.md)

