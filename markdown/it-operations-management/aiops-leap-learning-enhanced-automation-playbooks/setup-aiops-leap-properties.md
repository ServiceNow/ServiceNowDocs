---
title: Setup LEAP properties
description: Configure LEAP properties to estimate cost and time savings calculations for your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/setup-aiops-leap-properties.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: task
last_updated: "2026-08-10"
reading_time_minutes: 1
breadcrumb: [Configure, Learning Enhanced Automation Platform \(LEAP\), ITOM Visibility, IT Operations Management]
---

# Setup LEAP properties

Configure LEAP properties to estimate cost and time savings calculations for your organization.

## Before you begin

Role required: LEAP admin

Each knowledge base you plan to use in LEAP must have the correct Can Contribute permissions configured before you set up knowledge base routing. See [Knowledge base permissions for LEAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/configure-knowledge-base-user-collections.md).

## About this task

If you are a first-time user of LEAP, review the default values before making changes.

Settings include three configuration areas: cost and time savings estimation, AI agent behavior, and knowledge base routing. AI agent configuration controls the conditions under which the LEAP AI agent automatically creates problem records and knowledge base articles, such as minimum incident count and severity thresholds. Knowledge base routing controls where articles are stored when created by the LEAP AI agent or manually from an automation opportunity. Selecting a default knowledge base is mandatory — you cannot save settings without one. For details on all fields, see [LEAP settings fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/aiops-leap-settings-fields.md).

## Procedure

1.  Select **Configure settings**.

2.  On the settings page, choose one of the following options:

    -   Fresh Install
        1.  Select **Configure settings**.
        2.  Review the default values for each property.
        3.  Select **Save**.

            **Note:** LEAP recommends using default values initially to view and understand the cost and time savings estimates.

    -   Upgrade
        1.  Select **Configure settings**.
        2.  Review the default values for each property.
        3.  Modify values as needed.
        4.  Select **Save**.
3.  You are redirected to the LEAP landing page. For details on each field, see [LEAP settings fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/aiops-leap-settings-fields.md)
4.  [Activate LEAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/activate-aiops-leap.md).


