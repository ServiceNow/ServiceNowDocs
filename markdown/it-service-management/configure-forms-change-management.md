---
title: Configure forms for Simplified Change Management
description: Review and configure the change forms that IT fulfiller staff use to create and manage changes. Use the Form Builder to customize form layouts, fields, and sections to match your organization's change processes.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/it-service-management/configure-forms-change-management.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Change Management, forms configuration, form customization, Change Request, Form Builder]
breadcrumb: [Configuring Simplified Change Management, Configuring the fulfiller experience in Simplified IT Service Management, Configure integrations and ITSM experiences in Simplified IT Service Management, Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Configure forms for Simplified Change Management

Review and configure the change forms that IT fulfiller staff use to create and manage changes. Use the Form Builder to customize form layouts, fields, and sections to match your organization's change processes.

## Before you begin

Role required: sn\_itsm\_chg\_admin.forms\_config and sn\_ia\_config.ia\_user

**Note:** The sn\_itsm\_chg\_admin.forms\_config role no longer automatically inherits the sn\_ia\_config.ia\_user role. Users who need to configure the console must now be assigned both the appropriate Change Management role \(for example, sn\_itsm\_chg\_admin.forms\_config\) and the sn\_ia\_config.ia\_user role explicitly. Existing roles aren't modified during upgrade, allowing you to maintain full control over assignment of elevated privileges. After upgrading, if you have previously relied on inherited access, you won't be able to configure the console until the sn\_ia\_config.ia\_user role is assigned explicitly.

## About this task

Pre-configured forms are available by default and helps fulfiller staff plan, approve, and implement changes with minimal risk. You can modify these forms to include additional fields or remove fields that aren't required by your organization.

## Procedure

1.  From the header of your ServiceNow instance, navigate to **All** &gt; **Admin Home**.

2.  From the **Manage your products** section, select **View product overview** for IT Service Management.

3.  On the Product Hub page for IT Service Management, from the Configure your product section, select **Configure**.

4.  On the Configuration Console, from the left navigation panel, select **ITSM fulfiller experience &gt; Change Management &gt; Forms**. \[Omitted image "simplified-change-forms.png"\] Alt text: Change forms configuration page

    The Forms configuration page is displayed. You can see options to navigate to the current change form configuration and customize them.

5.  In the Validate in Service Operations Workspace \(SOW\) section, review and update the change form by performing the following:

    -   Log in as an IT fulfiller and navigate to SOW to view your customized form by selecting the **SOW** link.
    -   Log in as an admin to review the form experience and ensure all customizations display correctly by selecting the **SOW** link.
    -   Edit the change form directly in Form Builder by selecting the **Form Builder** link.
    You're navigated to the AITSM view in Form Builder, where you can make detailed edits to form layout, sections, and fields. For more information on using Form Builder, see [Forms in Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-view-configuration.md).

6.  When you have finished configuring, select **Mark as configured** to save your settings and mark this step as complete.

    As an alternative to the form-based wizard, you can also complete this configuration through the **Configure with AI** conversational flow, accessible from the banner at the top of the page.


## Result

You have reviewed and configured the change form experience used by your IT fulfiller staff.

**Parent Topic:**[Configuring Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configuring-change-management-experience-in-it-service-management.md)

