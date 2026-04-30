---
title: Major issue management overview
description: Major issue management enables customer communication for issues that impact a wider audience. Use this feature to proactively identify impacted customers, provide information to these customers, and manage the resolution process.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Administer Customer Service Management, Customer Service Management]
---

# Major issue management overview

Major issue management enables customer communication for issues that impact a wider audience. Use this feature to proactively identify impacted customers, provide information to these customers, and manage the resolution process.

This feature enables you to efficiently manage the communication and resolution process for issues that impact multiple customers. With major issue management, you can identify impacted customers who have not yet reported an issue and proactively create cases for these customers.

Major issue management introduces the concept of a major case which contains the details about a particular issue. Child cases can easily be created for a major case, with one child case created for each customer affected by the issue. These child cases contain the customer-specific information.

Identify affected customers by creating a recipients list of accounts or consumers and attaching it to the major case. Create this list using the Targeted Communications application. Build a recipients list by identifying dynamic conditions, running a script, or importing customer information into a template. Once attached to a major case, use the recipients list to create a child case for each customer included in the list.

A major case is created in one of two ways:

-   A customer service manager can create a major case.
-   A customer service manager or major issue manager can promote a major case candidate.

Major case candidates are created either by promoting an existing customer service case \(for customer reported issues\) or by creating a candidate case directly \(for non-customer reported issues\). Candidate cases require approval before being promoted to major cases.

Major issue management also provides properties that enable automatic synchronization from a major case to the associated child cases. Use these properties to enable synchronization and to identify the synchronized fields.

Major Issue Management menu can be used in the ServiceNow AI Platform interface and in the Agent Workspace interface.

## Identifying issues and creating major cases

Customer service agents, managers, and major issue managers can use the following process to identify potential issues, create major cases, and identify impacted customers.

1.  Create a major case candidate or flag an existing customer service case as a major case candidate.
2.  Review the major case candidate and either approve it as a major case or reject it.
    -   If approved, the candidate case becomes a child case of the major case.
    -   If rejected, the candidate case returns to a normal case.
3.  Associate other cases reported for the same issue as child cases of the major case.
4.  Identify other customers impacted by the issue by creating a recipients list and attaching it to the major case.
5.  Create child cases for the customers included in the recipients list.
6.  Manage the issue to resolution using the major case.
    -   Update the major case as needed, which automatically updates the child cases.
    -   Close the major case when the issue is resolved. Closing the major case automatically closes all the child cases.

