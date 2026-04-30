---
title: Compose Sales and Order Management workflows
description: Compose and build workflows and move data between different phases of a workflow using the sales and order management workflows.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Sales and Order Management workflows, Product data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Compose Sales and Order Management workflows

Compose and build workflows and move data between different phases of a workflow using the sales and order management workflows.

## Overview for sales and order management workflows

Use the core APIs like create instance, Delta, Effect, and Commit Instance to move data from Leads to Opportunities to Quotes and further until a sale is finalized. The APIs also provide guidelines on how Move, Add, Change, Resume, Suspend, and Disconnect flows for sold products can be performed. To learn more about the APIs, see [LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

## Workflows

The sales and order management APIs enable different workflows. The following image is an example of how a sold product can be modified to create a change order.

![image.SOM_workflows]

Select a sold product and modify it. This launches the configurator UI and creates an order. This happens with the help of the lead to cash core APIs. The APIs are the foundation used to build and modify several flows. To learn more about the existing APIs see [LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

