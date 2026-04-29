---
title: Define a remote instance
description: For each instance, define other instances in the hierarchy as remote instances.
locale: en-US
release: australia
product: Team Development
classification: team-development
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Team Development, Planning your application, Building applications]
---

# Define a remote instance

For each instance, define other instances in the hierarchy as remote instances.

## Before you begin

Role required: none

## About this task

For example, to set up remote instances for Sub-Dev 1:

## Procedure

1.  If IP address access control is enabled, log in to the remote instance and add Sub-Dev 1 as an exception.

2.  On Sub-Dev 1, navigate to **Team Development** &gt; **Remote Instances**.

3.  Click **New**.

4.  Define the remote instance, such as Dev-Parent, by completing the form \(see table\).

    ![Remote Instance](../image/RemoteInstance.png)

5.  Click **Submit**.

6.  Repeat [step 1](t_DefineARemoteInstance.md#step-1-add-exception) through [step 5](t_DefineARemoteInstance.md#step-5-submit) for each instance in the hierarchy that this instance needs to push and pull with \(for example, Sub-Dev 2 and Sub-Dev 3\).

    |Field|Description|
    |-----|-----------|
    |Name|Enter a unique name describing the instance.|
    |Type|Specify whether the remote instance is a development, test, or UAT instance.|
    |Active|Specify whether the local instance communicates with the remote instance as a member of Team Development. Team Development operations such as comparing changes between instances or selecting a parent instance are only available for active remote instances.|
    |URL|Specify the URL of the remote instance using the appropriate transfer protocol. Each remote instance record should have a unique URL. Creating duplicate records with the same URL can cause errors.|
    |Username|Enter the user on the remote instance who authorizes Team Development operations on the instance. This user account must have an appropriate role on the remote instance.|
    |Password|Enter the password of the authorizing user.|
    |Short description|\[Optional\] Enter any other relevant information about the remote instance.|


