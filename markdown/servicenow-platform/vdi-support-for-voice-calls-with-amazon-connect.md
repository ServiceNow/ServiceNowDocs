---
title: Configure a Virtual Desktop Infrastructure \(VDI\) for voice calls with Amazon Connect
description: Contact centers commonly use Virtual Desktop Infrastructure \(VDI\) to optimize agent usage of browser applications. This feature enables agents to use ServiceNow and the Amazon Connect Contact Control Panel \(CCP\) within a VDI environment, taking both inbound and outbound calls without disruption. Administrators can configure groups of agents to use either VDI or non-VDI browsers based on OpenFrame configuration values.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate ServiceNow Voice with Amazon Connect, Integrating Voice with other applications, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure a Virtual Desktop Infrastructure \(VDI\) for voice calls with Amazon Connect

Contact centers commonly use Virtual Desktop Infrastructure \(VDI\) to optimize agent usage of browser applications. This feature enables agents to use ServiceNow and the Amazon Connect Contact Control Panel \(CCP\) within a VDI environment, taking both inbound and outbound calls without disruption. Administrators can configure groups of agents to use either VDI or non-VDI browsers based on OpenFrame configuration values.

## VDI support for voice calls overview

VDI support for Contact Control Panel \(CCP\) enables agents working in virtual desktop environments can access all Amazon Connect call controls within their Workspace.

## Agent Use Case

Agents working in a VDI environment can do the following:

-   Use Amazon Connect CCP within the VDI environment.
-   Receive and handle inbound calls in Amazon CCP.
-   Initiate outbound calls in Amazon CCP.

## Admin Use Case

-   **Dependencies:**

    Role required: Admin

    -   Complete the VDI setup.

        **Note:**

        Refer to the following Amazon Workspace documents for reference:

        -   [Optimize Amazon Connect audio for Amazon WorkSpaces cloud desktops](https://docs.aws.amazon.com/connect/latest/adminguide/using-ccp-vdi-workspaces.html)
        -   [Amazon Connect audio optimization for WorkSpaces](https://docs.aws.amazon.com/connect/latest/adminguide/using-ccp-vdi-workspaces.html)
        Refer to the following VDI platform documents for reference:

        -   [Use Amazon Connect in a VDI environment](https://docs.aws.amazon.com/connect/latest/adminguide/using-ccp-vdi.html)
        -   [Setup network to use the Amazon Connect CCP](https://docs.aws.amazon.com/connect/latest/adminguide/ccp-networking.html)
        -   [System settings for Amazon Connect with Citrix VDI](https://docs.aws.amazon.com/connect/latest/adminguide/using-ccp-vdi-citrix-step-by-step.html)
        Refer to the Omnissa VDI document for reference: [Optimize Amazon Connect audio for Omnissa cloud desktops](https://docs.aws.amazon.com/connect/latest/adminguide/using-ccp-vdi-omnissa-step-by-step.html)

    -   Configure VDI setting in **OpenFrame Configuration** for the VDI type the agents use. The following VDI types are supported:

        -   CITRIX
        -   AWS\_WORKSPACE
        -   OMNISSA
        **Note:** The VDI type value in the **OpenFrame Configuration** must match the value from the preceding list.

    -   Manage separate agent groups with different browser environments from a single administration interface.
-   **Enable VDI support for agents using Amazon Connect:**
    1.  To enable VDI support for agents using ServiceNow Voice for Amazon Connect, configure the VDI support type. Set the **OpenFrame Configuration** value to specify the VDI type. Refer to the Admin use case.
    2.  Set the **OpenFrame Configuration** value to specify the VDI type.
    3.  Assign agents to the appropriate group based on their desktop environment.
    4.  Verify that agents can log in to the Amazon Connect CCP and handle calls from within their VDI session.

**Parent Topic:**[Integrate ServiceNow Voice with Amazon Connect](../task/integrate-ccc-amazonconnect.md)

