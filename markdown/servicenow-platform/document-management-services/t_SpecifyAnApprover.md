---
title: Specify an approver
description: You can specify approvers for a document record after you save it.
locale: en-US
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create or request a new document, Create a document, Managed Documents, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Specify an approver

You can specify approvers for a document record after you save it.

## Before you begin

Role required: document\_management\_admin

or

Role required: document\_management\_user

## About this task

You can have one approver or multiple approvers. For example, set multiple approvers to have one person do a quality check of the document and a different individual to serve as a final approver. Approvers are assigned a number. The lowest number \(usually number one\) approver always goes first, then any other approvers in ascending chronological order. Multiple approvers can have the same sequence number. For example, two approvers can do a quality check and be assigned sequence number 1. Then, two individuals can be final approvers and be assigned sequence number 2.

## Procedure

1.  Navigate to the document record.

2.  Select the additional actions icon ![Additional Actions icon](../../document-services/image/additional-actions-icon.png) and select **Add Approver**.

3.  Add a user name.

4.  Select a sequence number from the drop-down list.

    Lower numbers approve before higher numbers. For example, approver number one approves before number two.

5.  Click **Add User**.

6.  Repeat steps 2-5 to add more approvers.


**Parent Topic:**[Create or request a new document](t_CreateOrRequestANewDocument.md)

