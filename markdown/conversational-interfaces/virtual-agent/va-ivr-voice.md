---
title: Conversational IVR with Amazon Connect
description: ServiceNow's Conversational IVR with Amazon Connect enables Conversational Interactive Voice Response \(IVR\) to be conducted by your instance. Users will be able to conduct conversations with a bot via the phone channel, powered by ServiceNow Virtual Agent. Conversational IVR with Amazon Connect is available with the installation of Conversational IVR with Amazon Connect \(com.sn.va.amz.connect\) plugin.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Virtual Agent integration with Voice channels, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Conversational IVR with Amazon Connect

ServiceNow's Conversational IVR with Amazon Connect enables Conversational Interactive Voice Response \(IVR\) to be conducted by your instance. Users will be able to conduct conversations with a bot via the phone channel, powered by ServiceNow Virtual Agent. Conversational IVR with Amazon Connect is available with the installation of Conversational IVR with Amazon Connect \(com.sn.va.amz.connect\) plugin.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Overview of Conversational IVR with Amazon Connect

Enable your users to initiate an IVR \(Interactive Voice Response\) conversation with your Virtual Agent Agent by building an integration with Amazon Connect. Using the Conversational IVR with Amazon Connect, you can enable a user to have a voice-based conversation with your Virtual Agent using Amazon Connect to help provide this functionality. This integration also provides the user the flexibility to connect with an agent using ServiceNow AWA Advanced Work Assignment \(AWA\) over SoftPhone.

## Conversational IVR highlights

-   Use Virtual Agent topics as a Conversational IVR to enable deflection in Phone channels, providing consistent end-user experience.
-   Enable true-omnichannel flow including routing Phone to the Conversational VA-IVR.
-   In case of escalations, route calls smoothly to live agents using AWA via conversational infrastructure.

To get started with the Conversational Integration with Amazon Connect application, see [Install Conversational IVR with Amazon Connect](../task/install-va-ivr.md).

## Setup Conversational Integration with Amazon Connect

Install and configure the Conversational Integration with Amazon Connect application to enable users to have a conversational voice response with their Virtual Agent.

1.  To install the pre-built adapter for Conversational Integration with Amazon Connect, see [Install Conversational IVR with Amazon Connect](../task/install-va-ivr.md).
2.  To set up your Amazon Connect account if not already configured, see [Configuring your AWS account for use with Conversational IVR](configure-aws-account.md).
3.  To configure Conversational Integration with Amazon Connect, see [Configure Conversational IVR with Amazon Connect](../task/configure-va-ivr.md).
4.  To set up Live Agent transfer for Conversational IVR, see [Sync Agents to setup Live Agent transfer](../task/setup-live-agent-transfer.md).
5.  To configure user authentication, see [Configure user authentication for Conversational IVR](../task/setup-user-authentication-ivr.md).
6.  To modify the Conversational Integration with Amazon Connect settings for the best interactive voice response, see [Manage bot messages for Conversational IVR](../task/edit-va-ivr-messages.md).
7.  To configure callback functionality, see [Configure callback behavior for a channel](https://www.servicenow.com/docs/access?context=configure-callback-behavior&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

![Workflow describing the sequence of processes carried out in Conversational IVR with Amazon Connect integration.](../images/workflow-ivr-amz-cnct.png "Workflow of Conversational IVR with Amazon Connect")

