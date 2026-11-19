---
title: Configure knowledge base permissions for LEAP
description: Set the Can Contribute field on each knowledge base so that LEAP can route articles to it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/configure-knowledge-base-user-collections.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: task
last_updated: "2026-11-06"
reading_time_minutes: 1
keywords: [knowledge base permissions, Can Contribute, KB routing, knowledge base user collections]
breadcrumb: [Configure, Learning Enhanced Automation Platform \(LEAP\), ITOM Visibility, IT Operations Management]
---

# Configure knowledge base permissions for LEAP

Set the Can Contribute field on each knowledge base so that LEAP can route articles to it.

## Before you begin

Role required: LEAP admin

## About this task

LEAP routes knowledge base articles to the knowledge bases configured in LEAP properties. If the Can Contribute field is not set to allow users with the knowledge role to submit content, routing fails and the following error is displayed:

`KB creation failed. Verify that the 'Can Contribute' field in the selected knowledge base is set to 'Users with 'knowledge' role'.`

Complete this task for every knowledge base you plan to use in LEAP, including the default knowledge base and any knowledge bases listed in the **Eligible knowledge bases** field.

## Procedure

1.  Navigate to **Knowledge** &gt; **Administration** &gt; **Knowledge Bases**.

2.  Open the knowledge base that you want to use in LEAP.

3.  Select the **Can Contribute** tab.

4.  In the **Can Contribute** field, select **Users with 'knowledge' role for KB**.

5.  Save the changes.

6.  Repeat steps 2 through 5 for each additional knowledge base.


## Result

LEAP can route articles to the configured knowledge bases.

## What to do next

Set up knowledge base routing in LEAP properties. See [LEAP settings fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/aiops-leap-settings-fields.md).

