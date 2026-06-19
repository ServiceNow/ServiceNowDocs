---
title: Activate contextual email matching for CSM
description: Activate the Contextual Email Matching skill in Now Assist Skill Kit to link emails received on closed interactions by analyzing open cases linked to the closed interaction, enabling downstream flows to associate interactions with cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/activate-contextual-email-matching-csm.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-06-19"
reading_time_minutes: 1
keywords: [contextual email matching, Now Assist Skill Kit, CSM, Customer Service Management, email interaction, case matching, generative AI]
breadcrumb: [Email Interaction, Email channel, Enable communication channels, Configure, Customer Service Management]
---

# Activate contextual email matching for CSM

Activate the Contextual Email Matching skill in Now Assist Skill Kit to link emails received on closed interactions by analyzing open cases linked to the closed interaction, enabling downstream flows to associate interactions with cases.

## Before you begin

Confirm the following prerequisites are met before you begin:

-   The Email Interaction for CSM plugin must be installed and active on your instance.
-   A Now Assist for CSM license must be active on your instance.

Role required: sn\_nowassist\_admin.nsa\_admin

## About this task

The Contextual Email Matching skill analyzes emails on closed interactions and identifies the most relevant open case based on the content and context of the email. The skill provides a recommended case match that downstream flows can use to associate the interaction with the correct case.

## Procedure

1.  Navigate to **Admin** &gt; **Now Assist Admin** &gt; **Now Assist Skills**.

2.  Select **Customer** &gt; **CSM**.

    **Note:** Default skills cannot be edited. To modify the prompt or skill configuration, duplicate the skill, make your changes, and then publish the duplicated skill.

3.  Locate the **Contextual Email Matching** skill and select it to open the skill details.

4.  Select **Activate skill**.

    **Note:** By default, the skill is inactive.

5.  Complete the guided setup.

6.  In **Review and activate**, review your configuration.

7.  Select **Activate**.


## Result

The Contextual Email Matching skill is active. When an email on a closed interaction is received, the skill analyzes closed email interactions and returns a recommended case match that downstream flows can use to link the new email to the correct open case.

