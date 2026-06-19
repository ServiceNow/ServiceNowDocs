---
title: Configure the Standard change model
description: Configure the Standard change model to manage the pre-defined templates that requesters use to create Standard changes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/configure-standard-change-model-scm.html
release: australia
product: IT Service Management
classification: it-service-management
topic_type: task
last_updated: "2026-05-18"
reading_time_minutes: 1
keywords: [Standard change model, change templates]
breadcrumb: [Configure change models, Configuring Simplified Change Management, Configuring the fulfiller experience in Simplified IT Service Management, Configure integrations and ITSM experiences in Simplified IT Service Management, Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Configure the Standard change model

Configure the Standard change model to manage the pre-defined templates that requesters use to create Standard changes.

## Before you begin

Role required: sn\_itsm\_chg\_admin.change\_models\_config, sn\_itsm\_chg\_admin.admin, or admin

## About this task

Standard changes are pre-approved and accessed through templates rather than a change type picker. Requesters select a template directly to create a Standard change. Because Standard changes bypass the approval workflow, the model doesn't include availability, approval, or automatic task settings.

## Procedure

1.  Open the **Standard** change model in the Configuration Console.

    For navigation steps, see [Configure change models for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-change-models-scm.md).

2.  In the **New** section, review the templates listed under Templates that use this change model.

    Each template pre-fills common fields and follows the Standard change model's workflow. Requesters select a template to create a Standard change.

3.  To add a template, select **New template**.

    For steps to configure a template, see [Create and propose a change template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/create-change-template.md).

4.  Select **Save**.


## Result

The Standard change model configuration is saved. Requesters access Standard changes only through the templates listed in the **New** section.

## What to do next

To configure additional change models, return to [Configure change models for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-change-models-scm.md).

**Parent Topic:**[Configure change models for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-change-models-scm.md)

