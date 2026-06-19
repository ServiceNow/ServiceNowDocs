---
title: Use Interaction Controls Component \(ICC\) call controls with Amazon Connect
description: Agents can access the Active call controls directly from their CSM Configurable Workspace to manage phone interactions. This reduces context switching and improves productivity with Amazon Connect.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/amazon-connect-for-voice-calls.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrating with contact centers, Integrate, Customer Service Management]
---

# Use Interaction Controls Component \(ICC\) call controls with Amazon Connect

Agents can access the Active call controls directly from their CSM Configurable Workspace to manage phone interactions. This reduces context switching and improves productivity with Amazon Connect.

## Amazon Connect for voice calls overview

Amazon Connect integration with ICC provides voice controls enabling agents to handle phone interactions without leaving their Workspace. Call features include actions such as answering, holding, transferring, muting, ending, and accessing the phone directory. Real-time synchronization of agent presence, conformance, and support for various call management features are key achievements of this integration.

To use this feature, complete the steps in the **Enable Interaction Controls** section of the Amazon Connect guided setup for configuring the components. See 

## Key Features for Amazon Connect integration

-   **Call controls**

    Agents can answer, hold, transfer, mute, and end calls directly within their ServiceNow Workspace.

-   **Real-time agent presence updates**

    Agent status is automatically updated in real-time based on the Amazon Connect status change.

-   **Access to the phone directory for dialing calls**

    Agents can use the phone directory to search for customers to make outbound calls. They can also use it on an active call to search for internal agents to transfer customer calls via **Consult** or **Blind** transfer.

-   **Device settings**

    Agents can access the **Device settings** option from the drop-down list in the OpenFrame call window to choose the **Phone type** and change their audio device settings.


An agent performs the following key actions within their Workspace:

## Log in to Amazon Connect

Log in to Amazon Connect and set your status to **Available** within your Workspace. Your presence status updates in real time based on your Amazon Connect status change. You’re now available and ready to receive inbound customer calls.

## State presence

Your presence status synchronizes with Amazon Connect. Any changes in your status due to system events or supervisor actions are reflected in real-time within your inbox ensuring your availability is updated.

**Note:** Presence states values must match between ServiceNow and Amazon Connect to enable bidirectional synchronization.

## Receiving and accepting inbound calls

Use the inbox Alert Card to accept or reject calls. Manage calls via actions such as hold, transfer, mute, or access the transfer target list to transfer calls to other agents or queues. If you’re away from your Workspace, the alert times out and sets you in the **Missed call** status. Change your status back to **Available** to continue receiving calls. Additionally, you can open or close the phone keypad during an active call.

## After call work \(ACW\)

After call work \(ACW\) refers to the tasks agents complete after finishing a call. It can include documenting the conversation details, updating customer records, or following up on unresolved issues. When you hang up a call, the agent is put the ACW state. The Agent is required to change their status from ACW to **Available** to start getting new calls. To enable the agent to go immediately into the **Available** state after disconnecting a call, the Amazon Connect admin can set ACW to zero.

## Initiating outbound calls

Make outbound calls by using the keypad, phone directory, or select-to-call. You can also use letters corresponding to the numbers in the keypad to make outbound calls.

An outbound call creates an Interaction record that displays in the agent’s Workspace displaying the call details.

## Transferring a call to an agent or queue

Access the transfer target list in the Active call window to transfer calls to other agents or queues by searching for an agent or queue. Select thThank you!e contact and begin the call transfer to other agents via **Consult** or **Blind** transfer.

When the second agent accepts the call, the first agent can either end the call or continue to stay in the call. If the first agent ends the call after transferring it to the second agent, the call interaction is ready for wrap-up.

## Device settings

Agents can select the ellipsis icon in the OpenFrame call window and select the **Device settings** option to display the **Amazon Connect - Device settings** window.

-   Select the **Phone type** as **Softphone** and change the audio device settings as required.
-   Select the **Phone type** as **Desk phone** and enter a valid phone number to use the desk or mobile phone.

\[Omitted image "amazon-connect-device-settings-option.png"\] Alt text: Use the Device settings option to update the audio device settings

