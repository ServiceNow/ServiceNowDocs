---
title: Configure data to enable matter creation in Legal Tracker
description: Configure the data that is required to create a matter in Legal Tracker.
locale: en-US
release: yokohama
product: Legal Matter Management
classification: legal-matter-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Legal Matter Management to engage with outside counsel using Legal Tracker, Setting up Legal Matter Management, Legal Matter Management, Legal Service Delivery, Employee Service Management]
---

# Configure data to enable matter creation in Legal Tracker

Configure the data that is required to create a matter in Legal Tracker.

Matter type template in Legal Tracker helps define the fields and default options that are tracked for each matter type. This enables administrators to determine what data will be tracked in Legal Tracker matters. The current integration supports the minimal fields required by the Legal Tracker to create matter. Administrators should identify matter type templates with additional required fields for matter creation and create the records for them in the table Legal Tracker Matter Template \[sn\_lg\_matter\_legal\_tracker\_matter\_template\].

Data configured in tables serve as values, which submitters select when submitting an outside engagement request form. The values are used in the Legal Tracker to generate a matter.

To avoid failures while creating matter in Legal Tracker, administrators should maintain the same data as in Legal Tracker in the following tables.

<table id="table_wzm_wf1_yyb"><thead><tr><th>

Name

</th><th>

Table

</th></tr></thead><tbody><tr><td>

Outside Counsel

</td><td>

sn\_lg\_matter\_outside\_counsel**Note:** For more information, see [Add outside counsel details](lmm-lt-setup-outside-counsels.md)

</td></tr><tr><td>

Invoice Approval Route

</td><td>

sn\_lg\_matter\_legal\_tracker\_invoice\_approval\_route**Note:** For more information, see [Add approval route details](lmm-lt-setup-approval-route.md)

</td></tr></tbody>
</table>-   **[Add outside counsel details](lmm-lt-setup-outside-counsels.md)**  
Add outside counsel details for an outside firm to enable matter creation in Legal Tracker.
-   **[Add approval route details](lmm-lt-setup-approval-route.md)**  
Add approval route details in Legal Matter Management to enable matter creation in Legal Tracker.

**Parent Topic:**[Configure Legal Matter Management to engage with outside counsel using Legal Tracker](../concept/configurations-for-legal-tracker-integration.md)

