---
title: Report a broken device from your AI assistant
description: Create a break-fix case for broken or faulty equipment in your store by describing the problem to your AI assistant, without opening the portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/retail-industry/rahi-retail-report-device-issue-ai-assistant.html
release: australia
topic_type: task
last_updated: "2026-09-23"
reading_time_minutes: 2
keywords: [break-fix, AI assistant, Retail MCP Server, report device issue]
breadcrumb: [Retail MCP Server, Configure, Retail]
---

# Report a broken device from your AI assistant

Create a break-fix case for broken or faulty equipment in your store by describing the problem to your AI assistant, without opening the portal.

## Before you begin

Your AI assistant must be connected to the Retail MCP Server, and you must be a member of the store where the device is located.

Role required: sn\_rtl\_stre\_servcs.contributor, and sn\_retail.associate\_contributor or sn\_retail.associate\_fulfiller

## About this task

You don't need to use words like "case" or "ticket." Describe the problem the way you would to a colleague, for example, "The freezer in aisle 3 isn't cooling" or "My handheld scanner won't turn on."

For a question to HQ that isn't about equipment, see [Ask HQ a question from your AI assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/rahi-retail-ask-hq-question-ai-assistant.md).

## Procedure

1.  In your AI assistant, describe the equipment problem.

2.  If you belong to more than one store, tell the assistant which store the device is in.

    If you belong to only one store, the assistant uses it without asking.

3.  Confirm the device, or choose it from the list that the assistant shows you.

    The assistant matches your description to the devices registered to your store. You can also read out the asset tag on the device.

4.  Confirm or change the priority that the assistant proposes.

    For example, a device that stops the store from trading is Critical, and a cosmetic fault is Low.

5.  Review the case details that the assistant shows you, and confirm that it should create the case.

    The assistant writes the short description and description from what you've told it. Ask it to change anything that isn't right before you confirm.

6.  Optional: To add a photo or file, open the attachment link that the assistant gives you.

    The link opens the case in the portal. You can't send files through the assistant.


## Result

A break-fix case is created for the device, and the assistant gives you the case number and state. HQ receives the case in the usual break-fix workflow.

## What to do next

To check on the case later, see [Track and update your cases from your AI assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/rahi-retail-track-update-case-ai-assistant.md).

**Parent Topic:**[Retail MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/rahi-retail-mcp-server-overview.md)

**Related topics**  


[Retail MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/rahi-retail-mcp-server-overview.md)

[Submit Break-Fix Cases through Portal or Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/breakfix-submit-case.md)

[moveworks-breakfix-case-operations]

