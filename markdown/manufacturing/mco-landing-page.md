---
title: Manufacturing Commercial Operations landing page \(Agents or CSM/FSM configurable workspace\)
description: Manufacturing Commercial Operations enables OEMs or manufacturers to use Agents workspace as a landing page to create sales promotion and recall campaigns. It also enables the agents to view, submit, review, and approve claims.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-landing-page.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Explore, Manufacturing Commercial Operations]
---

# Manufacturing Commercial Operations landing page \(Agents or CSM/FSM configurable workspace\)

Manufacturing Commercial Operations enables OEMs or manufacturers to use Agents workspace as a landing page to create sales promotion and recall campaigns. It also enables the agents to view, submit, review, and approve claims.

Manufacturing Commercial Operations provides personalized landing pages for key Manufacturing Commercial Operations personas—Recall Manager, Sales Promotions Manager, Claims Agent, MCO admin, and Warranty Assessor—each displaying role-relevant case summaries, charts, and performance analytics widgets.

\[Omitted image "agents-ws-portal.png"\] Alt text: MCO Agents workspace

The agent workspace landing page includes different sections and components. It has the following capabilities:

-   Toggle between gallery view and list view.
-   View the isolated view of each module by selecting **View all**
-   Create records.

**Note:** Users without AI plugins installed can view the non-AI repair view experience.

|Tabs/Fields|Description|
|-----------|-----------|
|Active claims|Number of active repair and sales promotion claims.|
|Active pre-authorization requests|Number of active pre-authorization requests received from the dealers.|
|Active campaigns|Number of active recall and sales promotion campaigns published by OEMs.|

## Repair claim

The Repair Claims list displays warranty repair claims and their AI-suggested dispositions. Use the filter pills to narrow the list by disposition category.

|Filters|Description|
|-------|-----------|
|Suggested for Approval|Displays claims that have passed all validation checks and are within the approved threshold.|
|Suggested for Rejection|Displays claims flagged for rejection based on validation failures.|
|Suggested for Review|Displays claims that require manual review before a decision can be made.|
|Potential fraud|Displays claims flagged as potentially fraudulent by the AI agent.|
|All|Displays all repair claims regardless of disposition.|

When the Suggested for Approval filter is active, an AI-generated summary displays the total number of claims that have passed all checks and are within the approval threshold, along with a breakdown of the following amounts:

|Fields|Description|
|------|-----------|
|Total amount|Combined total of all charges across the filtered claims.|
|Total labor charges|Total labor costs across the filtered claims.|
|Total part charges|Total parts costs across the filtered claims.|
|Total miscellaneous charges|Total miscellaneous costs across the filtered claims.|
|Total external charges|Total external costs across the filtered claims.|

Each claim card in the list displays the claim number, current state, and suggested action reason.

## Sales promotion claim case

The Sales promotion claim case list displays all claim cases submitted by dealers for active sales promotions.

|Filters|Description|
|-------|-----------|
|All|Displays all claim cases.|
|Approved|Displays claim cases approved for reimbursement.|
|Rejected|Displays claim cases that were declined.|
|Pending Review|Displays claim cases awaiting review.|

|Fields|Description|
|------|-----------|
|Number|Unique identifier for the claim case.|
|Short description|Brief description of the claim.|
|Dealer|Dealer that submitted the claim.|
|Total claimed amount|Total amount submitted for reimbursement.|
|State|Current status of the claim case.|

## Pre-authorization request

The pre-authorized repair request list displays all pre-authorization requests submitted by dealers.

|Filters|Description|
|-------|-----------|
|All|Displays all pre-authorization requests regardless of status.|
|Approved|Displays requests that have been approved.|
|Rejected|Displays requests that have been declined.|
|Pending Review|Displays requests that are awaiting review.|

Each request displays the following information:

|Field|Description|
|-----|-----------|
|Number|Unique identifier for the pre-authorization request.|
|State|Current status of the request.|
|Dealer|Dealer that submitted the request.|
|Updated|Date and time the request was last updated.|

Use the Filter, Sort by, and Group by controls to refine and organize the list.

## Recall campaign

Displays all recall campaigns accessible to the logged-in user. Use the filter to narrow the list by campaign status.

|Filters|Description|
|-------|-----------|
|All|Displays all the recall campaign regardless of status.|
|Approved|Displays campaigns that have been approved.|
|Rejected|Displays campaigns that have been declined.|
|Pending Review|Displays campaigns that are awaiting review.|

## Sales promotion

Displays all sales promotions accessible to the logged-in user. Use the filter to narrow the list by promotion status.

|Filters|Description|
|-------|-----------|
|All|Displays all the sales promotion campaign regardless of status.|
|Approved|Displays campaigns that have been approved.|
|Rejected|Displays campaigns that have been declined.|
|Pending Review|Displays campaigns that are awaiting review.|

|Fields|Description|
|------|-----------|
|Number|Unique identifier for the sales promotion.|
|State|Current status of the promotion.|
|Description|Brief description of the promotion.|
|Promotion Type|Type of promotion associated with the record.|
|Owner|User responsible for the promotion.|

**Related topics**  


[Set up Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-setup.md)

[Set up sales promotion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-set-up-sls-prom.md)

[Agent management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-agent-management.md)

