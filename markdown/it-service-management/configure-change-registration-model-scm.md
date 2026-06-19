---
title: Configure the Change Registration change model
description: Configure the Change Registration change model to define who can register external changes and configure stakeholder notifications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/configure-change-registration-model-scm.html
release: australia
product: IT Service Management
classification: it-service-management
topic_type: task
last_updated: "2026-05-18"
reading_time_minutes: 1
keywords: [Change Registration change model, external changes, change registration]
breadcrumb: [Configure change models, Configuring Simplified Change Management, Configuring the fulfiller experience in Simplified IT Service Management, Configure integrations and ITSM experiences in Simplified IT Service Management, Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Configure the Change Registration change model

Configure the Change Registration change model to define who can register external changes and configure stakeholder notifications.

## Before you begin

Role required: sn\_itsm\_chg\_admin.change\_models\_config, sn\_itsm\_chg\_admin.admin, or admin

## About this task

Change Registration captures changes controlled by external teams or vendors, such as platform upgrades or vendor-managed changes. The model has no approval workflow. Configuration focuses on who can register changes and who receives notifications when a change is registered.

## Procedure

1.  Open the **Change Registration** change model in the Configuration Console.

    For navigation steps, see [Configure change models for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-change-models-scm.md).

2.  In the **Availability** section, set the **Available for new change requests** toggle.

    Select to expose the model in the change type picker. Clear to hide it from requesters.

3.  In the **Review** section, select who can register external changes and notification options.

    1.  Under **Who can register external changes?**, select the users or groups authorized to register external changes

        **Note:** Only users with the sn\_change\_write role are available for selection.

        Only the selected users and groups can choose the Change Registration model when recording an external change. Limit this to change managers or team leads who coordinate with external parties.

    2.  Under **Who should be informed about external changes?**, configure recipients and the email notification template.

        An email is sent to these users or groups to notify them of the registration of an external change.

4.  Select **Save**.


## Result

The Change Registration change model configuration is saved. Only the designated users and groups can register external changes, and the configured recipients receive email notifications on each registration.

## What to do next

To configure additional change models, return to [Configure change models for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-change-models-scm.md).

**Parent Topic:**[Configure change models for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-change-models-scm.md)

