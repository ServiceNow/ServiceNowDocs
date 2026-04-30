---
title: Virtual machine pre-built topics for ITSM Virtual Agent
description: ITSM Virtual Agent helps you manage a virtual machine \(VM\) using conversation flows. With this conversation flow, you can start, stop, terminate, describe, and provision a virtual machine.
locale: en-US
release: zurich
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Use pre-built topics, ITSM Virtual Agent, IT Service Management]
---

# Virtual machine pre-built topics for ITSM Virtual Agent

ITSM Virtual Agent helps you manage a virtual machine \(VM\) using conversation flows. With this conversation flow, you can start, stop, terminate, describe, and provision a virtual machine.

There are two categories of virtual machine management topics:

-   **Topics that support AWS and Azure providers**

    Topics that are labeled **CAI** use the Cloud Access Interface to take action on virtual machines provisioned on AWS and Azure. The user must have the sn\_managevm\_va.cai\_vm\_user role to perform these actions. The Virtual Agent admin can set the script variable **max\_records** \(default value=100\) to denote the number of records to be fetched from Azure in a single REST API call. The script variable **carousel\_entries\_threshold** denotes the number of records the carousel input shows. If the number of records are greater than the specified value, a reference choice list is shown to the user.

    Cloud Provisioning and Governance is not required to describe, start, stop, and terminate a VM for AWS and Azure. You can perform the following actions with the Cloud Access Interface \(CAI\) topics for Virtual Agent:

    -   Start a Virtual Machine CAI
    -   Stop a Virtual Machine CAI
    -   Terminate a Virtual Machine CAI
    -   Describe a Virtual Machine CAI
-   **Topics that use the [Cloud Provisioning and Governance plugin](https://www.servicenow.com/docs/access?context=request-plugin-cloud-mgt&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) \(com.snc.cloud.mgmt\)**

    The following topics integrate with Cloud Provisioning and Governance \(required\):

    -   Manage Virtual Machine
    -   Provision Virtual Machine

## Describe Virtual Machine CAI

Users can see details of any assigned VM instance associated with the credential set up by the system administrator.​ If AWS encounters an error, Virtual Agent asks the user to create an incident for further investigation.

Returned details include Provider, Region, and Instance ID. The user can specify which VM to describe, or Virtual Agent can provide a list of available VM instances and the user can select the desired VM to describe.

Requirement: User must have the sn\_managevm\_va.cai\_vm\_user role to perform these actions.

This topic uses the following [topic blocks](itsm-va-topic-blocks.md):

-   Virtual Machine Operation AWS
-   Virtual Machine Operation Azure

![Describe Virtual Machine CAI topic.](../image/DescribeCIAVM2.png)

## Manage Virtual Machine

This topic calls the appropriate topic block \(describe, start, stop, and terminate\) to complete an end-to-end fulfillment of the request.

This topic calls the appropriate topic block \(describe, start, stop, and terminate\) to complete an end-to-end fulfillment of the request. This pre-built topic is read-only. Duplicate the topic in the Virtual Machine Management for Virtual Agent scope and activate it to use the conversation flow.

Requirement: [Cloud Provisioning and Governance plugin](https://www.servicenow.com/docs/access?context=request-plugin-cloud-mgt&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) \(com.snc.cloud.mgmt\)

This topic uses the following [topic blocks](itsm-va-topic-blocks.md):

-   Describe Virtual Machine
-   Start Virtual Machine
-   Stop Virtual Machine
-   Terminate Virtual Machine

## Provision Virtual Machine

Users can request a new VM in a Virtual Agent conversation. Virtual Agent sends a link to the Cloud User Portal to submit the catalog item.

Requirement: [Cloud Provisioning and Governance plugin](https://www.servicenow.com/docs/access?context=request-plugin-cloud-mgt&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) \(com.snc.cloud.mgmt\)

Basic flow:

1.  User requests a virtual machine.
2.  Virtual Agent does one of the following:
    -   Provides a link to the [Cloud User Portal](https://www.servicenow.com/docs/access?context=cloudmgt-cloud-user-portal&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US), along with instructions for requesting a VM from the catalog.
    -   Displays items in the VM catalog that are assigned to the user.

        If the user can't find the desired catalog item, the user can either go directly to the Cloud User Portal or end the conversation.


![Provision Virtual Machine topic.](../image/ProvisionVM3.png)

## Start Virtual Machine CAI

Users can start any assigned virtual machine instance associated with their credentials set up by the system administrator.​ If AWS encounters an error, Virtual Agent asks the user to create an incident for further investigation.

Requirement: User must have the sn\_managevm\_va.cai\_vm\_user role to perform these actions.

This topic uses the following [topic blocks](itsm-va-topic-blocks.md):

-   Virtual Machine Operation AWS
-   Virtual Machine Operation Azure

Basic flow:

1.  User specifies which VM to start, or Virtual Agent provides a list of available VM instances for the user to choose from.
2.  Virtual Agent sends the user an actionable notification when the requested VM starts.
3.  User can choose to see details, request additional instructions to log in to the virtual machine, or skip the notification.

    Virtual Agent also notifies the user if the operation was unsuccessful.


![Start Virtual Machine CAI topic.](../image/StartVMCIA2.png)

## Stop Virtual Machine CAI

Users can stop any assigned VM instance associated with the credentials set up by the system administrator.​ If AWS encounters an error, Virtual Agent asks the user to create an incident for further investigation.

Requirement: User must have the sn\_managevm\_va.cai\_vm\_user role to perform these actions.

This topic uses the following [topic blocks](itsm-va-topic-blocks.md):

-   Virtual Machine Operation AWS
-   Virtual Machine Operation Azure

Basic flow:

1.  User specifies which VM to stop, or Virtual Agent provides a list of available VM instances for the user to choose from.
2.  Virtual Agent sends the user an actionable notification when the requested VM stops.
3.  User can choose to see details, request additional instructions to log in to the virtual machine, or skip the notification.

    Virtual Agent also notifies the user if the operation was unsuccessful.


![Stop Virtual Machine CAI topic.](../image/StopVMCIA3.png)

## Terminate Virtual Machine CAI

Users can terminate any assigned virtual machine instance associated with the credential set up by the system administrator.​ Because termination is a permanent action, Virtual Agent displays the VM details and asks for confirmation.​ If AWS encounters an error, Virtual Agent asks the user to create an incident for further investigation.

Requirement: User must have the sn\_managevm\_va.cai\_vm\_user role to perform these actions.

This topic uses the following [topic blocks](itsm-va-topic-blocks.md):

-   Virtual Machine Operation AWS
-   Virtual Machine Operation Azure

![Terminate Virtual Machine CAI topic.](../image/TerminateVMCAI2.png)

**Parent Topic:**[Using ITSM Virtual Agent pre-built topics](../concept/using-itsm-va.md)

