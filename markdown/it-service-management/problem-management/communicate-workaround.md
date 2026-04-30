---
title: Communicate workaround for Problem
description: Document and communicate workaround to let others know that you are aware of the issue. The workaround is a temporary way to restore service failures and lessen the impact of a Problem for which an actual resolution is not yet available.You can enter a workaround note into a problem record, and then post the information into every associated incident.
locale: en-US
release: yokohama
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Communicating the outcome of a problem, Problem Management, IT Service Management]
---

# Communicate workaround for Problem

Document and communicate workaround to let others know that you are aware of the issue. The workaround is a temporary way to restore service failures and lessen the impact of a Problem for which an actual resolution is not yet available.

## Before you begin

Role required: admin, problem\_admin, problem\_manager or problem\_coordinator

## About this task

When you communicate a workaround, notification is sent to related incidents that a workaround is available. The Incident process is designed to use the workaround information or to notify the user of the same. For more information on notification, refer [Synchronization between incident and problem records](../concept/sync-btwn-inci-prob.md).

**Note:** The topic applies to Problems where you have activated the Problem Management Best Practice — Madrid \(com.snc.best\_practice.problem.madrid\) plugin.

## Procedure

1.  Navigate to **All** &gt; **Problem** &gt; **Open**.

2.  Open the Problem record.

3.  Enter the information in the **Analysis information** &gt; **Workaround** field.

4.  Save the record.

5.  Under Related Links, click **Communicate Workaround**.


**Parent Topic:**[Communicating the outcome of a problem](../concept/communicate-outcome-of-problem.md)

## Communicate workaround \(legacy\)

You can enter a workaround note into a problem record, and then post the information into every associated incident.

### Before you begin

Role required: itil or admin

### About this task

The **Communicate Workaround** related link on the Problem form eliminates the need to manually update each incident related to the Problem.

### Procedure

1.  Open the problem for which you have a workaround.

2.  Enter the information in the **Workaround** field.

3.  Click **Post**.

4.  Click the **Communicate Workaround** related link.

    The problem number and the content of the **Workaround** field are added to the activity stream on all related incidents. By default, any entries made in an incident activity stream field generate an email notification to the **Caller** that you mention on the Incident form.

    If group on-call rotation scheduling is in effect when you communicate a workaround, the system stops the escalations on the associated incidents. Escalation stops because a workaround is available. This action effectively communicates knowledge to the appropriate audience, but does not create a knowledge article.


