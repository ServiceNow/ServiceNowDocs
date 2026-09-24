---
title: \(Legacy\) Get the Alexa skill ID
description: Get the Alexa Skill ID from your Alexa developer console after configuring the skill. The Skill ID is the Alexa identifier for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/get-skill-id.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Set up, Configure Conversational Integration with Alexa, Conversational Integration with Alexa, Integrate VA for NLU with voice channels, Virtual Agent channel integrations, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Get the Alexa skill ID

Get the Alexa Skill ID from your Alexa developer console after configuring the skill. The Skill ID is the Alexa identifier for the application.

## Before you begin

Role required: admin

## Procedure

1.  Log in to the Alexa developer console with your Amazon developer account.

    You can get the skill ID in two ways.

    1.  On the Alexa developer console:
        1.  Click the **Your Skills** tab.
        2.  Navigate to the skill name for which you want to copy the skill ID.
        3.  Under the skill name, click **Copy Skill ID**.
    2.  On the left Custom navigator pane of the Alexa developer console:
        1.  Select a skill from the **Your Skills** tab.
        2.  Navigate to **Assets** &gt; **Endpoint** on the Custom navigator pane.
        3.  In the AWS Lambda ARN section, click **Copy to Clipboard**.
2.  In the Provider Channel Identity record of your ServiceNow instance, paste the copied skill ID in the **Inbound ID** field.

3.  Click **Update**.


**Parent Topic:**[\(Legacy\) Set up Conversational Integration with Alexa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/setup-alexa.md)

